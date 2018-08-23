---
swagger: "2.0"
x-collection-name: Foursquare
x-complete: 0
info:
  title: Foursquare Post Venues Add
  description: /venues/{VENUE_ID}
  version: 1.0.0
host: api.foursquare.com
basePath: /v2/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /venues/add:
    post:
      summary: Post Venues Add
      description: /venues/{VENUE_ID}
      operationId: venuesvenue-id
      x-api-path-slug: venuesadd-post
      parameters:
      - in: query
        name: address
        description: The address of the venue
      - in: query
        name: city
        description: The city name where this venue is
      - in: query
        name: crossStreet
        description: The nearest intersecting street or streets
      - in: query
        name: description
        description: A freeform description of the venue, up to 300 characters
      - in: query
        name: ignoreDuplicates
        description: A boolean flag telling the server to ignore duplicates and force
          the addition of this venue
      - in: query
        name: ignoreDuplicatesKey
        description: Required if ignoreDuplicates is true
      - in: query
        name: ll
        description: Latitude and longitude of the venue, as accurate as is known
      - in: query
        name: name
        description: The name of the venue
      - in: query
        name: phone
        description: The phone number of the venue
      - in: query
        name: primaryCategoryId
        description: The ID of the category to which you want to assign this venue
      - in: query
        name: state
        description: The nearest state or province to the venue
      - in: query
        name: twitter
        description: The twitter handle of the venue
      - in: query
        name: url
        description: The url of the homepage of the venue
      - in: query
        name: v
        description: All requests now accept a v=YYYYMMDD param, which indicates that
          the client is up to date as of the specified date
      - in: query
        name: zip
        description: The zip or postal code for the venue
      responses:
        200:
          description: OK
      tags:
      - Venues
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