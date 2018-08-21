{
  "info": {
    "name": "My News Desk Pressroom List News Search",
    "_postman_id": "60df7b5b-5eb8-4982-89ea-a3d9ab8c1825",
    "description": "News Search",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "News",
      "item": [
        {
          "id": "6931fa4a-d60c-4920-bfe7-65d56e6e0a32",
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
              "id": "1ebe3e08-ed69-46e1-8447-d872f268c595"
            }
          ]
        },
        {
          "id": "bec8ac0f-d1e0-4f3d-8539-f730073abbd9",
          "name": "getPressroomInfo",
          "request": {
            "url": "http://www.mynewsdesk.com/services/pressroom/pressroom_info/?pressroom=%7B%7D&unique key=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Pressroom Info"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "68a5ad93-6386-440a-b65f-13ad667d4eac"
            }
          ]
        },
        {
          "id": "bb8dafb8-49ba-4b29-8a71-63aa65f0bbeb",
          "name": "getSearch",
          "request": {
            "url": "http://www.mynewsdesk.com/services/pressroom/search/?callback=%7B%7D&date_end=%7B%7D&date_mode=%7B%7D&date_on=%7B%7D&date_start=%7B%7D&format=%7B%7D&limit=%7B%7D&page=%7B%7D&pressroom=%7B%7D&query=%7B%7D&type_of_media=%7B%7D&unique key=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "News Search"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fd378fec-8a96-4e87-be29-f996316e0cf9"
            }
          ]
        }
      ]
    }
  ]
}