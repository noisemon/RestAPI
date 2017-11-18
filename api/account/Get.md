**Get Account information**
----
  Retrieves all account information. This can (and probably will have to be) extended with extra information. Please contact Michel or Salva for more info. 

* **URL**

  /api/account/get

* **Method:**

  `GET`
  
* **URL Params**

  None

* **Data Params**

  None

* **Success Response:**

  * **Code:** 200 <br />
    **Content:**
    ```
    {
      <example to be provided>
    }
    ```

* **Error Response:**

  * **Code:** 400 BAD REQUEST <br />
    **Content:** `{ error : "Missing requested Account ID." }`

  OR

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Please log in before using the API." }`
    
* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/api/account/get?id=qewfnwqrgqeRGQEGRCQgniweifcqwrgQQERGq",
      dataType: "json",
      type : "GET",
      success : function(r) {
        console.log(r);
      }
    });
  ```

* **Notes**

  * Make sure SSL is used.
