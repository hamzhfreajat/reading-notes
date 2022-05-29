# Cognito
The Amplify Auth category provides an interface for authenticating a user.

## Amazon Cognito

Amazon Cognito lets you add user sign-up, sign-in, and access control to your web and mobile apps quickly and easily. Amazon Cognito scales to millions of users and supports sign-in with social identity providers, such as Apple, Facebook, Google, and Amazon, and enterprise identity providers via SAML 2.0 and OpenID Connect.

## Configure Auth Category
execute the command:

    amplify add auth

then execute the command:

    amplify push

Add the following dependency : 

    dependencies {
    implementation 'com.amplifyframework:aws-auth-cognito:1.35.4'
    }

## Sign in
The Auth category can be used to register a user, confirm attributes like email/phone, and sign in with optional multi-factor authentication. It is set up to use Amazon Cognito User Pools which manages the users and their properties.

### Register a user

    AuthSignUpOptions options = AuthSignUpOptions.builder()
        .userAttribute(AuthUserAttributeKey.email(), "my@email.com")
        .build();
        Amplify.Auth.signUp("username", "Password123", options,
        result -> Log.i("AuthQuickStart", "Result: " + result.toString()),
        error -> Log.e("AuthQuickStart", "Sign up failed", error)
    );

## Sign out
Invoke the signOut api to sign out a user from the Auth category.

    Amplify.Auth.signOut(
        () -> Log.i("AuthQuickstart", "Signed out successfully"),
        error -> Log.e("AuthQuickstart", error.toString())
    );