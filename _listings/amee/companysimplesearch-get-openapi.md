---
swagger: "2.0"
x-collection-name: AMEE
x-complete: 0
info:
  title: AMEE Company API Get Company Simple Search
  description: Get company simple search.
  version: "1.0"
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
  /company-credit-decision:
    get:
      summary: Get Company Credit Decision
      description: Get company credit decision.
      operationId: getCompanyCreditDecision
      x-api-path-slug: companycreditdecision-get
      parameters:
      - in: query
        name: companyId
        description: Company identification for the company
      - in: query
        name: countryCode
        description: Country code for the company
      - in: query
        name: template
        description: Template for credit decision
      responses:
        200:
          description: OK
      tags:
      - Company
      - Credit
      - Decision
  /company-economy-overview:
    get:
      summary: Get Company Economy Overview
      description: Get company economy overview.
      operationId: getCompanyEconomyOverview
      x-api-path-slug: companyeconomyoverview-get
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
      - Economy
      - Overview
  /company-overview:
    get:
      summary: Get Company Overview
      description: Get company overview.
      operationId: getCompanyOverview
      x-api-path-slug: companyoverview-get
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
      - Overview
  /company-signatory:
    get:
      summary: Get Company Signatory
      description: Get company signatory.
      operationId: getCompanySignatory
      x-api-path-slug: companysignatory-get
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
      - Signatory
  /company-simple-search:
    get:
      summary: Get Company Simple Search
      description: Get company simple search.
      operationId: getCompanySimpleSearch
      x-api-path-slug: companysimplesearch-get
      parameters:
      - in: query
        name: companyName
        description: Company name
      - in: query
        name: countryCode
        description: Country code for the company
      - in: query
        name: town
        description: Town
      responses:
        200:
          description: OK
      tags:
      - Company
      - Simple
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