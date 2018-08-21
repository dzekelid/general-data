---
swagger: "2.0"
x-collection-name: Intrinio
x-complete: 0
info:
  title: Intrinio API Securities
  description: Returns security list and information for all securities covered by
    Intrinio.
  version: 1.0.0
host: api.intrinio.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /companies:
    get:
      summary: Company Master
      description: Returns the master list of all companies covered by the Intrinio
        Data Marketplace.  You can view the Company/Security Master here.
      operationId: company-master
      x-api-path-slug: companies-get
      parameters:
      - in: query
        name: latest_filing_date
        description: 'a date value that returns the list of companies whose latest
          SEC filing was filed on or after this date: YYYY'
        type: string
      - in: query
        name: page_number
        description: an integer greater than or equal to 1 for specifying the page
          number for the return values
        type: string
      - in: query
        name: page_size
        description: an integer greater than 1 for specifying the number of results
          on each page
        type: string
      - in: query
        name: query
        description: a string query search of company name or ticker symbol with the
          returned results being the relevant companies in compacted list format
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Companies
  /securities:
    get:
      summary: Securities
      description: Returns security list and information for all securities covered
        by Intrinio.
      operationId: securities
      x-api-path-slug: securities-get
      parameters:
      - in: query
        name: exch_symbol
        description: 'the Intrinio Stock Market Symbol, to specify the exchange for
          the list of securities:'
        type: string
      - in: query
        name: identifier
        description: 'the identifier for the legal entity or a security associated
          with the company:'
        type: string
      - in: query
        name: last_crsp_adj_date
        description: 'a date value that returns the list of securities that have had
          adjusted stock prices due to a corporate event after this date: YYYY'
        type: string
      - in: query
        name: page_number
        description: an integer greater than or equal to 1 for specifying the page
          number for the return values
        type: string
      - in: query
        name: page_size
        description: an integer greater than 1 for specifying the number of results
          on each page
        type: string
      - in: query
        name: query
        description: a string query search of security name or ticker symbol with
          the returned results being the relevant securities in compacted list format
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Securities
x-streamrank:
  polling_total_time_average: "0.94"
  polling_size_download_average: "29095.58"
  streaming_total_time_average: "0.5"
  streaming_size_download_average: "14559.58"
  change_yes: "19"
  change_no: "3726"
  time_percentage: "47"
  size_percentage: "50"
  change_percentage: "1"
  last_run: "2018-02-19"
  days_run: "3"
  minute_run: "0"
---