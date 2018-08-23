{
  "info": {
    "name": "School Digger API V1 Returns a SchoolDigger district ranking list",
    "_postman_id": "6ab37a44-367f-465e-a84a-7fcfc0e7ef6d",
    "description": "",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "id": "e98ad8e3-279f-461b-9f6e-48c3ec986e47",
      "name": "Districts_GetAllDistricts",
      "request": {
        "url": "http://api.schooldigger.com/v1/districts?appID=%7B%7D&appKey=%7B%7D&boundaryAddress=%7B%7D&boxLatitudeNW=%7B%7D&boxLatitudeSE=%7B%7D&boxLongitudeNW=%7B%7D&boxLongitudeSE=%7B%7D&city=%7B%7D&distanceMiles=%7B%7D&isInBoundaryOnly=%7B%7D&nearLatitude=%7B%7D&nearLongitude=%7B%7D&page=%7B%7D&perPage=%7B%7D&q=%7B%7D&sortBy=%7B%7D&st=%7B%7D&zip=%7B%7D",
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
        "description": "Search the SchoolDigger database for districts. You may use any combination of criteria as query parameters."
      },
      "response": [
        {
          "status": "OK",
          "code": 200,
          "name": "Response_200",
          "id": "533573c6-0122-400b-ad8f-17a6920c0f14"
        }
      ]
    },
    {
      "id": "f0c51f33-f354-49b3-8ff4-4c57fbff3381",
      "name": "Districts_GetDistrict",
      "request": {
        "url": {
          "protocol": "http",
          "host": "api.schooldigger.com",
          "path": [
            "v1/districts/:id"
          ],
          "query": [
            {
              "key": "appID",
              "value": "%7B%7D",
              "disabled": false
            },
            {
              "key": "appKey",
              "value": "%7B%7D",
              "disabled": false
            }
          ],
          "variable": [
            {
              "id": "id",
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
        "description": "Retrieve a single district record from the SchoolDigger database"
      },
      "response": [
        {
          "status": "OK",
          "code": 200,
          "name": "Response_200",
          "id": "87d1454d-8d76-4de5-93d1-3795abdf8708"
        }
      ]
    },
    {
      "id": "cb3eed01-4290-44e0-abb6-299d41bf2907",
      "name": "v1.rankings.districts.st.get",
      "request": {
        "url": {
          "protocol": "http",
          "host": "api.schooldigger.com",
          "path": [
            "v1/rankings/districts/:st"
          ],
          "query": [
            {
              "key": "appID",
              "value": "%7B%7D",
              "disabled": false
            },
            {
              "key": "appKey",
              "value": "%7B%7D",
              "disabled": false
            },
            {
              "key": "page",
              "value": "%7B%7D",
              "disabled": false
            },
            {
              "key": "perPage",
              "value": "%7B%7D",
              "disabled": false
            },
            {
              "key": "year",
              "value": "%7B%7D",
              "disabled": false
            }
          ],
          "variable": [
            {
              "id": "st",
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
        "description": "Returns a SchoolDigger district ranking list"
      },
      "response": [
        {
          "status": "OK",
          "code": 200,
          "name": "Response_200",
          "id": "f6c87fc3-514f-40eb-ab0f-dc8842ace585"
        }
      ]
    }
  ]
}