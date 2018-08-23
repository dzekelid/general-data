{
  "info": {
    "name": "Attom Data Solutions API Returns POIs based on point.",
    "_postman_id": "3779579f-3fe6-4b27-9dd1-984df9a2d138",
    "description": "This search returns a list of POI in proximity to a latitude/longitude.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Returns",
      "item": [
        {
          "id": "5842663a-1a91-4071-a7bb-f5027b1ba128",
          "name": "getPropertyIdList",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/property/id?geoid=%7B%7D&maxBeds=%7B%7D&minBeds=%7B%7D&orderby=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get a list of property IDs within a specific geography that have a specific number of beds. Use orderby to choose how you want your results sorted."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3f68b43a-b1c3-4b98-8e2b-760d39b32d24"
            }
          ]
        },
        {
          "id": "27fa8a6c-58c0-4b3b-89c0-a5b0842802dc",
          "name": "propertyDetails",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/property/detail?address=%7B%7D&id=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get property details based on its Onboard property ID."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d600639f-659b-4f3d-8727-6d9e7060a0e8"
            }
          ]
        },
        {
          "id": "5765f35b-fb1a-42a6-bad3-56adfba0e745",
          "name": "adressList",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/property/address?address1=%7B%7D&address2=%7B%7D&orderby=%7B%7D&page=%7B%7D&pagesize=%7B%7D&postalcode=%7B%7D&propertytype=%7B%7D&radius=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get a list of properties within a zip code. Use propertytype and order by to narrow down your results."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c18421cf-95bd-4992-a933-868272fb810d"
            }
          ]
        },
        {
          "id": "6adb9d58-1f10-4d25-b10c-5cf3f3f77974",
          "name": "propertySnapshot",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/property/snapshot?cityname=%7B%7D&latitude=%7B%7D&longitude=%7B%7D&maxavmvalue=%7B%7D&maxLotSize1=%7B%7D&maxtaxamt=%7B%7D&minavmvalue=%7B%7D&minLotSize1=%7B%7D&mintaxamt=%7B%7D&orderby=%7B%7D&postalcode=%7B%7D&propertytype=%7B%7D&radius=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get a list of property snapshots within a specific city that are within a desired size range and a specific property type."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b44de001-981d-403a-80ee-781b39f55c92"
            }
          ]
        },
        {
          "id": "9b1ff676-4b2e-4ce3-bcbd-fd6c63fbcc42",
          "name": "propertyBasicProfile",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/property/basicprofile?attomid=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get basic property information and most recent transaction and taxes for a specific attom id."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f887e099-d19e-41fe-91c0-fa33801dd270"
            }
          ]
        },
        {
          "id": "7267adcc-1da0-4d73-85cc-e7a703671087",
          "name": "propertyExpandedProfile",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/property/expandedprofile?address1=%7B%7D&address2=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get a detailed property information and most recent transaction and taxes for a specific address."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "904af782-b1c5-4bc5-ade9-377b3283c131"
            }
          ]
        },
        {
          "id": "78e30ff0-87bc-4289-9dba-590caeb1cef9",
          "name": "getAllEventsDetailAddress",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/allevents/detail?address1=%7B%7D&address2=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "API Security Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get a detail of all the events on a specific property based on its address."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1ea5e9e7-ebd9-4ce0-9e6f-6f8cbe1b39c0"
            }
          ]
        },
        {
          "id": "aad21019-f324-4ac7-936e-28c4c0139a68",
          "name": "propertyDetailsMortage",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/property/detailmortgage?address1=%7B%7D&address2=%7B%7D&id=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get property details mortgage based on its Onboard property ID."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "959f941f-04b9-4580-8b84-33cbb90caa24"
            }
          ]
        },
        {
          "id": "48075231-e9b3-4a1f-9ede-cb67ae3b9592",
          "name": "propertyDetailsOwner",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/property/detailowner?address1=%7B%7D&address2=%7B%7D&id=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get property details owner based on its Onboard property ID."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "54143596-5350-4ca6-8c03-4f64d6a64530"
            }
          ]
        },
        {
          "id": "58e6c980-db3c-4bed-b866-4e06ea0c70f4",
          "name": "propertyDetailsMortgageOwner",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/property/detailmortgageowner?address1=%7B%7D&address2=%7B%7D&id=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get property details mortgageowner based on its Onboard property ID."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "880a55a1-5458-4b3d-a86b-84dd15a34a34"
            }
          ]
        },
        {
          "id": "5997d729-72ec-40fd-9a59-339e541786af",
          "name": "getAssessmentSnapshotTotal",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/assessment/snapshot?address1=%7B%7D&address2=%7B%7D&maxmktttlvalue=%7B%7D&minmktttlvalue=%7B%7D&radius=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get snapshots of the properties within a radius of a property that have a total market value within a specified range."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6c87cb15-af14-4308-a9f0-2e026eb97022"
            }
          ]
        },
        {
          "id": "5e587fa0-38a0-441a-b04c-583461fef479",
          "name": "assessmenDetailPropertyId",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/assessment/detail?postalcode=%7B%7D&propertytype=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get assessment details for properties within a zip code. Use propertytpe to select a specific property type for your search."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c7964d94-70a0-4229-b92f-fc657c950788"
            }
          ]
        },
        {
          "id": "4e1ded6b-198b-4925-b718-30659d66e8ae",
          "name": "assessmentHistoryDetailID",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/assessmenthistory/detail?id=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get a full detail of property characteristics and assessment history information for a specific property."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "58a3fcdb-cafd-40c2-8fb6-df46aa65ae30"
            }
          ]
        },
        {
          "id": "97bd17b7-f66a-4a83-abdc-eb2d7bb5ef46",
          "name": "avmSnapshotGeoID",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/avm/snapshot?geoid=%7B%7D&maxavmvalue=%7B%7D&minavmvalue=%7B%7D&propertytype=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get a list of AVM snapshot records that fall within an Onboard GeoID with a specific value range. Use propertytpe to select a specific property type for your search."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2e93019d-5a08-4e42-ae86-884ff0ba4de1"
            }
          ]
        },
        {
          "id": "4ec3c8a5-bae9-4bad-a9dd-7d3645d3eb61",
          "name": "avmDetailPostal",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/avm/detail?address1=%7B%7D&address2=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get AVM details for a specific address."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "727cc08c-81ae-4a59-83cc-ede64a418ff9"
            }
          ]
        },
        {
          "id": "d8adf206-d649-4c47-98ac-df90997175e3",
          "name": "attomAvmDetail",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/attomavm/detail?attomid=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get Attomized AVM and other property details for a specific address."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c5700cb6-97fa-4a44-9419-cb631dcff6e4"
            }
          ]
        },
        {
          "id": "8f842744-a5fe-424c-8433-895367f85141",
          "name": "getHomeSaleSnapshotsGeoId",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/sale/snapshot?address1=%7B%7D&address2=%7B%7D&endsalesearchdate=%7B%7D&geoid=%7B%7D&maxsaleamt=%7B%7D&minsaleamt=%7B%7D&propertytype=%7B%7D&radius=%7B%7D&startsalesearchdate=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get a list of home sale snapshots within a Onboard GeoID that sold within a date range and specified sale amount."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "874dd3fa-cfd8-4a0a-9a8e-9d11ff616232"
            }
          ]
        },
        {
          "id": "560cbcfe-06ac-414c-b4d2-030fcdc91254",
          "name": "getSaleDetailPostal",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/sale/detail?address1=%7B%7D&address2=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get sales information for a specific address."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d8785b19-c5a0-4d4a-a540-8e2279d04822"
            }
          ]
        },
        {
          "id": "ebfc4b3c-4861-40d1-b0ab-2b676cc7ca50",
          "name": "getSaleHistorySnapshotPropertyId",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/saleshistory/snapshot?id=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get a sales history snapshot of a property based on an Onboard property ID."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b390f3f5-7abf-4c20-825c-2a1104c1627b"
            }
          ]
        },
        {
          "id": "4fddf0a0-cef6-4e96-8386-2e6528a135f4",
          "name": "saleHistoryBasicHistory",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/saleshistory/basichistory?address1=%7B%7D&address2=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get the basic transaction and loan history on a property for a specific address."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2c603d1f-8320-4951-9d9c-bb60f06493ee"
            }
          ]
        },
        {
          "id": "3c49a8fc-262f-42a0-9e8b-3535787e3618",
          "name": "saleHistoryExpandedHistory",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/saleshistory/expandedhistory?address1=%7B%7D&address2=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get the detailed transaction, pre-foreclosure and loan history on a property for a specific address."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ff9d9f6b-4c26-4bc5-90ae-a5710d86c9ea"
            }
          ]
        },
        {
          "id": "9854b248-f214-4c23-85bf-c97e7d2b9367",
          "name": "getSaleHistoryDetailAddress",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/saleshistory/detail?address1=%7B%7D&address2=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get a sales history snapshot of a property based on an address."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5f1a1a28-c257-4b69-b9a5-a8884f39827e"
            }
          ]
        },
        {
          "id": "ca00e9d0-fe66-4483-a53a-df32dbfbd7da",
          "name": "getSalesTrendByYear",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/salestrend/snapshot?endmonth=%7B%7D&endyear=%7B%7D&geoid=%7B%7D&interval=%7B%7D&startmonth=%7B%7D&startyear=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get the average sale price, median sale price, and count of sales for the past 2 years in yearly intervals."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2e3cb1e7-b3f8-4988-9975-a794ef0aba6e"
            }
          ]
        },
        {
          "id": "aee6ee5b-9f04-4b37-a31e-618130bb760f",
          "name": "getAreaHierarchyLookup",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/hierarchy/lookup?geoType=%7B%7D&latitude=%7B%7D&longitude=%7B%7D&WKTString=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "This method allows you to pass a latitude and longitude point and geo type to retrieve a list of geographies that point falls within. Required input is a valid WKT (Well Known Text) point."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7192e985-57ec-4989-9a7d-81b4123b23e2"
            }
          ]
        },
        {
          "id": "67237855-9b9e-414c-a1fc-c33b7fa94169",
          "name": "getPOISearchGeography",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/poi/geography?PostalCodeKey=%7B%7D&RecordLimit=%7B%7D&SearchDistance=%7B%7D&Sort=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "ApiKey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "This search returns a list of Points of Interest in proximity to the centroid of a zip code."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a7f24ba4-f66e-46b3-828c-bf38a0553775"
            }
          ]
        },
        {
          "id": "1340137f-9e58-4790-bbd7-19c19c2f722c",
          "name": "getPOISearchPoint",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/poi/point?BusinessCategory=%7B%7D&Point=%7B%7D&RecordLimit=%7B%7D&SearchDistance=%7B%7D&Sort=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "This search returns a list of POI in proximity to a latitude/longitude."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3031355f-10e0-4c03-b698-1bb441bcfad4"
            }
          ]
        }
      ]
    },
    {
      "name": "Return",
      "item": [
        {
          "id": "1767e315-0f8f-4ab9-9a8b-595c18acab81",
          "name": "propertyDetailsWithSchools",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/property/detailwithschools?id=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Search for a property to have the property details returned, along with the schools in the associated attendance zones."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3c4d7275-ec53-4692-999e-20919bfff9d9"
            }
          ]
        },
        {
          "id": "ff6781ce-be5b-46e8-a3dc-f81839795f0d",
          "name": "propertySchoolSnapshot",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/school/snapshot?filetypetext=%7B%7D&latitude=%7B%7D&longitude=%7B%7D&radius=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Search for all schools that are located within a given radius around a given latitude and longitude."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4b28dfec-885f-4865-9cf7-5b4e68193d95"
            }
          ]
        },
        {
          "id": "19a8f535-0bf1-486a-939c-44d0edef8fcb",
          "name": "propertyDetails",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/school/detail?id=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Search by school ID to return all of the available details about a school"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "53cc2d73-9f02-455c-b4ca-a29459c7d758"
            }
          ]
        },
        {
          "id": "8589fcb5-d3c9-4424-b940-a08910a61ac0",
          "name": "propertySchoolDistrictDetail",
          "request": {
            "url": "http://search.onboard-apis.com/communityapi/v2.0.0/school/districtdetail?id=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "accept",
                "value": "{}",
                "description": "application/xml or application/json (default)",
                "disabled": false
              },
              {
                "key": "apikey",
                "value": "{}",
                "description": "Application Key",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Search by district number to return all of the available details about a school district"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "153a3be7-113c-454f-a7d1-87b28760dbf9"
            }
          ]
        }
      ]
    }
  ]
}