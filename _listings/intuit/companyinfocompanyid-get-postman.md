{
  "info": {
    "name": "QuickBooks Online V3 API Get Company",
    "_postman_id": "3eb84a6b-6349-42ff-8aa7-ce7c29a77fa3",
    "description": "Method : GET",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Accounting",
      "item": [
        {
          "id": "80940a61-c055-4440-8b71-a8015dbb9b87",
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
              "id": "c19e3086-01dc-48ce-b8ce-f06208c1bc97"
            }
          ]
        },
        {
          "id": "a18c205a-4262-4cb2-aaeb-13bd053bea93",
          "name": "getCompanyinfoCompany",
          "request": {
            "url": {
              "protocol": "http",
              "host": "defaultparametervalue",
              "path": [
                "v3",
                "company",
                "DefaultParameterValue",
                "companyinfo/:companyid"
              ],
              "query": [
                {
                  "key": "minorversion",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "companyid",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
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
            "description": "Method : GET"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "02e80820-49d7-492e-abd9-3966c8f25137"
            }
          ]
        }
      ]
    }
  ]
}