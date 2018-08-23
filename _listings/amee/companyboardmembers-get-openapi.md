---
swagger: "2.0"
x-collection-name: AMEE
x-complete: 0
info:
  title: AMEE Company API Get Company Board Members
  version: "1.0"
  description: Get company board members.
host: api.roaring.io
basePath: /company/1.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /company-board-members:
    get:
      summary: Get Company Board Members
      description: Get company board members.
      operationId: getCompanyBoardMembers
      x-api-path-slug: companyboardmembers-get
      parameters:
      - in: query
        name: companyId
        description: Company identification for the company
      - in: query
        name: countryCode
        description: Country code for the company
      responses:
        200:
          description: OK
      tags:
      - Company
      - Board
      - Members
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