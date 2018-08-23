---
swagger: "2.0"
x-collection-name: Meetup
x-complete: 0
info:
  title: Meetup Venues
  description: Search for Meetup venues by one of your groups, events, or venue identifiers.
    For a full text search on public venues use [OpenVenues](/meetup_api/docs/2/open_venues).
  version: 1.0.0
host: api.meetup.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /activity:
    get:
      summary: ActivityFeed
      description: API method for retrieving the activity feed for a member's groups
      operationId: feeds
      x-api-path-slug: activity-get
      parameters:
      - in: query
        name: member_id
        description: Returns activity from this members groups
        type: string
      - in: query
        name: page_start
        description: Starting timestamp for item to return
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Activity
      - Feeds
  /2/venues:
    get:
      summary: Venues
      description: Search for Meetup venues by one of your groups, events, or venue
        identifiers. For a full text search on public venues use [OpenVenues](/meetup_api/docs/2/open_venues).
      operationId: venues
      x-api-path-slug: 2venues-get
      parameters:
      - in: query
        name: event_id
        description: multiple ids may be separated with commas
        type: string
      - in: query
        name: fields
        description: Request that additional fields (separated by commas) be included
          in the output
        type: string
      - in: query
        name: group_id
        description: multiple ids may be separated with commas
        type: string
      - in: query
        name: group_urlname
        description: path to group from meetup
        type: string
      - in: query
        name: venue_id
        description: multiple ids may be separated with commas
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
      - Venues
x-streamrank:
  polling_total_time_average: "0.12"
  polling_size_download_average: "4810.15"
  streaming_total_time_average: "0.07"
  streaming_size_download_average: "2411.43"
  change_yes: "25"
  change_no: "2256"
  time_percentage: "41"
  size_percentage: "50"
  change_percentage: "1"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---