{
  "info": {
    "name": "Data.gov API Get Organizations Org",
    "_postman_id": "3dfd3438-f543-4588-bde2-d3f12262e564",
    "description": "Get a organization given its identifier",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "organizations",
      "item": [
        {
          "id": "402562ac-80c3-4d24-9b4e-6c9ca6b1638a",
          "name": "getOrganizationsOrg",
          "request": {
            "url": {
              "protocol": "http",
              "host": "catalog.data.gov",
              "path": [
                "api",
                "3",
                "organizations/:org/"
              ],
              "variable": [
                {
                  "id": "org",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get a organization given its identifier"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d8e48291-c8ea-428a-b147-4b3daa5b08a4"
            }
          ]
        }
      ]
    }
  ]
}