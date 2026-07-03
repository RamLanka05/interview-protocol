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

## 1. A REST API is a form of API that allows for two different softwares to communicate and exchange data over the internet.

## 2. 