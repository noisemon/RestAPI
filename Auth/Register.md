**Register new account**
----
  Registers new account to the system. Needs to be done at least once. The user creates an account, and afterwards, once logged in, can access his resources (Noise Monitors). Username should be a valid emailaddress which will have to be validated by the user. Password needs to be at least 8 characters long, contain lowercase letters, uppercase letters, digits, and special characters.

* **URL**

  /auth/register

* **Method:**

  `POST`
  
* **URL Params**

  None

* **Data Params**

  ```
  {
    username: "donald.trump@whitehouse.com",
    password: "ImDumb@ssNr1"
  }
  ```

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{ message: "Registration succeeded" }`
 
* **Error Response:**

  * **Code:** 400 BAD REQUEST <br />
    **Content:** `{ error : "Missing registration information." }`
    
* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/auth/register",
      dataType: "json",
      data: {
        username: "donald.trump@whitehouse.com",
        password: "ImDumb@ssNr1"
      }
      type : "POST",
      success : function(r) {
        console.log(r);
      }
    });
  ```

* **Notes**

  Make sure SSL is used.
