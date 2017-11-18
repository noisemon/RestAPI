**Login**
----
  Logs the user in, and creates a session for him. Upon success, the response will contain a **AUTH_KEY** header which must be sent on each API request.

* **URL**

  /auth/login

* **Method:**

  `POST`
  
* **URL Params**

  None

* **Data Params**

  ```
  {
    email: "donald.trump@whitehouse.com",
    password: "ImDumb@ssNr1"
  }
  ```

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{ message: "Login succeeded" }`
 
* **Error Response:**

  * **Code:** 400 BAD REQUEST <br />
    **Content:** `{ error : "Invalid email or password specified." }`
        
* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/auth/login",
      dataType: "json",
      data: {
        email: "donald.trump@whitehouse.com",
        password: "ImDumb@ssNr1"
      }
      type : "POST",
      success : function(r) {
        console.log(r);
      }
    });
  ```

* **Notes**

  * Make sure SSL is used.
