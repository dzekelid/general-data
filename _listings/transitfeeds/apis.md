---
name: TransitFeeds
x-slug: transitfeeds
description: The best source of open official public transit data. Maintained by @qzervaas
  + others
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/26209-rta-service-alerts.jpg
x-kinRank: "7"
x-alexaRank: "558301"
tags: General Data
created: "2018-08-27"
modified: "2018-08-27"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/transitfeeds/apis.md
specificationVersion: "0.14"
apis:
- name: TransitFeeds API - Retrieve a list of feeds.
  x-api-slug: getfeeds-get
  description: |-
    Used this API to retrieve a list of feeds in the system. Doing so can be usedful to discover feed IDs that
    can be used in other API calls.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/26209-rta-service-alerts.jpg
  humanURL: https://transitfeeds.com
  baseURL: https://api.transitfeeds.com//v1
  tags: Transit, General Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/transitfeeds/getfeeds-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/transitfeeds/getfeeds-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://transavia.api.gallery.streamdata.io
- type: x-twitter
  url: https://twitter.com/TransitFeeds
- type: x-website
  url: https://transitfeeds.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---