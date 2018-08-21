---
swagger: "2.0"
x-collection-name: Intuit
x-complete: 1
info:
  title: QuickBooks Online V3 API
  description: the-quickbooks-online-accounting-api-is-a-restful-api-that-is-used-to-access-quickbooks-companies-docs-
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
---