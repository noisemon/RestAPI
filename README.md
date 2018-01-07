# Rest API Documentation
This document describes the Rest API which is used to access the NoiseMon backoffice.

## Authentication
In order to create an account, a user must first register. For registration he needs a valid email address and choose a password. Every registration must be validated by clicking on a link received by email.
Once registered, a user is able to login using his credentials, and he can add/view/edit his Noise Monitors.
If a user forgets his password, he can request a new one using a specific endpoint.

The following endpoints allow for these actions:
  * [Registration](./Auth/Register.md)
  * [Verification](./Auth/Verify.md)
  * [Login](./Auth/Login.md)
  * [Forgot password](./Auth/ForgotPassword.md)
  * [Logout](./Auth/Logout.md)

## Configuration
Once logged in, a user can configure his account, administer his Noise Monitors etc.

Endpoints for **Account** configuration:
 * [List all accounts](./api/account/List.md) - Only for administrators.
 * [Get count of accounts](./api/account/GetCount.md) - Only for administrators.
 * [Get details on current/specific account](./api/account/Get.md) - Specific only for administrators.
 * [Update details of current/specific account](./api/account/Update.md) - Specific only for administrators.

Endpoints for **Noise Monitor** configuration:
 * [List all Noise Monitors](./api/noisemonitor/List.md)
 * [Get count of Noise Monitors for current/specific/all account(s)](./api/noisemonitor/GetCount.md)
 * [Get details on current/specific Noise Monitor](./api/noisemonitor/Get.md) - Specific only for administrators.
 * [Update details of a Noise Monitor](./api/noisemonitor/Update.md)
 * [Add Noise Monitor to account](./api/noisemonitor/Add.md)
 * [Remove Noise Monitor from account](./api/noisemonitor/Remove.md)

Endpoints for **Noise Monitor Group** configuration:
 * [List all Noise Monitor Groups](./api/noisemonitorgroup/List.md)
 * [Get count of Noise Monitor Groups for current account(s)](./api/noisemonitorgroup/GetCount.md)
 * [Get details on current/specific Noise Monitor Group](./api/noisemonitorgroup/Get.md)
 * [Update details of a Noise Monitor Group](./api/noisemonitorgroup/Update.md)
 * [Create a new Noise Monitor Group](./api/noisemonitorgroup/Create.md)
 * [Delete a Noise Monitor Group](./api/noisemonitorgroup/Delete.md)
 * [Add Noise Monitor to Group](./api/noisemonitorgroup/Add.md)
 * [Remove Noise Monitor from Group](./api/noisemonitorgroup/Remove.md)

## Data
Finally, there are endpoints to view the current and historical Noise Monitors data

Endpoints for **Noise Monitor** data:
 * [Get last x seconds of Noise Data from a Noise Monitor](./api/noise/Get.md)
