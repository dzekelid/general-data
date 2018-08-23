{
  "info": {
    "name": "RingCentral Get Company Info",
    "_postman_id": "4a5fe5f3-79ce-438f-8c54-3488d7fbb395",
    "description": "Returns a company by ID.\nApp Permission\nGlip\nUser Permission\nGlip\nUsage Plan Group\nLight",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Company",
      "item": [
        {
          "id": "05a91dfd-4978-4834-8459-0a792735f946",
          "name": "loadGlipCompany",
          "request": {
            "url": {
              "protocol": "http",
              "host": "platform.ringcentral.com",
              "path": [
                "restapi/v1.0/glip/companies/:companyId"
              ],
              "variable": [
                {
                  "id": "companyId",
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
            "description": "Returns a company by ID.\nApp Permission\nGlip\nUser Permission\nGlip\nUsage Plan Group\nLight"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ed262f4c-8393-47ea-9d0e-b641fa637135"
            }
          ]
        }
      ]
    }
  ]
}