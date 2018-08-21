---
swagger: "2.0"
x-collection-name: Oxford Dictionaries
x-complete: 0
info:
  title: Oxford Dictionaries Lists available filters for specific endpoint
  description: Returns a list of all the valid filters for a given endpoint to construct
    API calls.
  termsOfService: http://helloreverb.com/terms/
  version: 1.8.0
host: od-api-demo.oxforddictionaries.com:443
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /filters/{endpoint}:
    get:
      summary: Lists available filters for specific endpoint
      description: Returns a list of all the valid filters for a given endpoint to
        construct API calls.
      operationId: getFiltersEndpoint
      x-api-path-slug: filtersendpoint-get
      parameters:
      - in: path
        name: endpoint
        description: Name of the endpoint
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Filters
      - Endpoint
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---