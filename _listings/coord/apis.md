---
name: Coord
x-slug: coord
description: Coord is a mobility company that creates seamless mobility and self-driving
  experiences today through deep integrations. The company offers bike-share API,
  Curbs API, Tolls API, Routing API and etc.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
x-kinRank: "7"
x-alexaRank: "1035226"
tags: General Data
created: "2018-08-22"
modified: "2018-08-22"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/coord/apis.md
specificationVersion: "0.14"
apis:
- name: Coord Bike Share API
  x-api-slug: coord-bike-share-api
  description: Coord is a mobility company that creates seamless mobility and self-driving
    experiences today through deep integrations. The company offers bike-share API,
    Curbs API, Tolls API, Routing API and etc.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
  humanURL: https://coord.co
  baseURL: https://api.coord.co//v1/bike
  tags: General Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/coord/openapi.md
- name: Coord Curb Search API
  x-api-slug: coord-curb-search-api
  description: Coord is a mobility company that creates seamless mobility and self-driving
    experiences today through deep integrations. The company offers bike-share API,
    Curbs API, Tolls API, Routing API and etc.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
  humanURL: https://coord.co
  baseURL: https://api.coord.co//v1/search/curbs
  tags: General Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/coord/openapi.md
- name: Coord Multimodal Routing API
  x-api-slug: coord-multimodal-routing-api
  description: Coord is a mobility company that creates seamless mobility and self-driving
    experiences today through deep integrations. The company offers bike-share API,
    Curbs API, Tolls API, Routing API and etc.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
  humanURL: https://coord.co
  baseURL: https://api.coord.co//v1/routing
  tags: General Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/coord/openapi.md
- name: Coord Parking Access API
  x-api-slug: coord-parking-access-api
  description: Coord is a mobility company that creates seamless mobility and self-driving
    experiences today through deep integrations. The company offers bike-share API,
    Curbs API, Tolls API, Routing API and etc.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
  humanURL: https://coord.co
  baseURL: https://api.coord.co//v1/access/parking
  tags: General Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/coord/openapi.md
- name: Coord Parking Search API
  x-api-slug: coord-parking-search-api
  description: the-parking-search-api-is-a-readonly-service-to-answer-questionsabout-where-and-when-a-person-can-park-in-lots-and-garages--for-onstreet-parkinguse-the-curbs-api-finding-parking-locationsa-place-where-you-can-park-is-called-a-location--this-is-usually-either-a-surface-parkinglot-or-a-parking-garage--to-find-parking-locations-in-a-given-area-use-thelocationreference0getalistoflocations-request--this-will-return-an-object-for-each-open--location-in-that-area-ordered-by-distance-when-we-have-live-parking-availability-for-a-location-we-will-also-fill-inavailability-probability-for-it--this-represents-the-probability-that-there-will-be-at-leastthreshold-spaces-available-at-the-location--we-find-availability-probability-a-prettygreat-way-to-reason-about-parking-locations-which-may-have-uncertainty-around-theiravailability-both-at-the-current-time-and-in-the-future-when-someone-may-be-arriving-aftera-trip-getting-data-on-a-single-locationuse-locationreference0getasinglelocations-requests-to-get-the-same-information-aboutjust-one-location-accessing-a-lotyou-can-allow-your-mobile-users-to-check-into-and-out-of-select-locationsusing-the-parking-access-api--parking-rates-select-locations-will-have-a-rates-field-set-with-a-list-of-rates-which-can-be-displayed-toyour-end-users-for-a-rough-idea-on-the-price-of-parking-all-locations-will-include-a-total-price-if--parking-start-time-and-duration-m-are-setappropriately-
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
  humanURL: https://coord.co
  baseURL: https://api.coord.co//v1/search/parking
  tags: Parking, Tolls, Bikes, Routes, General Data, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/coord/location-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/coord/location-get-openapi.md
- name: Coord Parking Search API
  x-api-slug: coord-parking-search-api
  description: the-parking-search-api-is-a-readonly-service-to-answer-questionsabout-where-and-when-a-person-can-park-in-lots-and-garages--for-onstreet-parkinguse-the-curbs-api-finding-parking-locationsa-place-where-you-can-park-is-called-a-location--this-is-usually-either-a-surface-parkinglot-or-a-parking-garage--to-find-parking-locations-in-a-given-area-use-thelocationreference0getalistoflocations-request--this-will-return-an-object-for-each-open--location-in-that-area-ordered-by-distance-when-we-have-live-parking-availability-for-a-location-we-will-also-fill-inavailability-probability-for-it--this-represents-the-probability-that-there-will-be-at-leastthreshold-spaces-available-at-the-location--we-find-availability-probability-a-prettygreat-way-to-reason-about-parking-locations-which-may-have-uncertainty-around-theiravailability-both-at-the-current-time-and-in-the-future-when-someone-may-be-arriving-aftera-trip-getting-data-on-a-single-locationuse-locationreference0getasinglelocations-requests-to-get-the-same-information-aboutjust-one-location-accessing-a-lotyou-can-allow-your-mobile-users-to-check-into-and-out-of-select-locationsusing-the-parking-access-api--parking-rates-select-locations-will-have-a-rates-field-set-with-a-list-of-rates-which-can-be-displayed-toyour-end-users-for-a-rough-idea-on-the-price-of-parking-all-locations-will-include-a-total-price-if--parking-start-time-and-duration-m-are-setappropriately-
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
  humanURL: https://coord.co
  baseURL: https://api.coord.co//v1/search/parking
  tags: Parking, Tolls, Bikes, Routes, General Data, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/coord/location-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/coord/location-get-openapi.md
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/coord/locationid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/coord/locationid-get-openapi.md
- name: Coord Parking Search API
  x-api-slug: coord-parking-search-api
  description: Coord is a mobility company that creates seamless mobility and self-driving
    experiences today through deep integrations. The company offers bike-share API,
    Curbs API, Tolls API, Routing API and etc.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
  humanURL: https://coord.co
  baseURL: https://api.coord.co//v1/search/parking
  tags: General Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/coord/openapi.md
- name: Coord Tolls API
  x-api-slug: coord-tolls-api
  description: Coord is a mobility company that creates seamless mobility and self-driving
    experiences today through deep integrations. The company offers bike-share API,
    Curbs API, Tolls API, Routing API and etc.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
  humanURL: https://coord.co
  baseURL: https://api.coord.co//v1/search/tolling
  tags: General Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/coord/openapi.md
- name: Coord Users API
  x-api-slug: coord-users-api
  description: Coord is a mobility company that creates seamless mobility and self-driving
    experiences today through deep integrations. The company offers bike-share API,
    Curbs API, Tolls API, Routing API and etc.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/coord-logo.png
  humanURL: https://coord.co
  baseURL: https://api.coord.co//v1/users
  tags: General Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/coord/openapi.md
x-common:
- type: x-blog
  url: https://medium.com/coord
- type: x-blog-rss
  url: https://medium.com/feed/coord
- type: x-openapi
  url: https://jsapi.apiary.io/apis/coordprodsearchtolls.source
- type: x-api-gallery
  url: http://convertapi.api.gallery.streamdata.io
- type: x-api-stack
  url: http://coord.stack.network
- type: x-developer
  url: https://coord.co/docs/
- type: x-pricing
  url: https://coord.co/#pricing
- type: x-twitter
  url: https://twitter.com/coordcity
- type: x-website
  url: https://coord.co
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---