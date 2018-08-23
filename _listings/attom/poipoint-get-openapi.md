---
swagger: "2.0"
x-collection-name: ATTOM
x-complete: 0
info:
  title: Attom Data Solutions API Returns POIs based on point.
  version: 1.0.0
  description: This search returns a list of POI in proximity to a latitude/longitude.
host: search.onboard-apis.com
basePath: /communityapi/v2.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /poi/point:
    get:
      summary: Returns POIs based on point.
      description: This search returns a list of POI in proximity to a latitude/longitude.
      operationId: getPOISearchPoint
      x-api-path-slug: poipoint-get
      parameters:
      - in: header
        name: accept
        description: application/xml or application/json (default)
      - in: header
        name: apikey
        description: Application Key
      - in: query
        name: BusinessCategory
        description: This is Business Category as per Lookup separated by pipe |
      - in: query
        name: Point
        description: This is the Point value
      - in: query
        name: RecordLimit
        description: This is RecordLimit
      - in: query
        name: SearchDistance
        description: This is SearchDistance
      - in: query
        name: Sort
        description: This is for Sortable Columns
      responses:
        200:
          description: OK
      tags:
      - Returns
      - POIs
      - Based
      - "On"
      - Point
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