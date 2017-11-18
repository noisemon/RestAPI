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
    **Content:** `{ id : 12, name : "Michael Bloom" }`
 
* **Error Response:**

  * **Code:** 404 NOT FOUND <br />
    **Content:** `{ error : "User doesn't exist" }`

  OR

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "You are unauthorized to make this request." }`

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
