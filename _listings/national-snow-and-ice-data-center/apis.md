---
name: National Snow and Ice Data Center
x-slug: national-snow-and-ice-data-center
description: NSIDC manages and distributes scientific data, creates tools for data
  access, supports data users, performs scientific research, and educates the public
  about the cryosphere.
image: ""
x-kinRank: "7"
x-alexaRank: "0"
tags: General Data
created: "2018-08-27"
modified: "2018-08-27"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/national-snow-and-ice-data-center/apis.md
specificationVersion: "0.14"
apis:
- name: NSIDC Web Service Documentation Index - View the facet information corresponding
    to a search
  x-api-slug: facets-get
  description: In the NSIDC Search and Arctic Data Explorer interfaces, this endpoint
    is used in conjunction with /OpenSearch whenever a user submits a new search.
    Consequently, it has the same parameters as /OpenSearch.
  image: ""
  humanURL: http://nsidc.org
  baseURL: https://nsidc.org//api/dataset/2
  tags: API Provider, Environment, Sensors, Weather, Water, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/national-snow-and-ice-data-center/facets-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/national-snow-and-ice-data-center/facets-get-openapi.md
- name: NSIDC Web Service Documentation Index - Search documents using the OpenSearch
    1.1 Specification
  x-api-slug: opensearch-get
  description: This endpoint uses parameters from the OpenSearch 1.1 specification,
    as well as parameters from the OpenSearch Geo (1.0) and SRU (1.0) extensions.
  image: ""
  humanURL: http://nsidc.org
  baseURL: https://nsidc.org//api/dataset/2
  tags: API Provider, Environment, Sensors, Weather, Water, Profiles, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/national-snow-and-ice-data-center/opensearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/national-snow-and-ice-data-center/opensearch-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://national.renewable.energy.laboratory.api.gallery.streamdata.io
- type: x-api-stack
  url: http://national.snow.and.ice.data.center.stack.network
- type: x-website
  url: http://nsidc.org
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---