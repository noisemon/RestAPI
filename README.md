# Rest API Documentation
This document describes the Rest API which is used to access the NoiseMon backoffice.

## Authentication
In order to create an account, a user must first register. For registration he needs a valid email address and choose a password. Every registration must be validated by clicking on a link received by email.
Once registered, a user is able to login using his credentials, and he can add/view/edit his Noise Monitors.
If a user forgets his password, he can request a new one using a specific endpoint.

The following endpoints allow for these actions:
  * [Registration](./Auth/Register.md)
  * [Verification](./Auth/Verify.md)
  * [Forgot password](./Auth/ForgotPassword.md)
  * [Login](./Auth/Login.md)
  * [Logout](./Auth/Logout.md)

## Configuration
Once logged in, a user can configure his account, administer his Noise Monitors etc.

Endpoints for **Account** configuration:
 * [List](./api/account/List.md) - List all accounts. (Only for administrators)
 * [Get](./api/account/Get.md) - Get details on current or specific account. (Specific only for administrators)

<br />
**still some work to be done here**

Endpoints for **Noise Monitor** configuration:

<br />
**still some work to be done here**

## Data
Finally, there are endpoints to view the current and historical Noise Monitors data

Endpoints for **Noise Monitor** data:

<br />
**still some work to be done here**
