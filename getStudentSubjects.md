**getStudentSubjects**
----
  Returns a structure of Students with an array of structured Subject data in JSON format.

* **Version:**

  2

* **Method:**

  `GET | POST`
  
*  **Params:**

   **Required:**

   `code [string]` -  Valid student code or 'all'
   
   **Optional:**

   none

   **Conditional:**
 
   none

* **Success Response:**

    ```javascript
      {
        "0009080": [
          {
            "semester": 1,
            "year_grp_desc": 11,
            "sub_code": "ANCH20",
            "from_date": "",
            "sub_short": "AnHist",
            "year_grp": 11,
            "year_num": 2018,
            "to_date": "",
            "student_code": "0009080",
            "sub_long": "Ancient History",
            "class": "A",
            "sub_type": "COR"
          },
          {
            "semester": 1,
            "year_grp_desc": 11,
            "sub_code": "0080",
            "from_date": "",
            "sub_short": "Art",
            "year_grp": 11,
            "year_num": 2018,
            "to_date": "",
            "student_code": "0009080",
            "sub_long": "Art AR Desc",
            "class": "C",
            "sub_type": "ELE"
          },
          {
            "semester": 1,
            "year_grp_desc": 11,
            "sub_code": "ASSEMBLY",
            "from_date": "",
            "sub_short": "ASSEMB",
            "year_grp": 11,
            "year_num": 2018,
            "to_date": "",
            "student_code": "0009080",
            "sub_long": "School Assembly",
            "class": "A",
            "sub_type": "NON"
          }
        ],
        "0009704": [
          {
          "semester": 1,
          "year_grp_desc": 6,
          "sub_code": "ASSEMBLY",
          "from_date": "",
          "sub_short": "ASSEMB",
          "year_grp": 6,
          "year_num": 2018,
          "to_date": "",
          "student_code": "0009704",
          "sub_long": "School Assembly",
          "class": "A",
          "sub_type": "NON"
          }
        ]
      }
    ```
 
* **Error Response:**

    `code` not supplied
    ```javascript
    __invalid: {
      "code": "field is required"
    }
    ```
   
* **Sample Parameters:**

  ```javascript
    { 
      "code":"0009080"
    }
  ```

* **Sample GET:** (With URL Encoded `token`)

  ```HTML
    http://api.tasscloud.com.au/tassweb/api/?method=GetStudentsSubjects&appcode=DEMOSD&company=10&v=2&token=l1D8owEn111IHcXLRwXTB0oU2GX6rj%2BISqa9zXA8We1Gqx9%2Fzb%2BcbVFartivsDN%2FxGgAIIjtABAYfzYPqTCpLf3gb0nW3h%2FTrPFLMhAdNcVvHD0Gz4FkRj5jRAD1aAGQ
  ```
  
* **Sample POST:**

  ```HTML
    <form id="postForm" name="postForm" method="POST" action="http://api.tasscloud.com.au/tassweb/api/">
       <input type="hidden" name="method" value="getStudentsSubjects">
       <input type="hidden" name="appcode" value="DEMOSD">
       <input type="hidden" name="company" value="10">
       <input type="hidden" name="v" value="2">
       <textarea name="token">l1D8owEn111IHcXLRwXTB0oU2GX6rj+ISqa9zXA8We1Gqx9/zb+cbVFartivsDN/xGgAIIjtABAYfzYPqTCpLf3gb0nW3h/TrPFLMhAdNcVvHD0Gz4FkRj5jRAD1aAGQ</textarea>
    </form>
  ```