---
swagger: "2.0"
x-collection-name: OrgHunter
x-complete: 0
info:
  title: Org Hunter Get summary data!
  description: This operation provides summary data.
  version: 1.0.0
host: data.orghunter.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/charitysearch:
    post:
      summary: Get summary data!
      description: This operation provides summary data.
      operationId: postV1Charitysearch
      x-api-path-slug: v1charitysearch-post
      parameters:
      - in: query
        name: category
        description: Category Value Selected from Categories API
      - in: query
        name: city
        description: City Name
      - in: query
        name: ein
        description: Employer Identification Number (EIN)
      - in: query
        name: eligible
        description: eligible=1 will return only organizations that are tax deductible
          and in good standing with the IRS
      - in: query
        name: rows
        description: Records Per Page
      - in: query
        name: searchTerm
        description: Charity Name or Keyword
      - in: query
        name: start
        description: Record Set Start Position
      - in: query
        name: state
        description: State Name - Two letter state abbreviation
      - in: query
        name: zipCode
        description: Zipcode Value - 5 digit zipcode value
      responses:
        200:
          description: OK
      tags:
      - Charity
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