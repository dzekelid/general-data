---
swagger: "2.0"
x-collection-name: IEX
x-complete: 1
info:
  title: IEX
  description: the-iex-api-is-a-set-of-services-designed-for-developers-and-engineers--it-can-be-used-to-build-highquality-apps-and-services--were-always-working-to-improve-the-iex-api--please-check-back-for-enhancements-and-improvements-
  termsOfService: https://iextrading.com/api-terms/
  version: 1.0.0
host: api.iextrading.com
basePath: /1.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
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
  /hist:
    get:
      summary: HIST
      description: HIST will provide the output of IEX data products for download
        on a T+1 basis. Data will remain available for the trailing twelve months.
      operationId: hist
      x-api-path-slug: hist-get
      parameters:
      - in: query
        name: date
        description: Parameter is optional Value needs to be in four-digit year, two-digit
          month, two-digit day format (YYYYMMDD) (i
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Historical
---