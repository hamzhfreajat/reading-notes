# Spring Boot and OAuth2
There are several samples building on each other, adding new features at each step:

- simple: a very basic static app with just a home page and unconditional login via Spring Boot’s OAuth 2.0 configuration properties (if you visit the home page, you will be automatically redirected to GitHub).

- click: adds an explicit link that the user has to click to login.

- logout: adds a logout link as well for authenticated users.

- two-providers: adds a second login provider so the user can choose on the home page which one to use.

custom-error: adds an error message for unauthenticated users, and a custom authentication based on GitHub’s API.
## Single Sign On With GitHub
### Creating a New Project
you need to create a Spring Boot application, which can be done in a number of ways like : 

    $ mkdir ui && cd ui
    $ curl https://start.spring.io/starter.tgz -d style=web -d name=simple | tar -xzvf -

### Add a Home Page

    <!doctype html>
    <html lang="en">
    <head>
        <meta charset="utf-8"/>
        <meta http-equiv="X-UA-Compatible" content="IE=edge"/>
        <title>Demo</title>
        <meta name="description" content=""/>
        <meta name="viewport" content="width=device-width"/>
        <base href="/"/>
        <link rel="stylesheet" type="text/css" href="/webjars/bootstrap/css/bootstrap.min.css"/>
        <script type="text/javascript" src="/webjars/jquery/jquery.min.js"></script>
        <script type="text/javascript" src="/webjars/bootstrap/js/bootstrap.min.js"></script>
    </head>
    <body>
        <h1>Demo</h1>
        <div class="container"></div>
    </body>
    </html>

### Add dependency

    <dependency>
        <groupId>org.webjars</groupId>
        <artifactId>jquery</artifactId>
        <version>3.4.1</version>
    </dependency>
    <dependency>
        <groupId>org.webjars</groupId>
        <artifactId>bootstrap</artifactId>
        <version>4.3.1</version>
    </dependency>
    <dependency>
        <groupId>org.webjars</groupId>
        <artifactId>webjars-locator-core</artifactId>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-oauth2-client</artifactId>
    </dependency>