---
swagger: "2.0"
x-collection-name: IEX
x-complete: 0
info:
  title: IEX Trading API Historical Summary
  description: See our stats page for a reference of the keys.
  termsOfService: https://iextrading.com/api-terms/
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
host: api.iextrading.com
basePath: /1.0
paths:
  /stats/historical:
    get:
      summary: Historical Summary
      description: See our stats page for a reference of the keys.
      operationId: historical-summary
      x-api-path-slug: statshistorical-get
      parameters:
      - in: query
        name: date
        description: Parameter is optional Value needs to be in four-digit year, two-digit
          month format (YYYYMM) (i
      - in: query
        name: format
        description: Parameter is optional Value can only be csv When parameter is
          not present, format defaults to JSON
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Historical
x-streamrank:
  polling_total_time_average: "0.16"
  polling_size_download_average: "1482"
  streaming_total_time_average: "0.09"
  streaming_size_download_average: "741"
  change_yes: "1"
  change_no: "1799"
  time_percentage: "41"
  size_percentage: "50"
  change_percentage: "0"
  last_run: "2018-02-20"
  days_run: "1"
  minute_run: "0"
---