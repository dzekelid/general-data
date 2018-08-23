{
  "info": {
    "name": "Data.gov API Get Organizations Org Membership",
    "_postman_id": "2aaa815e-f99f-43ec-9d3b-705743a85f3d",
    "description": "List membership requests for a given organization",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "organizations",
      "item": [
        {
          "id": "f5c76c37-460e-4149-b375-1ba2ac523130",
          "name": "getOrganizationsOrgMembership",
          "request": {
            "url": {
              "protocol": "http",
              "host": "catalog.data.gov",
              "path": [
                "api",
                "3",
                "organizations/:org/membership/"
              ],
              "query": [
                {
                  "key": "status",
                  "value": "%7B%7D",
                  "disabled": false
                }
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
            "description": "List membership requests for a given organization"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6452f013-8d99-4089-9b24-a970fe50d364"
            }
          ]
        }
      ]
    }
  ]
}