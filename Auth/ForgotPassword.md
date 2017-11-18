**Forgot Password**
----
  Allows a user who forgot his password, to have it reset to a new system generated password. The new password will be sent by email to him.

* **URL**

  /auth/forgotpass

* **Method:**

  `POST`
  
* **URL Params**

  None

* **Data Params**

  ```
  {
    email: "donald.trump@whitehouse.com"
  }
  ```

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{ message: "Password reset successfully" }`
 
* **Error Response:**

  * **Code:** 400 BAD REQUEST <br />
    **Content:** `{ error : "Missing email information" }`
    
* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/auth/forgotpass",
      dataType: "json",
      data: {
        email: "donald.trump@whitehouse.com"
      }
      type : "POST",
      success : function(r) {
        console.log(r);
      }
    });
  ```

* **Notes**

  * Make sure SSL is used.
  * Upon success, the user will receive an email with an his new password.
