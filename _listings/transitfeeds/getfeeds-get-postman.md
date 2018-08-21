{
  "info": {
    "name": "TransitFeeds Retrieve a list of feeds.",
    "_postman_id": "ee800246-373b-44b1-a84a-29040b64f09a",
    "description": "Used this API to retrieve a list of feeds in the system. Doing so can be usedful to discover feed IDs that\ncan be used in other API calls.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Retrieve",
      "item": [
        {
          "id": "fbb2b46a-7f16-4de3-a378-82f536af1fae",
          "name": "getFeeds",
          "request": {
            "url": "http://api.transitfeeds.com/v1/getFeeds?descendants=%7B%7D&key=%7B%7D&limit=%7B%7D&location=%7B%7D&page=%7B%7D&type=%7B%7D",
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
            "description": "Used this API to retrieve a list of feeds in the system. Doing so can be usedful to discover feed IDs that\ncan be used in other API calls."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5af5ea44-d415-48c3-8667-c591c9ae3b9c"
            }
          ]
        }
      ]
    }
  ]
}