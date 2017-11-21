**Get Account count**
----
  Retrieves the number of Noise Monitors the current/specific account has. Administrators can also get the total number of Noise Monitors registered in the system. 

* **URL**

  /api/noisemonitor/getcount

* **Method:**

  `GET`
  
* **URL Params**

   **Optional:**
 
    * **ID** Specify the Account ID from which you want to count the number of Noise Monitors. <br/>
      **Example** `id=OGRmNWI1NGItM2U3NC00ZTlhLTk3MzgtNjAyYmY1ZmJhNzdh`

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
      url: "/api/noisemonitor/getcount",
      dataType: "json",
      type : "GET",
      success : function(r) {
        console.log(r);
      }
    });
  ```

* **Notes**

  * Make sure SSL is used.
  * If **no** account ID is specified, the method returns the number of Noise Monitors of the current account, unless the current account is an administrator. In that case, the method returns the total number of Noise Monitors in the entire system.
  * If an account ID is specified, the method only returns the number of Noise Monitors of that specific account, if the current account is administrator. Otherwise, the method fails with a non-authorization message.
