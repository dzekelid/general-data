---
swagger: "2.0"
x-collection-name: Data.Gov
x-complete: 0
info:
  title: Data.gov API Get Metrics
  description: Fetch metrics for an object given its ID
  version: "3"
host: catalog.data.gov
basePath: /api/3/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /metrics/{id}:
    get:
      summary: Get Metrics
      description: Fetch metrics for an object given its ID
      operationId: getMetrics
      x-api-path-slug: metricsid-get
      parameters:
      - in: query
        name: cumulative
        description: Either cumulative metrics or not
      - in: query
        name: day
        description: Specific day date to fetch
      - in: query
        name: end
        description: End of the period to fetch
      - in: path
        name: id
        description: The object ID to fetch metric for
      - in: query
        name: start
        description: Start of the period to fetch
      responses:
        200:
          description: OK
      tags:
      - Metrics
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