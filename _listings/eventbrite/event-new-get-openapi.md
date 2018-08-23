---
swagger: "2.0"
x-collection-name: Eventbrite
x-complete: 0
info:
  title: Eventbrite Get Event New
  description: This method creates a new event. It returns the ID of the newly created
    event.
  version: 1.0.0
host: www.eventbrite.com
basePath: /%7Bdata-type%7D/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /event_search:
    get:
      summary: Get Event Search
      description: This method uses our search index to find publicly listed events.
      operationId: Get_event_search_
      x-api-path-slug: event-search-get
      parameters:
      - in: query
        name: address
        description: The venue address
      - in: query
        name: category
        description: 'Event categories (comma seperated): conference, conventions,
          entertainment, fundraisers, meetings, other, performances, reunions, sales,
          seminars, social, sports, tradeshows, travel, religion, fairs, food, music,
          recreation'
      - in: query
        name: city
        description: The venue city
      - in: query
        name: country
        description: 2-letter country code, according to the ISO 3166 format
      - in: query
        name: count_only
        description: Only return the total number of events (???true??? or ???false???)
      - in: query
        name: data-type
        description: xml or json data-types are supported
      - in: query
        name: date
        description: The event start date
      - in: query
        name: date_created
        description: The date range the event was created, specified by a label or
          by exact dates
      - in: query
        name: date_modified
        description: The date range the event was modified, specified by a label or
          by exact dates
      - in: query
        name: keywords
        description: The search keywords
      - in: query
        name: latitude
        description: If ???within??? is set you can limit your search to wgs84 coordinates
          (latitude, longitude)
      - in: query
        name: longitude
        description: If ???within??? is set you can limit your search to wgs84 coordinates
          (latitude, longitude)
      - in: query
        name: max
        description: Limit the number of events returned
      - in: query
        name: organizer
        description: The organizer name
      - in: query
        name: page
        description: Allows for paging through the results of a query
      - in: query
        name: postal_code
        description: The postal/zip code of the venue
      - in: query
        name: region
        description: The venue state/province/county/territory depending on the country
      - in: query
        name: since_id
        description: Returns events with id greater than ???since_id??? value
      - in: query
        name: sort_by
        description: Sort the list of events by ???id???, ???date???, ???name???,
          ???city???
      - in: query
        name: tracking_link
        description: The tracking link code to add to the event URLs
      - in: query
        name: within
        description: If ???within??? is set and the ???city??? or ???zipcode??? resolve
          to a specific geolocation, the search will be restricted to the specified
          within radius
      - in: query
        name: within_unit
        description: 'If within is set, you can specify the unit to use: ???M??? for
          miles, or ???K??? for kilometers'
      responses:
        200:
          description: OK
      tags:
      - Event
      - Search
  /event_new:
    get:
      summary: Get Event New
      description: This method creates a new event. It returns the ID of the newly
        created event.
      operationId: Get_event_new_
      x-api-path-slug: event-new-get
      parameters:
      - in: query
        name: background_color
        description: Custom hexadecimal color for your registration page
      - in: query
        name: box_background_color
        description: Custom hexadecimal color for your registration page
      - in: query
        name: box_border_color
        description: Custom hexadecimal color for your registration page
      - in: query
        name: box_header_background_color
        description: Custom hexadecimal color for your registration page
      - in: query
        name: box_header_text_color
        description: Custom hexadecimal color for your registration page
      - in: query
        name: box_text_color
        description: Custom hexadecimal color for your registration page
      - in: query
        name: capacity
        description: The maximum number of people who can attend the event
      - in: query
        name: currency
        description: The event currency in ISO 4217 format (e
      - in: query
        name: custom_footer
        description: Custom HTML footer for your registration page
      - in: query
        name: custom_header
        description: Custom HTML header for your registration page
      - in: query
        name: data-type
        description: xml or json data-types are supported
      - in: query
        name: description
        description: The event description
      - in: query
        name: end_date
        description: The event end date and time, in ISO 8601 format (e
      - in: query
        name: organizer_id
        description: The event organizer ID
      - in: query
        name: personalized_url
        description: The event registration URL
      - in: query
        name: privacy
        description: 0 for a private event, 1 for a public event
      - in: query
        name: start_date
        description: The event start date and time, in ISO 8601 format (e
      - in: query
        name: status
        description: The event status
      - in: query
        name: text_color
        description: Custom hexadecimal color for your registration page
      - in: query
        name: timezone
        description: The event time zone in relation to GMT (e
      - in: query
        name: title
        description: The event title
      - in: query
        name: title_text_color
        description: Custom hexadecimal color for your registration page
      - in: query
        name: venue_id
        description: The event venue ID
      responses:
        200:
          description: OK
      tags:
      - Event
      - New
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