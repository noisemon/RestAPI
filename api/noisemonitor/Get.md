**Get Noise Monitor information**
----
  Retrieves all Noise Monitor information. This can (and probably will have to be) extended with extra information. Please contact Michel or Salva for more info. 

* **URL**

  /api/noisemonitor/get

* **Method:**

  `GET`
  
* **URL Params**

   **Required:**
 
 * **MAC** Specify the Noise Monitor ID fro which you wish to retrieve the information. <br/>
   **Example** `mac=01AE3B567E22`

* **Data Params**

  None

* **Success Response:**

  * **Code:** 200 <br />
    **Content:**
    ```
    {
      mac: "01AE3B567E22",
      swversion: "1",
      hwversion: "1",
      description: "Living room",
      threshold: "70.0",
      duration: "5",
      smsemail: ""
    }
    ```

* **Error Response:**

  * **Code:** 400 BAD REQUEST <br />
    **Content:** `{ error : "Invalid Noise Monitor ID." }`

  OR

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Please log in before using the API." }`
    
* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/api/noisemonitor/get?mac=01AE3B567E22",
      dataType: "json",
      type : "GET",
      success : function(r) {
        console.log(r);
      }
    });
  ```

* **Notes**

  * Make sure SSL is used.
