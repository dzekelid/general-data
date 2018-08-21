---
swagger: "2.0"
x-collection-name: RipaEx
x-complete: 1
info:
  title: RIPA Node Documentation
  description: this-is-a-documentation-for-ripanodehttpsgithub-comripaexripanode-built-with-swagger-ui-to-make-testing-a-breeze--if-you-find-any-issues-come-over-to-ripaexripanodetestapihttpsgithub-comripaexripanodetestapi-to-open-an-issue-or-even-better-send-a-pr-that-fixes-the-issue-the-community-ssl-public-api-used-as-test-host-is-provided-from-ripaex-iohttpswww-ripaex-io-
  version: 1.0.0
host: api.ripaex.io
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/transactions:
    get:
      summary: Transactions
      description: Get all transactions.
      operationId: transactions.getTransactions
      x-api-path-slug: apitransactions-get
      parameters:
      - in: query
        name: amount
        description: An unsigned integer that specifies the transaction amount
      - in: query
        name: blockId
        description: An unsigned integer that specifies the block ID
      - in: query
        name: fee
        description: An unsigned integer that specifies the transaction fee
      - in: query
        name: limit
        description: An unsigned integer that specifies the maximum number of records
      - in: query
        name: offset
        description: An unsigned integer that specified the number of records to skip
      - in: query
        name: orderBy
        description: A string that specifies the column by which to sort the records
      - in: query
        name: ownerAddress
        description: A valid RIPA Address
      - in: query
        name: ownerPublicKey
        description: A valid RIPA Address
      - in: query
        name: recipientId
        description: A valid RIPA Address
      - in: query
        name: senderId
        description: A valid RIPA Address
      - in: query
        name: senderPublicKey
        description: A valid RIPA Public Key
      - in: query
        name: type
        description: An unsigned integer that specifies the transaction type
      - in: query
        name: vendorField
        description: A string that specifies the SmartBridge used
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - Transactions
---