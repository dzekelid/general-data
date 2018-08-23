{
  "info": {
    "name": "Data.gov API Add Organizations Org Logo",
    "_postman_id": "37680b9b-e832-4706-a620-7b6e4c0b3865",
    "description": "Upload a new logo",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "organizations",
      "item": [
        {
          "id": "3da415ec-68b0-4dd5-8867-1f2ff3be08a1",
          "name": "postOrganizationsOrgLogo",
          "request": {
            "url": {
              "protocol": "http",
              "host": "catalog.data.gov",
              "path": [
                "api",
                "3",
                "organizations/:org/logo"
              ],
              "variable": [
                {
                  "id": "org",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "bbox",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                },
                {
                  "key": "file",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                }
              ]
            },
            "description": "Upload a new logo"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ef1d09ef-a10f-4637-a9e8-20a3fe84b916"
            }
          ]
        }
      ]
    }
  ]
}