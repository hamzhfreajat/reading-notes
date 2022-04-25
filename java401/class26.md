# Android Fundamentals
Android apps can be written using Kotlin, Java, and C++ languages. The SDK tools will compile your code to APK . 

## App components
- Activities
- Services
- Broadcast receivers
- Content providers

### Activities
An activity is the entry point for interacting with the user. It represents a single screen with a user interface .

### Services
A service is a general-purpose entry point for keeping an app running in the background for all kinds of reasons.

### Broadcast receivers
A broadcast receiver is a component that enables the system to deliver events to the app outside of a regular user flow, allowing the app to respond to system-wide broadcast announcements.

### Content providers

A content provider manages a shared set of app data that you can store in the file system, in a SQLite database, on the web, or on any other persistent storage location that your app can access.

## Intent
Intents bind individual components to each other at runtime , An intent is created with an Intent object, which defines a message to activate either a specific component (explicit intent) or a specific type of component (implicit intent).

## The manifest file
`AndroidManifest.xml` Your app must declare all its components in this file, which must be at the root of the app project directory.

    <?xml version="1.0" encoding="utf-8"?>
    <manifest ... >
    <application android:icon="@drawable/app_icon.png" ... >
    <activity android:name="com.example.project.ExampleActivity"
    android:label="@string/example_label" ... >
    </activity>
    ...
    </application>
    </manifest>