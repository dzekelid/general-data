{
  "info": {
    "name": "QuickBooks Online V3 API Get Exchangerate",
    "_postman_id": "0b0a8f0b-1d91-40c6-b237-27bb43e1b4cd",
    "description": "Get ExchangeRate\nMethod : GET",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Accounting",
      "item": [
        {
          "id": "979919f8-2a22-4d97-9aeb-59de3da4a64e",
          "name": "getExchangerate",
          "request": {
            "url": "http://DefaultParameterValue/v3/company/DefaultParameterValue/exchangerate?asofdate=%7B%7D&minorversion=%7B%7D&sourcecurrencycode=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Content-Type",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "User-Agent",
                "value": "{}",
                "description": "",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get ExchangeRate\nMethod : GET"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6c0d431f-c7cc-4b2b-a391-d6260e95c76c"
            }
          ]
        }
      ]
    }
  ]
}