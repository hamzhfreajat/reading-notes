# Spring Authentication
authentication is just `who are you?` .

## Authentication Manager
An `AuthenticationManager` can do one of 3 things in its authenticate() method:

- Return an Authentication (normally with authenticated=true) if it can verify that the input represents a valid principal.

- Throw an AuthenticationException if it believes that the input represents an invalid principal.

- Return null if it cannot decide.

## Web Security
Spring Security in the web tier (for UIs and HTTP back ends) is based on Servlet Filters to become more secure
![Filter](../assets/class16/filter.png)