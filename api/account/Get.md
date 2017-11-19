**Get Account information**
----
  Retrieves all account information. This can (and probably will have to be) extended with extra information. Please contact Michel or Salva for more info. 

* **URL**

  /api/account/get

* **Method:**

  `GET`
  
* **URL Params**

   **Optional:**
 
 * **ID** The Account ID to be retrieved. <br/>
   **Example** `id=OGRmNWI1NGItM2U3NC00ZTlhLTk3MzgtNjAyYmY1ZmJhNzdh`

* **Data Params**

  None

* **Success Response:**

  * **Code:** 200 <br />
    **Content:**
    ```
    {
      id: "OGRmNWI1NGItM2U3NC00ZTlhLTk3MzgtNjAyYmY1ZmJhNzdh",
      email: "lemmy.kilmister@motorhead.com",
      god: "1"
    }
    ```

* **Error Response:**

  * **Code:** 400 BAD REQUEST <br />
    **Content:** `{ error : "Invalid Account ID." }`

  OR

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Please log in before using the API." }`
    
* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/api/account/get?id=OGRmNWI1NGItM2U3NC00ZTlhLTk3MzgtNjAyYmY1ZmJhNzdh",
      dataType: "json",
      type : "GET",
      success : function(r) {
        console.log(r);
      }
    });
  ```

* **Notes**

  * Make sure SSL is used.
