swagger: "2.0"
x-collection-name: US Digital Registry
x-complete: 1
info:
  title: U.S. Digital Registry Tag API
  description: provides-a-access-to-the-list-of-tags-applied-to-federal-government-agencies-and-their-social-media-accounts-
  version: 1.0.0
host: usdigitalregistry.digitalgov.gov
basePath: /api/v1/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /social_media/verify.json:
    get:
      summary: Social Media Verify
      description: This returns an agency based on an URL. If not found, it will return
        a 404
      operationId: Api::V1::SocialMedia#verify
      x-api-path-slug: social-mediaverify-json-get
      parameters:
      - in: query
        name: url
        description: URL of social media account
      responses:
        200:
          description: OK
      tags:
      - Social Media