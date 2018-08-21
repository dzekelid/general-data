{
  "info": {
    "name": "NSIDC Web Service Documentation Index View the facet information corresponding to a search",
    "_postman_id": "ae76e337-6fe4-46a4-bb21-6c6a90fe56b3",
    "description": "In the NSIDC Search and Arctic Data Explorer interfaces, this endpoint is used in conjunction with /OpenSearch whenever a user submits a new search. Consequently, it has the same parameters as /OpenSearch.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Environment",
      "item": [
        {
          "id": "bfd7546c-9f8c-4fbf-85e9-ce3923d584b9",
          "name": "facets",
          "request": {
            "url": "http://nsidc.org/api/dataset/2/Facets?count=%7B%7D&endDate=%7B%7D&facetFilters=%7B%7D&searchTerms=%7B%7D&sortKeys=%7B%7D&source=%7B%7D&spatial=%7B%7D&startDate=%7B%7D&startIndex=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "In the NSIDC Search and Arctic Data Explorer interfaces, this endpoint is used in conjunction with /OpenSearch whenever a user submits a new search. Consequently, it has the same parameters as /OpenSearch."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b414bf48-a0d5-44ab-a410-131e6d541a39"
            }
          ]
        }
      ]
    }
  ]
}