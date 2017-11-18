**Logout**
----
  Logs the user out; the **AUTH_KEY** associated with his session gets destroyed.

* **URL**

  /auth/logout

* **Method:**

  `DELETE`
  
* **URL Params**

  None

* **Data Params**

  None

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{ message: "Logout succeeded" }`
 
* **Error Response:**

  * **Code:** 400 BAD REQUEST <br />
    **Content:** `{ error : "No session ID provided." }`

* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/auth/logout",
      dataType: "json",
      type : "DELETE",
      beforeSend: function(request) {
        request.setRequestHeader("AUTH_KEY", authKey);
      },
      success : function(r) {
        console.log(r);
      }
    });
  ```

* **Notes**

  * Make sure SSL is used.
