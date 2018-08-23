{
  "info": {
    "name": "AMEE Company API Get Company Board Members",
    "_postman_id": "c9cf6790-773f-43cf-9228-9fd9ee43c564",
    "description": "Get company board members.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Company",
      "item": [
        {
          "id": "14cfd8d8-1e40-4736-a5c4-f83737ab879f",
          "name": "getCompanyBoardMembers",
          "request": {
            "url": "http://api.roaring.io/company/1.0/company-board-members?companyId=%7B%7D&countryCode=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get company board members."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b55097c2-5987-4e43-aede-94191fb78651"
            }
          ]
        }
      ]
    }
  ]
}