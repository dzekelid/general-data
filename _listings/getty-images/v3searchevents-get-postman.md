{
  "info": {
    "name": "Getty Images Search for events",
    "_postman_id": "62ac41e8-1c3e-4cfe-83a5-d389e34f8151",
    "description": "Use this endpoint to search Getty Images news, sports and entertainment events. Getty Images photographers and videographers cover editorially relevant events occurring around the world.  All images or video clips produced in association with an event, are assigned the same EventID. EventIDs are part of the meta-data returned in Search Results. Only content produced under a Getty Images brand name (Getty Images News, Getty Images Sports, Getty Images Entertainment, Film Magic, Wire Image) will be consistently assigned an EventID. The Event framework may also be used to group similar content, such as \"Hats from the Royal Wedding\" or \"Odd-ballOffbeat images of the week\".   \r\n\r\nYou'll need an API key and access token to use this resource. Please see our [Getting Started](http://developers.gettyimages.com/en/getting-started.html) page for more information on how to sign up for an API key.\r\n\r\n\r\nYou can show different information in the response by specifying values on the \"fields\" parameter (see details below).\r\nYou can search with only an API key, and that will give you search results that are equivalent to doing a search on the GettyImages.com site without being logged in (anonymous search).  If you are a Getty Images API customer and would like to ensure that your API searches return only assets that you have a license to use, you need to also include an authorization token in the header of your request.  Please consult our [Authorization FAQ](http://developers.gettyimages.com/en/authorization-faq.html) for more information on authorization tokens, and our [Authorization Workflows](https://github.com/gettyimages/gettyimages-api/blob/master/OAuth2Workflow.md) for code examples of getting a token.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "images",
      "item": [
        {
          "id": "f455ee7e-0f22-4478-a2cb-bcc1b0c825b4",
          "name": "Search_GetEvents",
          "request": {
            "url": "http://api.gettyimages.com/v3/search/events?date_from=%7B%7D&date_to=%7B%7D&editorial_segment=%7B%7D&fields=%7B%7D&page=%7B%7D&page_size=%7B%7D&phrase=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept-Language",
                "value": "{}",
                "description": "Provide a header to specify the language of result values",
                "disabled": false
              },
              {
                "key": "Authorization",
                "value": "{}",
                "description": "Provide access token in the format of 'Bearer {token}'",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Use this endpoint to search Getty Images news, sports and entertainment events"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "61353c10-670e-4bab-bcb1-771a166ca81f"
            }
          ]
        }
      ]
    }
  ]
}