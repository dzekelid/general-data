---
swagger: "2.0"
x-collection-name: Lykke
x-complete: 1
info:
  title: Wallet_Api
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/Ethereum/history/{address}:
    get:
      summary: Get API Ethereum History Address
      description: Get api ethereum history address.
      operationId: ApiEthereumHistoryByAddressGet
      x-api-path-slug: apiethereumhistoryaddress-get
      parameters:
      - in: path
        name: address
      - in: query
        name: assetId
      - in: header
        name: Authorization
        description: access token
      - in: query
        name: count
      - in: query
        name: start
      responses:
        200:
          description: OK
      tags:
      - Ethereum
      - History
      - Ress
---