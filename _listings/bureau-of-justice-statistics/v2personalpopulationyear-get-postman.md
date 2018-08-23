{
  "info": {
    "name": "National Crime Victimization Survey (NCVS) API Get Personal Population Year",
    "_postman_id": "c379c275-08e5-4b45-9168-37d63dabbd2c",
    "description": "Returns the personal population of reported incidents.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Personal",
      "item": [
        {
          "id": "6edd579a-eb94-4be4-8f67-39b76a7572f9",
          "name": "getV2PersonalFields",
          "request": {
            "url": "http://www.bjs.gov/bjs/ncvs/v2/personal/fields/",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a description of the fields/columns used returned in the personal data sets."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dfe1bfc9-2c92-4d06-80e8-f54932ffb5ff"
            }
          ]
        },
        {
          "id": "ad217cfa-0c2d-4915-bbbb-55837d825419",
          "name": "getV2PersonalPopulationYear",
          "request": {
            "url": {
              "protocol": "http",
              "host": "www.bjs.gov",
              "path": [
                "bjs",
                "ncvs",
                "v2/personal/population/:year"
              ],
              "query": [
                {
                  "key": "format",
                  "value": "%7B%7D",
                  "disabled": false
                }
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
            "body": {
              "mode": "raw"
            },
            "description": "Returns the personal population of reported incidents."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "96f095e0-b721-433d-8ed8-d6c28479ef22"
            }
          ]
        }
      ]
    }
  ]
}