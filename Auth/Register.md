**Register new account**
----
  Registers new account.

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
