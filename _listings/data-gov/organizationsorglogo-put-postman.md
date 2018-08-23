{
  "info": {
    "name": "Data.gov API Put Organizations Org Logo",
    "_postman_id": "3d7855e6-9359-4bd3-b9d6-8ba89a8024be",
    "description": "Set the logo BBox",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "organizations",
      "item": [
        {
          "id": "b13a32cd-7722-4402-9ae2-a5a0881598ed",
          "name": "putOrganizationsOrgLogo",
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
            "method": "PUT",
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
            "description": "Set the logo BBox"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0c1cd6bf-2a66-46ea-8296-e99ffd517b9f"
            }
          ]
        }
      ]
    }
  ]
}