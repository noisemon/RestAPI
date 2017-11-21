**Get Account count information**
----
  Retrieves the number of accounts. Returns always 1 in case you are not an administrator. 

* **URL**

  /api/account/getcount

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
      count: 12
    }
    ```

* **Error Response:**

  * **Code:** 400 BAD REQUEST <br />
    **Content:** `{ error : "Could not find active Account Entity." }`

  OR

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Please log in before using the API." }`
    
* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/api/account/getcount",
      dataType: "json",
      type : "GET",
      success : function(r) {
        console.log(r);
      }
    });
  ```

* **Notes**

  * Make sure SSL is used.
  * Method only makes sense for administrators.
