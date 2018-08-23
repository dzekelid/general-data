{
  "info": {
    "name": "Data.gov API Get Metrics",
    "_postman_id": "367c56ba-06a2-42e9-bae3-b5e7d0250eb9",
    "description": "Fetch metrics for an object given its ID",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "metrics",
      "item": [
        {
          "id": "80c22caf-0a6e-4e2b-baf9-efc406e66db0",
          "name": "getMetrics",
          "request": {
            "url": {
              "protocol": "http",
              "host": "catalog.data.gov",
              "path": [
                "api",
                "3",
                "metrics/:id"
              ],
              "query": [
                {
                  "key": "cumulative",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "day",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "end",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "start",
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
            "body": {
              "mode": "raw"
            },
            "description": "Fetch metrics for an object given its ID"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f67c7f75-f843-4500-848d-98adbf1fad44"
            }
          ]
        }
      ]
    }
  ]
}