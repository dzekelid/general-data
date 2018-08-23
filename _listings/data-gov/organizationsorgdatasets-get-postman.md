{
  "info": {
    "name": "Data.gov API Get Organizations Org Datasets",
    "_postman_id": "e0ed9805-db36-4f6c-b1ff-69431eca2112",
    "description": "List organization datasets (including private ones when member)",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "organizations",
      "item": [
        {
          "id": "531f7485-360c-4f40-bc27-3ff3ea512d8d",
          "name": "getOrganizationsOrgDatasets",
          "request": {
            "url": {
              "protocol": "http",
              "host": "catalog.data.gov",
              "path": [
                "api",
                "3",
                "organizations/:org/datasets/"
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
            "description": "List organization datasets (including private ones when member)"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "951061c5-437c-46eb-a6de-472e93ed32f1"
            }
          ]
        }
      ]
    }
  ]
}