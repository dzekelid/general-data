{
  "info": {
    "name": "EPA Air Facility System (AFS) API ",
    "_postman_id": "9a890c47-f37b-4b6e-acff-196fb561970e",
    "description": "",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "id": "77c47772-b982-4903-9920-5e45ff4cb915",
      "name": "enviroFacts_EFFRS_AFSACT1",
      "request": {
        "url": {
          "protocol": "http",
          "host": "iaspub.epa.gov",
          "path": [
            "enviro",
            "efservice",
            "EFFRS_AFSACT1/ROWS/:row_start::row_end/:output"
          ],
          "variable": [
            {
              "id": "output",
              "value": "{}",
              "type": "string"
            },
            {
              "id": "row_end",
              "value": "{}",
              "type": "string"
            },
            {
              "id": "row_start",
              "value": "{}",
              "type": "string"
            }
          ]
        },
        "method": "GET",
        "body": {
          "mode": "raw"
        },
        "description": ""
      },
      "response": [
        {
          "status": "OK",
          "code": 200,
          "name": "Response_200",
          "id": "839deaaa-7f4a-4927-9bc5-d49eece2eaa0"
        }
      ]
    }
  ]
}