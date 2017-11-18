**Verify account registration**
----
  Validates the authentication code the user received by email upon registration. If this succeeds, the account is created, and the user is able to log in.

* **URL**

  /auth/verify

* **Method:**

  `GET`
  
* **URL Params**

  None

* **Data Params**

   **Required:**
 
 * **Code** The activation code received by email by the user. <br/>
   **Example** `code=OGRmNWI1NGItM2U3NC00ZTlhLTk3MzgtNjAyYmY1ZmJhNzdh`

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{ message: "Verification succeeded" }`
 
* **Error Response:**

  * **Code:** 400 BAD REQUEST <br />
    **Content:** `{ error : "Invalid activation code." }`
    
* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/auth/verify?code=OGRmNWI1NGItM2U3NC00ZTlhLTk3MzgtNjAyYmY1ZmJhNzdh",
      dataType: "json",
      type : "GET",
      success : function(r) {
        console.log(r);
      }
    });
  ```

* **Notes**

  * Make sure SSL is used.
  * This method is normally only called by the email client of the user, after he performed a registration.
