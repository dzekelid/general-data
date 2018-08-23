{
  "info": {
    "name": "Transport for London Unified Accent Stats year",
    "_postman_id": "79de4ff1-747d-431c-a433-919fba113f82",
    "description": "Gets all accident details for accidents occuring in the specified year.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Accent",
      "item": [
        {
          "id": "544c3bdb-a326-4a3d-bfb9-209a997e7b39",
          "name": "AccidentStats_Get",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.tfl.gov.uk",
              "path": [
                "AccidentStats/:year"
              ],
              "variable": [
                {
                  "id": "year",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Gets all accident details for accidents occuring in the specified year."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "19e6b899-4f47-4f44-b4f4-de64ca057012"
            }
          ]
        }
      ]
    }
  ]
}