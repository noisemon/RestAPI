**Update account details**
----
  Updates the account details. Only the email address can **not** be changed.

* **URL**

  /api/account/update

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
    **Content:** `{ message: "Account updated successfully." }`
 
* **Error Response:**

  * **Code:** 400 BAD REQUEST <br />
    **Content:** `{ error : "Invalid email or password specified." }`
        
* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/api/account/update",
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
