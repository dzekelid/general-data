---
swagger: "2.0"
x-collection-name: Knoema
x-complete: 0
info:
  title: Knoema API Search by keyword
  description: This namespace provides search details for data accessible by that
    user.
  version: 1.0.0
host: knoema.com
basePath: /api/1.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /search:
    get:
      summary: Search by keyword
      description: This namespace provides search details for data accessible by that
        user.
      operationId: search
      x-api-path-slug: search-get
      parameters:
      - in: query
        name: correct
        description: correct (default true) - correct mistakes in the query or not
        type: string
        format: string
      - in: query
        name: count
        description: count (default 100) - number results count [0
        type: string
        format: string
      - in: query
        name: query
        description: search query for which data is required
        type: string
        format: string
      - in: query
        name: scope
        description: String to specify the type of search results
        type: string
        format: string
      - in: query
        name: start
        description: start (default 0) - number of the first result [0
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Datasets
      - Search
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