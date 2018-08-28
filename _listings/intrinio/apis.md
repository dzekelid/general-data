---
name: Intrinio
x-slug: intrinio
description: Intelligent Data, On Demand. The financial data platform for developers,
  investors, students, and educators, with over 200 feeds including real-time, intraday,
  EOD, and international financial data available via REST API, WebSocket, CSV, Excel,
  and Goo...
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/intrinio-logo-data-intelligence-on-demand.png
x-kinRank: "8"
x-alexaRank: "303229"
tags: General Data
created: "2018-08-27"
modified: "2018-08-27"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/intrinio/apis.md
specificationVersion: "0.14"
apis:
- name: Intrinio - Company Master
  x-api-slug: companies-get
  description: Returns the master list of all companies covered by the Intrinio Data
    Marketplace.  You can view the Company/Security Master here.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/intrinio-logo-data-intelligence-on-demand.png
  humanURL: http://www.intrinio.com
  baseURL: https://api.intrinio.com//
  tags: SaaS, Technology, Enterprise, Financial Services, Market Data, JSON, Paid
    Tier, REST, Free Tier, Have API Key, API Provider, Profiles, General Data, Relative
    Data, Service API, Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/intrinio/companies-get-openapi.md
- name: Intrinio - Securities
  x-api-slug: securities-get
  description: Returns security list and information for all securities covered by
    Intrinio.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/intrinio-logo-data-intelligence-on-demand.png
  humanURL: http://www.intrinio.com
  baseURL: https://api.intrinio.com//
  tags: SaaS, Technology, Enterprise, Financial Services, Market Data, JSON, Paid
    Tier, REST, Free Tier, Have API Key, API Provider, Profiles, General Data, Relative
    Data, Service API, Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/intrinio/securities-get-openapi.md
- name: Intrinio - Historical Data
  x-api-slug: historical-data-get
  description: Returns the historical data for for a selected identifier (ticker symbol
    or index symbol) for a selected tag.  The complete list of tags available through
    this function are available here.  Income statement, cash flow statement, and
    ratios are returned as trailing twelve months values by default, but can be changed
    with the type parameter.  All other historical data points are returned as their
    value on a certain day based on filings reported as of that date.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/intrinio-logo-data-intelligence-on-demand.png
  humanURL: http://www.intrinio.com
  baseURL: https://api.intrinio.com//
  tags: SaaS, Technology, Enterprise, Financial Services, Market Data, JSON, Paid
    Tier, REST, Free Tier, Have API Key, API Provider, Profiles, General Data, Relative
    Data, Service API, Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/intrinio/historical-data-get-openapi.md
- name: Intrinio - Exchange Prices
  x-api-slug: pricesexchange-get
  description: Returns professional-grade historical stock prices for all securities
    traded on a stock exchange for a single specified day.  Historical prices are
    available back to 1996 or the IPO date, with some companies with data back to
    the 1970s.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/intrinio-logo-data-intelligence-on-demand.png
  humanURL: http://www.intrinio.com
  baseURL: https://api.intrinio.com//
  tags: SaaS, Technology, Enterprise, Financial Services, Market Data, JSON, Paid
    Tier, REST, Free Tier, Have API Key, API Provider, Profiles, General Data, Relative
    Data, Service API, Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/intrinio/pricesexchange-get-openapi.md
- name: Intrinio - Company SEC Filings
  x-api-slug: companiesfilings-get
  description: Returns the complete list of SEC filings for a company.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/intrinio-logo-data-intelligence-on-demand.png
  humanURL: http://www.intrinio.com
  baseURL: https://api.intrinio.com//
  tags: SaaS, Technology, Enterprise, Financial Services, Market Data, JSON, Paid
    Tier, REST, Free Tier, Have API Key, API Provider, Profiles, General Data, Relative
    Data, Service API, Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/intrinio/companiesfilings-get-openapi.md
- name: Intrinio - Insider Transactions by Company
  x-api-slug: companiesinsider-transactions-get
  description: Returns a list of all insider transactions in a company.  Criteria
    for being an insider include being a director, officer, or 10%+ owner in the company.  Transactions
    are detailed for both non-derivative and derivative transactions by the insider.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/intrinio-logo-data-intelligence-on-demand.png
  humanURL: http://www.intrinio.com
  baseURL: https://api.intrinio.com//
  tags: SaaS, Technology, Enterprise, Financial Services, Market Data, JSON, Paid
    Tier, REST, Free Tier, Have API Key, API Provider, Profiles, General Data, Relative
    Data, Service API, Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/intrinio/companiesinsider-transactions-get-openapi.md
- name: Intrinio - Sector News Sentiments
  x-api-slug: news-sector-sentiments-get
  description: Returns daily summaries of news sentiments by sector and date.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/intrinio-logo-data-intelligence-on-demand.png
  humanURL: http://www.intrinio.com
  baseURL: https://api.intrinio.com//
  tags: SaaS, Technology, Enterprise, Financial Services, Market Data, JSON, Paid
    Tier, REST, Free Tier, Have API Key, API Provider, Profiles, General Data, Relative
    Data, Service API, Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/intrinio/news-sector-sentiments-get-openapi.md
- name: Intrinio - Bank XBRL Tags and Labels
  x-api-slug: tagsbanks-get
  description: Returns the Bank XBRL tags and labels for a given ticker/RSSD ID, statement,
    and date or fiscal year/fiscal quarter.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/intrinio-logo-data-intelligence-on-demand.png
  humanURL: http://www.intrinio.com
  baseURL: https://api.intrinio.com//
  tags: SaaS, Technology, Enterprise, Financial Services, Market Data, JSON, Paid
    Tier, REST, Free Tier, Have API Key, API Provider, Profiles, General Data, Relative
    Data, Service API, Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/intrinio/tagsbanks-get-openapi.md
- name: Intrinio - Executive Master
  x-api-slug: executives-get
  description: Returns a list of all executives and their unique executive identifier,
    including both U.S. and International executives.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/intrinio-logo-data-intelligence-on-demand.png
  humanURL: http://www.intrinio.com
  baseURL: https://api.intrinio.com//
  tags: SaaS, Technology, Enterprise, Financial Services, Market Data, JSON, Paid
    Tier, REST, Free Tier, Have API Key, API Provider, Profiles, General Data, Relative
    Data, Service API, Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/intrinio/executives-get-openapi.md
- name: Intrinio - Company Executive Contacts
  x-api-slug: executivescompanies-get
  description: Returns a list of all information for an executive and their related
    companies.  Information includes the unique Intrinio executive company identifier,
    and detailed contact information for the executive at a specified company.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/intrinio-logo-data-intelligence-on-demand.png
  humanURL: http://www.intrinio.com
  baseURL: https://api.intrinio.com//
  tags: SaaS, Technology, Enterprise, Financial Services, Market Data, JSON, Paid
    Tier, REST, Free Tier, Have API Key, API Provider, Profiles, General Data, Relative
    Data, Service API, Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/intrinio/executivescompanies-get-openapi.md
- name: Intrinio - Company Executive Roles
  x-api-slug: executivesroles-get
  description: For a specific executive company identifier, returns a list of all
    roles within the company.  For example, an executive may be the Chief Executive
    Officer, a Director, and the Chairman of the Board of Directors.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/intrinio-logo-data-intelligence-on-demand.png
  humanURL: http://www.intrinio.com
  baseURL: https://api.intrinio.com//
  tags: SaaS, Technology, Enterprise, Financial Services, Market Data, JSON, Paid
    Tier, REST, Free Tier, Have API Key, API Provider, Profiles, General Data, Relative
    Data, Service API, Historical Data API, Relative StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/intrinio/executivesroles-get-openapi.md
x-common:
- type: x-website
  url: http://www.intrinio.com
- type: x-api-gallery
  url: http://international.trade.administration.api.gallery.streamdata.io
- type: x-api-stack
  url: http://intrinio.stack.network
- type: x-applications-showcase
  url: https://intrinio.com/marketplace/apps
- type: x-authentication
  url: http://docs.intrinio.com/#authentication
- type: x-blog
  url: http://blog.intrinio.com/
- type: x-blog-rss
  url: http://blog.intrinio.com/feed/
- type: x-code
  url: http://docs.intrinio.com/#sdks
- type: x-crunchbase
  url: https://crunchbase.com/organization/tribunat
- type: x-developer
  url: https://intrinio.com/we-love-developers
- type: x-documentation
  url: https://intrinio.com/marketplace/data
- type: x-email
  url: cfarley@intrinio.com
- type: x-email
  url: admin@intrinio.com
- type: x-email
  url: support@intrinio.com
- type: x-email
  url: acarpenter@intrinio.com
- type: x-login
  url: https://intrinio.com/login
- type: x-partners
  url: https://intrinio.com/partners
- type: x-press
  url: https://intrinio.com/press
- type: x-rate-limits
  url: http://docs.intrinio.com/#limits
- type: x-selfservice-registration
  url: https://intrinio.com/signup
- type: x-spreadsheets
  url: http://docs.intrinio.com/#spreadsheet-add-ins
- type: x-support
  url: https://intrinio.com/help
- type: x-tutorial
  url: https://intrinio.com/tutorial/web_api
- type: x-twitter
  url: https://twitter.com/intrinio
- type: x-website
  url: https://intrinio.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---