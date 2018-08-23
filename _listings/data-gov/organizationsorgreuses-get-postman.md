{
  "info": {
    "name": "Data.gov API Get Organizations Org Reuses",
    "_postman_id": "ba6321ef-e43f-477f-8f2d-e3bdb1b79a9a",
    "description": "List organization reuses (including private ones when member)",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "organizations",
      "item": [
        {
          "id": "1a697531-677e-4a73-86f5-59f705456c18",
          "name": "getOrganizationsOrgReuses",
          "request": {
            "url": {
              "protocol": "http",
              "host": "catalog.data.gov",
              "path": [
                "api",
                "3",
                "organizations/:org/reuses/"
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
            "description": "List organization reuses (including private ones when member)"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "922ee1a0-f41c-4640-8b56-526847067e45"
            }
          ]
        }
      ]
    }
  ]
}