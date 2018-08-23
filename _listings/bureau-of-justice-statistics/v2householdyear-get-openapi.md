---
swagger: "2.0"
x-collection-name: Bureau of Justice Statistics
x-complete: 0
info:
  title: National Crime Victimization Survey (NCVS) API Get Household Year
  description: Returns the household counts of reported incidents
  version: v2
host: www.bjs.gov
basePath: /bjs/ncvs/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  v2/personal/{year}:
    get:
      summary: Get Personal Year
      description: Returns the personal counts of reported incidents.
      operationId: getV2PersonalYear
      x-api-path-slug: v2personalyear-get
      parameters:
      - in: query
        name: format
        description: Format the data will be provided in
      - in: query
        name: year
        description: Year will limit the data to only values that occurred the given
          year
      responses:
        200:
          description: OK
      tags:
      - Personal
      - Year
  v2/personal/population/{year}:
    get:
      summary: Get Personal Population Year
      description: Returns the personal population of reported incidents.
      operationId: getV2PersonalPopulationYear
      x-api-path-slug: v2personalpopulationyear-get
      parameters:
      - in: query
        name: format
        description: Format the data will be provided in
      - in: query
        name: year
        description: Year will limit the data to only values that occurred the given
          year
      responses:
        200:
          description: OK
      tags:
      - Personal
      - Population
      - Year
  v2/household/{year}:
    get:
      summary: Get Household Year
      description: Returns the household counts of reported incidents
      operationId: getV2HouseholdYear
      x-api-path-slug: v2householdyear-get
      parameters:
      - in: query
        name: format
        description: Format the data will be provided in
      - in: query
        name: year
        description: Year will limit the data to only values that occurred the given
          year
      responses:
        200:
          description: OK
      tags:
      - Household
      - Year
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