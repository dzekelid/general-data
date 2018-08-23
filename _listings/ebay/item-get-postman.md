{
  "info": {
    "name": "Ebay Get Item",
    "_postman_id": "3ca58fe0-06ba-4a35-b79b-8650a871946a",
    "description": "The Item feed file is generated each day. This call lets you download a daily TSV_GZIP (tab separated value gzip) Item feed file of all the items that were listed on a specific day in a specific category. For each item, all the item details are returned, except for the item description. The description of each item is excluded because these can be huge and items in an item group (an item with variations, such as size and color) can share the same description. The item descriptions are returned in a separate Descriptions gzip feed file by the getItemDescriptionFeed call. To store the complete item details, you would always run the getItemFeed and getItemDescriptionFeed calls with the same parameters. &nbsp;&nbsp;&nbsp; /item?feed_scope=NEWLY_LISTED&amp;category_id=625&amp;date=20170918 &nbsp;&nbsp;&nbsp; /item_description?feed_scope=NEWLY_LISTED&amp;category_id=625&amp;date=20170918 Items returned in the feed file All items in the file are: In new condition Fixed price (Buy It Now); no auctions From eBay trusted sellers The feed file contains all the items from all the child categories of the specified category. The first line of the file is the header, which indicates the order of the values on each line. Each header is described in the Response fields section on this page. Downloading feed files Item feed files are binary gzip files. If the file is larger than 100 MB, the download must be streamed in chunks. You specify the size of the chunks in bytes using the Range request header. The Content-range response header indicates where in the full resource this partial chunk of data belongs and the total number of bytes in the file. For more information about using these headers, see Retrieving a gzip feed file. Important: The response is always a TSV_GZIP file. But for documentation purposes, the response is shown as JSON fields so that the value returned in each column can be explained. The order of the response fields, shows you the order of the columns in the feed file. Restrictions For a list of supported sites and other restrictions, see API Restrictions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "auctions",
      "item": [
        {
          "id": "1f64e02e-5730-40e7-bd06-aa96ef957a4d",
          "name": "getItemFeed",
          "request": {
            "url": "http://api.ebay.com/item?category_id=%7B%7D&date=%7B%7D&feed_scope=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Range",
                "value": "{}",
                "description": "This header specifies the range in bytes of the chunks of the gzip file being returned",
                "disabled": false
              },
              {
                "key": "X-EBAY-C-MARKETPLACE-ID",
                "value": "{}",
                "description": "The ID for the eBay marketplace where the items are hosted",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "The Item feed file is generated each day"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c1c12a62-409a-4e33-ab59-4d2dc775a66d"
            }
          ]
        }
      ]
    }
  ]
}