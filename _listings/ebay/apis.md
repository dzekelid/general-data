---
name: eBay
x-slug: ebay
description: Buy and sell electronics, cars, fashion apparel, collectibles, sporting
  goods, digital cameras, baby items, coupons, and everything else on eBay, the worlds
  online marketplace
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/138-ebay.jpg
x-kinRank: "8"
x-alexaRank: "42"
tags: General Data
created: "2018-08-27"
modified: "2018-08-27"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/ebay/apis.md
specificationVersion: "0.14"
apis:
- name: Ebay - Get Item
  x-api-slug: item-get
  description: 'The Item feed file is generated each day. This call lets you download
    a daily TSV_GZIP (tab separated value gzip) Item feed file of all the items that
    were listed on a specific day in a specific category. For each item, all the item
    details are returned, except for the item description. The description of each
    item is excluded because these can be huge and items in an item group (an item
    with variations, such as size and color) can share the same description. The item
    descriptions are returned in a separate Descriptions gzip feed file by the getItemDescriptionFeed
    call. To store the complete item details, you would always run the getItemFeed
    and getItemDescriptionFeed calls with the same parameters. &nbsp;&nbsp;&nbsp;
    /item?feed_scope=NEWLY_LISTED&amp;category_id=625&amp;date=20170918 &nbsp;&nbsp;&nbsp;
    /item_description?feed_scope=NEWLY_LISTED&amp;category_id=625&amp;date=20170918
    Items returned in the feed file All items in the file are: In new condition Fixed
    price (Buy It Now); no auctions From eBay trusted sellers The feed file contains
    all the items from all the child categories of the specified category. The first
    line of the file is the header, which indicates the order of the values on each
    line. Each header is described in the Response fields section on this page. Downloading
    feed files Item feed files are binary gzip files. If the file is larger than 100
    MB, the download must be streamed in chunks. You specify the size of the chunks
    in bytes using the Range request header. The Content-range response header indicates
    where in the full resource this partial chunk of data belongs and the total number
    of bytes in the file. For more information about using these headers, see Retrieving
    a gzip feed file. Important: The response is always a TSV_GZIP file. But for documentation
    purposes, the response is shown as JSON fields so that the value returned in each
    column can be explained. The order of the response fields, shows you the order
    of the columns in the feed file. Restrictions For a list of supported sites and
    other restrictions, see API Restrictions.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/138-ebay.jpg
  humanURL: https://ebay.com
  baseURL: https://api.ebay.com//
  tags: Commerce, Stack, internet, Marketplace, Technology, API Provider, Auctions,
    Profiles, General Data, Relative Data, Service API, Pedestal, Historical Data
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/ebay/item-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/ebay/item-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://easycron.api.gallery.streamdata.io
- type: x-api-stack
  url: http://ebay.stack.network
- type: x-blog
  url: https://go.developer.ebay.com/dev-program-blog
- type: x-crunchbase
  url: http://www.crunchbase.com/company/ebay
- type: x-crunchbase
  url: https://crunchbase.com/organization/leah
- type: x-developer
  url: https://go.developer.ebay.com/
- type: x-email
  url: spam@ebay.com
- type: x-email
  url: spoof@ebay.com
- type: x-github
  url: https://github.com/eBayDeveloper
- type: x-twitter
  url: https://twitter.com/eBay
- type: x-twitter
  url: https://twitter.com/ebaydev
- type: x-website
  url: https://ebay.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---