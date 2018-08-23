---
swagger: "2.0"
x-collection-name: RingCentral
x-complete: 1
info:
  title: RingCentral Connect Platform API Explorer
  description: this-is-an-interactive-api-explorer-for-the-ringcentral-connect-platform--to-use-this-service-you-will-need-to-have-a-developer-account---links--a-hrefhttpsnetstorage-ringcentral-comdpwapiexplorerrcplatform-basic-ymlv20180514092722-target-blankringcentral-api-specaspannbspnbspopenapi-fka-swagger-formatnbspnbspnbspnbspspana-hrefhttpsgithub-comoaiopenapispecification-target-blanklearn-more-about-openapia
  version: 1.0.0
host: platform.ringcentral.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /restapi/v1.0/glip/companies/{companyId}:
    get:
      summary: Get Company Info
      description: |-
        Returns a company by ID.
        App Permission
        Glip
        User Permission
        Glip
        Usage Plan Group
        Light
      operationId: loadGlipCompany
      x-api-path-slug: restapiv1-0glipcompaniescompanyid-get
      parameters:
      - in: path
        name: companyId
        description: Internal identifier of an RC account/Glip company, or tilde (~)
          to indicate a company the current user belongs to
      responses:
        200:
          description: OK
      tags:
      - Company
      - Info
---