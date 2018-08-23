---
swagger: "2.0"
x-collection-name: GlobalChange.gov
x-complete: 0
info:
  title: Global Change Information System API Get a representation of an organization.
  description: Get JSON which represents the structure of an organization.
  version: v1
host: data.globalchange.gov
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /organization/{organization_identifier}:
    get:
      summary: Get a representation of an organization.
      description: Get JSON which represents the structure of an organization.
      operationId: get-json-which-represents-the-structure-of-an-organization
      x-api-path-slug: organizationorganization-identifier-get
      parameters:
      - in: path
        name: organization_identifier
        description: organization_identifier description
      responses:
        200:
          description: OK
      tags:
      - Representation
      - Organization
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