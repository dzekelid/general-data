{
  "info": {
    "name": "National Crime Victimization Survey (NCVS) API Get Household Population Year",
    "_postman_id": "af7ee4b9-5110-49ac-a4ef-e88c4c829af5",
    "description": "Returns the personal population of reported incidents.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Folder",
      "item": [
        {
          "id": "a9cc28f5-ecca-483c-8a04-6078a32e570b",
          "name": "getV2",
          "request": {
            "url": "http://www.bjs.gov/bjs/ncvs/v2/",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of available datasets and data types they are available in."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ccf12d8a-8b1d-4a1f-819a-f98a93e0a44c"
            }
          ]
        }
      ]
    },
    {
      "name": "Household",
      "item": [
        {
          "id": "c10a1db7-4bec-4299-87ac-6ba78b46e046",
          "name": "getV2HouseholdFields",
          "request": {
            "url": "http://www.bjs.gov/bjs/ncvs/v2/household/fields/",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a description of the fields/columns used returned in the household data sets."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6cbf7760-7b6d-428a-b419-c124b4a26c5d"
            }
          ]
        },
        {
          "id": "c61a10db-4044-4cd3-8646-a79be5326a8e",
          "name": "getV2HouseholdPopulationYear",
          "request": {
            "url": {
              "protocol": "http",
              "host": "www.bjs.gov",
              "path": [
                "bjs",
                "ncvs",
                "v2/household/population/:year"
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
              "id": "2a15e2b3-a9a4-4600-a15f-23d2c4b4f326"
            }
          ]
        }
      ]
    }
  ]
}