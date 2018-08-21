---
swagger: "2.0"
x-collection-name: Transport for London Unified
x-complete: 0
info:
  title: Transport for London Unified Road s  Status
  description: Gets the specified roads with the status aggregated over the date range
    specified, or now until the end of today if no dates are passed..
  version: v1
host: api.tfl.gov.uk
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /AccidentStats/{year}:
    get:
      summary: Accent Stats year
      description: Gets all accident details for accidents occuring in the specified
        year.
      operationId: AccidentStats_Get
      x-api-path-slug: accidentstatsyear-get
      parameters:
      - in: path
        name: year
        description: The year for which to filter the accidents on
      responses:
        200:
          description: OK
      tags:
      - Accent
      - Stats
      - Year
  /Road/{ids}/Status:
    get:
      summary: Road s  Status
      description: Gets the specified roads with the status aggregated over the date
        range specified, or now until the end of today if no dates are passed..
      operationId: Road_Status
      x-api-path-slug: roadidsstatus-get
      parameters:
      - in: query
        name: dateRangeNullable.endDate
      - in: query
        name: dateRangeNullable.startDate
      - in: path
        name: ids
        description: Comma-separated list of road identifiers e
      responses:
        200:
          description: OK
      tags:
      - Road
      - S
      - ""
      - Status
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