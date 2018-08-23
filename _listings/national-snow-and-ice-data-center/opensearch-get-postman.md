{
  "info": {
    "name": "NSIDC Web Service Documentation Index Search documents using the OpenSearch 1.1 Specification",
    "_postman_id": "fefdb1d4-38d8-4dcd-9184-abb7efe79a55",
    "description": "This endpoint uses parameters from the OpenSearch 1.1 specification, as well as parameters from the OpenSearch Geo (1.0) and SRU (1.0) extensions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Environment",
      "item": [
        {
          "id": "f3b68919-2d55-460d-8cd0-f54c2398dbfa",
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
              "id": "451c7058-936f-4771-8017-e8f9a12388a5"
            }
          ]
        },
        {
          "id": "2768b3ea-5d02-48c1-b5a6-13885963ac9f",
          "name": "OpenSearch.get",
          "request": {
            "url": "http://nsidc.org/api/dataset/2/OpenSearch?count=%7B%7D&endDate=%7B%7D&facetFilters=%7B%7D&searchTerms=%7B%7D&sortKeys=%7B%7D&source=%7B%7D&spatial=%7B%7D&startDate=%7B%7D&startIndex=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This endpoint uses parameters from the OpenSearch 1.1 specification, as well as parameters from the OpenSearch Geo (1.0) and SRU (1.0) extensions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0b6c6b5b-fece-406a-af2e-0f8f6136e694"
            }
          ]
        }
      ]
    }
  ]
}