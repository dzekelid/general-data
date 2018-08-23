{
  "info": {
    "name": "Geneea Natural Language Processing Get Entities",
    "_postman_id": "5b95555a-200d-4565-b283-e9e7837f8149",
    "description": "Performs named-entity recognition on the given document.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Entities",
      "item": [
        {
          "id": "b9449ec5-407f-4796-9a83-016b7937a60a",
          "name": "getS1Entities",
          "request": {
            "url": "http://api.geneea.com/s1/entities?extractor=%7B%7D&language=%7B%7D&returnTextInfo=%7B%7D&text=%7B%7D&url=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Performs named-entity recognition on the given document."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a0af0c32-f964-479e-bbaf-1132b47c726b"
            }
          ]
        }
      ]
    }
  ]
}