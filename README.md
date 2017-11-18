# Rest API Documentation
This document describes the Rest API which is used to in the NoiseMon backoffice.

## Authentication
In order to create an account, a user must first register. For registration he needs a valid email address and choose a password. Every registration must be validated by clicking on a link received by email.
Once registered, a user is able to login using his credentials, and he can add/view/edit his Noise Monitors.
If a user forgets his password, he can request a new one using a specific endpoint.

The following endpoints allow for these actions:
  * [Registration](RestAPI/Auth/Register.md)
  * [Verification](RestAPI/Auth/Verify.md)
  * Forgot password
  * Login
  * Logout
