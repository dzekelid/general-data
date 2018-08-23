---
swagger: "2.0"
x-collection-name: Intrinio
x-complete: 0
info:
  title: Intrinio API Company Executive Contacts
  description: Returns a list of all information for an executive and their related
    companies.  Information includes the unique Intrinio executive company identifier,
    and detailed contact information for the executive at a specified company.
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
  /historical_data:
    get:
      summary: Historical Data
      description: Returns the historical data for for a selected identifier (ticker
        symbol or index symbol) for a selected tag.  The complete list of tags available
        through this function are available here.  Income statement, cash flow statement,
        and ratios are returned as trailing twelve months values by default, but can
        be changed with the type parameter.  All other historical data points are
        returned as their value on a certain day based on filings reported as of that
        date.
      operationId: historical-data
      x-api-path-slug: historical-data-get
      parameters:
      - in: query
        name: end_date
        description: 'the latest date for which to return data: YYYY'
        type: string
      - in: query
        name: frequency
        description: 'the frequency of the historical prices &amp; valuation data:
          daily | weekly | monthly | quarterly | yearly'
        type: string
      - in: query
        name: identifier
        description: the stock market ticker symbol associated with the company&rsquo;s
          common stock or index
        type: string
      - in: query
        name: item
        description: the specified standardized tag requested
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
        name: sequence
        description: in function)
        type: string
      - in: query
        name: show_date
        description: 'in, false by default) if true, the function will return the
          date value, and if false the function will return the data point value for
          a given query: true | false'
        type: string
      - in: query
        name: sort_order
        description: 'the order of the historical stock price dates: asc | desc'
        type: string
      - in: query
        name: start_date
        description: 'the earliest date for which to return data: YYYY'
        type: string
      - in: query
        name: type
        description: the type of periods requested
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Historical Data
  /prices/exchange:
    get:
      summary: Exchange Prices
      description: Returns professional-grade historical stock prices for all securities
        traded on a stock exchange for a single specified day.  Historical prices
        are available back to 1996 or the IPO date, with some companies with data
        back to the 1970s.
      operationId: exchange-prices
      x-api-path-slug: pricesexchange-get
      parameters:
      - in: query
        name: identifier
        description: 'the stock market ticker symbol associated with the companies
          common stock securities or the stock market index:'
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
        name: price_date
        description: the specified date in which historical stock prices are returned
          for a stock exchange
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Prices
      - Exchanges
  /companies/filings:
    get:
      summary: Company SEC Filings
      description: Returns the complete list of SEC filings for a company.
      operationId: company-sec-filings
      x-api-path-slug: companiesfilings-get
      parameters:
      - in: query
        name: end_date
        description: 'the last filing date for which to return filings, in the format:
          YYYY'
        type: string
      - in: query
        name: identifier
        description: the stock market ticker symbol associated with the company&rsquo;s
          common stock
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
        name: report_type
        description: 'the report type of the filing requested: 10'
        type: string
      - in: query
        name: start_date
        description: 'the earliest filing date for which to return filings, in the
          format: YYYY'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Companies
      - Company Filings
  /companies/insider_transactions:
    get:
      summary: Insider Transactions by Company
      description: Returns a list of all insider transactions in a company.  Criteria
        for being an insider include being a director, officer, or 10%+ owner in the
        company.  Transactions are detailed for both non-derivative and derivative
        transactions by the insider.
      operationId: insider-transactions-by-company
      x-api-path-slug: companiesinsider-transactions-get
      parameters:
      - in: query
        name: end_date
        description: 'the latest transaction date for which to return data: YYYY'
        type: string
      - in: query
        name: identifier
        description: 'the stock market ticker symbol associated with the companies
          common stock securities or the Central Index Key issued by the SEC, which
          is the unique identifier all company filings are issued under:'
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
        name: start_date
        description: 'the earliest transaction date for which to return data: YYYY'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Insider Transactions
  /news_sector_sentiments:
    get:
      summary: Sector News Sentiments
      description: Returns daily summaries of news sentiments by sector and date.
      operationId: sector-news-sentiments
      x-api-path-slug: news-sector-sentiments-get
      parameters:
      - in: query
        name: end_date
        description: 'the latest date for which to return data: YYYY'
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
        name: sector
        description: 'the name of the sector: SECTORS'
        type: string
      - in: query
        name: source
        description: 'The source of the data: tip'
        type: string
      - in: query
        name: start_date
        description: 'the earliest date for which to return data: YYYY'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - News
      - Sector
      - Sentiments
  /tags/banks:
    get:
      summary: Bank XBRL Tags and Labels
      description: Returns the Bank XBRL tags and labels for a given ticker/RSSD ID,
        statement, and date or fiscal year/fiscal quarter.
      operationId: bank-xbrl-tags-and-labels
      x-api-path-slug: tagsbanks-get
      parameters:
      - in: query
        name: fiscal_period
        description: 'the fiscal period associated with the fundamental: FY | Q1 |
          Q2 | Q3 | Q4 | Q1TTM | Q2TTM | Q3TTM | Q2YTD | Q3YTD'
        type: string
      - in: query
        name: fiscal_year
        description: 'the fiscal year associated with the fundamental: YYYY'
        type: string
      - in: query
        name: identifier
        description: 'the stock market ticker symbol associated with the companies
          common stock securities, or the bank/bank holding company RSSD ID issued
          by the Federal Reserve:'
        type: string
      - in: query
        name: item
        description: in function)
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
        name: sequence
        description: an integer 0 or greater for calling a single tag from the first
          entry
        type: string
      - in: query
        name: statement
        description: the financial statement requested from the call report, the UBPR
          report or Y
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Banks
  /executives:
    get:
      summary: Executive Master
      description: Returns a list of all executives and their unique executive identifier,
        including both U.S. and International executives.
      operationId: executive-master
      x-api-path-slug: executives-get
      parameters:
      - in: query
        name: company
        description: 'the identifier for the specified security or company:'
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
        description: a string query search of executives name
        type: string
      - in: query
        name: role
        description: the normalized executive and officer role
        type: string
      - in: query
        name: type
        description: 'select whether to show only US or International executives:
          us | non'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Executives
  /executives/companies:
    get:
      summary: Company Executive Contacts
      description: Returns a list of all information for an executive and their related
        companies.  Information includes the unique Intrinio executive company identifier,
        and detailed contact information for the executive at a specified company.
      operationId: company-executive-contacts
      x-api-path-slug: executivescompanies-get
      parameters:
      - in: query
        name: company
        description: 'the identifier for the specified security or company:'
        type: string
      - in: query
        name: identifier
        description: the Intrinio executive identifier
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Executives
      - companies
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