---
swagger: "2.0"
x-collection-name: Geneea
x-complete: 0
info:
  title: Geneea Natural Language Processing Get Entities
  description: Performs named-entity recognition on the given document.
  version: "1.0"
host: api.geneea.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /s1/entities:
    get:
      summary: Get Entities
      description: Performs named-entity recognition on the given document.
      operationId: getS1Entities
      x-api-path-slug: s1entities-get
      parameters:
      - in: query
        name: extractor
        description: document extractor
      - in: query
        name: language
        description: document language
      - in: query
        name: returnTextInfo
      - in: query
        name: text
        description: raw document text
      - in: query
        name: url
        description: document URL
      responses:
        200:
          description: OK
      tags:
      - Entities
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