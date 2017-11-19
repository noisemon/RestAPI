**List all noise monitors for an account**
----
  Provides a way of listing the Noise Monitors that belong to a specific Account. Note that if no account ID is supplied, only the Noise Monitors for that account are shown, unless the user has **god** rights. In that case **ALL** noisemonitors will be returned; that can be a **HUGE** list!

* **URL**

  /api/noisemonitor/list

* **Method:**

  `GET`
  
* **URL Params**

   **Optional:**
 
    * **ID** Specify the Account ID from which you wish to retrieve the Noise Monitors. <br/>
      **Example** `id=OGRmNWI1NGItM2U3NC00ZTlhLTk3MzgtNjAyYmY1ZmJhNzdh`

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
    **Content:** `{ error : "Not enough rights." }`

  OR

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Please log in before using the API." }`
    
* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/api/noisemonitor/list?id=OGRmNWI1NGItM2U3NC00ZTlhLTk3MzgtNjAyYmY1ZmJhNzdh",
      dataType: "json",
      type : "GET",
      success : function(r) {
        console.log(r);
      }
    });
  ```

* **Notes**

  * Make sure SSL is used.
  * Please note that if you omit Account ID, you may receive **all** Noise Monitors if the user has 'god' rights; that list can be huge !
