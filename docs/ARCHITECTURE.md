# OAuth:

## 1. OAuth exists so your app (interview-protocol) never sees your Gmail password. Instead:

### You (the user) log in directly with Google
### Google gives interview-protocol a token
### interview-protocol uses the token to read your emails
### Google can revoke the token anytime, but your password stays safe

## The benefit: If interview-protocol gets hacked, your Gmail password is still secure (they only got a token, which you can revoke).

## 2. An access token is a short term token used for secure API requests, whereas a refresh token is a long term token used only to ask for a new access token when the previous one expires.

## 3. A stolen refresh token is worse than a stolen password because it bypasses MFA. They can generate new access tokens indefinitely without triggering security alerts.


# REST APIs and JSON

## 1. The difference between GET and POST is that a GET is a read request, whereas a POST is a write request.

## 2. The HTTP methods indicate the specific action to be performed on a given resource when a client communicates with a server. They form the backbone of web communication and RESTful APIs, mapping directly to standard data management operations.

## 3. When you make an API call, you send an HTTP request to the server.

# ENVs and Setup

## 1. Storing API Keys in your code means they are open to the public, and as such can be taken and used maliciously to anyone who can see the repository or the code.

## 2. A .env file is a local text config file which stores environment variables and sensitive data such as API keys which should not be committed to GitHub.

## 3. At execution, an env parser library looks for an .env file, and parses it one line at a time, separating the keys from the values as process.env.KEY_NAME.
