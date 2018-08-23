---
swagger: "2.0"
x-collection-name: Intuit
x-complete: 0
info:
  title: QuickBooks Online V3 API Get Company
  description: 'Method : GET'
  version: 1.0.0
host: DefaultParameterValue
basePath: /v3/company/DefaultParameterValue
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /exchangerate:
    get:
      summary: Get Exchangerate
      description: |-
        Get ExchangeRate
        Method : GET
      operationId: getExchangerate
      x-api-path-slug: exchangerate-get
      parameters:
      - in: header
        name: Accept
      - in: query
        name: asofdate
      - in: header
        name: Content-Type
      - in: query
        name: minorversion
      - in: query
        name: sourcecurrencycode
      - in: header
        name: User-Agent
      responses:
        200:
          description: OK
      tags:
      - Accounting
      - Accounting
      - Exchangerate
  /companyinfo/{companyid}:
    get:
      summary: Get Company
      description: 'Method : GET'
      operationId: getCompanyinfoCompany
      x-api-path-slug: companyinfocompanyid-get
      parameters:
      - in: header
        name: Accept
      - in: path
        name: companyid
      - in: header
        name: Content-Type
      - in: query
        name: minorversion
      - in: header
        name: User-Agent
      responses:
        200:
          description: OK
      tags:
      - Accounting
      - Accounting
      - Company
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