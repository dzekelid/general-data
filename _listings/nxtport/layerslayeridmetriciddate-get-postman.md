{
  "info": {
    "name": "NxtPort Bel Air API Retrieve the city layer data for the specified layer, metric and date.",
    "_postman_id": "459f2aee-b258-4852-a06c-801e6c9f9d29",
    "description": "This operation retrieves city layer data for the specified layer, metric and date combination. The date is passed in the following format: YYYYMMDD. The values for the layerId and metricId can be fetched from the /layers and /metrics operations.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Layers",
      "item": [
        {
          "id": "701e4662-901f-4dfd-89cf-400f44d7ddb3",
          "name": "getLayerDateByLayerMetricDate",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api-stg.nxtport.eu",
              "path": [
                "belair",
                "v1",
                "layers/:layerId/:metricId/:date"
              ],
              "variable": [
                {
                  "id": "date",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "layerId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "metricId",
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
            "description": "This operation retrieves city layer data for the specified layer, metric and date combination. The date is passed in the following format: YYYYMMDD. The values for the layerId and metricId can be fetched from the /layers and /metrics operations."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d34e04a6-e743-4340-b8e2-aa5c446a19b7"
            }
          ]
        }
      ]
    }
  ]
}