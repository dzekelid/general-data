{
  "info": {
    "name": "My News Desk Pressroom List Lists news",
    "_postman_id": "f2b7a5a1-4c1e-4e6b-a5f1-0e25c544c19e",
    "description": "Lists news",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "News",
      "item": [
        {
          "id": "64b84d0a-6e55-4683-862d-ee659c5d82f3",
          "name": "getList",
          "request": {
            "url": "http://www.mynewsdesk.com/services/pressroom/list/?archived=%7B%7D&callback=%7B%7D&format=%7B%7D&limit=%7B%7D&offset=%7B%7D&order=%7B%7D&pressroom=%7B%7D&type_of_media=%7B%7D&unique key=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists news"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5186146c-1ed1-4582-a129-cc4e71679b27"
            }
          ]
        }
      ]
    }
  ]
}