{
  "info": {
    "name": "National Crime Victimization Survey (NCVS) API Get Household Year",
    "_postman_id": "0c5de844-9da1-4df6-b9b4-a0c3165df686",
    "description": "Returns the household counts of reported incidents",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Folder",
      "item": [
        {
          "id": "6147a65b-6476-48b6-b04d-1d02f1f4ed73",
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
              "id": "2f8f5f0f-81e5-4892-adf4-19b571412f54"
            }
          ]
        }
      ]
    },
    {
      "name": "Household",
      "item": [
        {
          "id": "42c1def7-8174-4733-898f-593d8fa629a2",
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
              "id": "321967c1-e1aa-4ae4-9e11-f6b0d22804e0"
            }
          ]
        },
        {
          "id": "7c201f2d-e2e5-4a1c-9850-3624220960c3",
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
              "id": "501717fe-bd16-430e-9b7a-bf46033b679b"
            }
          ]
        },
        {
          "id": "bcb8f4e4-177c-4ed4-9244-0102a1c48c40",
          "name": "getV2HouseholdYear",
          "request": {
            "url": {
              "protocol": "http",
              "host": "www.bjs.gov",
              "path": [
                "bjs",
                "ncvs",
                "v2/household/:year"
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
            "description": "Returns the household counts of reported incidents"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "88e89b3c-8d9d-4a81-9d11-d2865580176f"
            }
          ]
        }
      ]
    }
  ]
}