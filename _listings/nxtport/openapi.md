swagger: "2.0"
x-collection-name: NxtPort
x-complete: 1
info:
  title: Portcall+ API (sandbox)
  description: portplus-api
  version: 1.0.0
host: api-sb.nxtport.eu
basePath: /PortCallPlus/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /layers/{layerId}/{metricId}/{date}:
    get:
      summary: Retrieve the city layer data for the specified layer, metric and date.
      description: 'This operation retrieves city layer data for the specified layer,
        metric and date combination. The date is passed in the following format: YYYYMMDD.
        The values for the layerId and metricId can be fetched from the /layers and
        /metrics operations.'
      operationId: getLayerDateByLayerMetricDate
      x-api-path-slug: layerslayeridmetriciddate-get
      parameters:
      - in: path
        name: date
        description: TODO
      - in: path
        name: layerId
        description: TODO
      - in: path
        name: metricId
        description: TODO
      responses:
        200:
          description: OK
      tags:
      - Layers
      - Metrics