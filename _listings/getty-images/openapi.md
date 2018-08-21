---
swagger: "2.0"
x-collection-name: Getty Images
x-complete: 1
info:
  title: Getty Images
  description: build-applications-using-the-worlds-most-powerful-imagery
  version: 1.0.0
host: api.gettyimages.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/search/events:
    get:
      summary: Search for events
      description: "Use this endpoint to search Getty Images news, sports and entertainment
        events. Getty Images photographers and videographers cover editorially relevant
        events occurring around the world.  All images or video clips produced in
        association with an event, are assigned the same EventID. EventIDs are part
        of the meta-data returned in Search Results. Only content produced under a
        Getty Images brand name (Getty Images News, Getty Images Sports, Getty Images
        Entertainment, Film Magic, Wire Image) will be consistently assigned an EventID.
        The Event framework may also be used to group similar content, such as \"Hats
        from the Royal Wedding\" or \"Odd-ballOffbeat images of the week\".   \r\n\r\nYou'll
        need an API key and access token to use this resource. Please see our [Getting
        Started](http://developers.gettyimages.com/en/getting-started.html) page for
        more information on how to sign up for an API key.\r\n\r\n\r\nYou can show
        different information in the response by specifying values on the \"fields\"
        parameter (see details below).\r\nYou can search with only an API key, and
        that will give you search results that are equivalent to doing a search on
        the GettyImages.com site without being logged in (anonymous search).  If you
        are a Getty Images API customer and would like to ensure that your API searches
        return only assets that you have a license to use, you need to also include
        an authorization token in the header of your request.  Please consult our
        [Authorization FAQ](http://developers.gettyimages.com/en/authorization-faq.html)
        for more information on authorization tokens, and our [Authorization Workflows](https://github.com/gettyimages/gettyimages-api/blob/master/OAuth2Workflow.md)
        for code examples of getting a token."
      operationId: Search_GetEvents
      x-api-path-slug: v3searchevents-get
      parameters:
      - in: header
        name: Accept-Language
        description: Provide a header to specify the language of result values
      - in: header
        name: Authorization
        description: Provide access token in the format of Bearer {token}
      - in: query
        name: date_from
        description: Filters to events that start on or after this date
      - in: query
        name: date_to
        description: Filters to events that start on or before this date
      - in: query
        name: editorial_segment
        description: Filters to events with a matching editorial segment
      - in: query
        name: fields
        description: Specifies fields to return
      - in: query
        name: page
        description: Request results starting at a page number (default is 1, maximum
          is 50)
      - in: query
        name: page_size
        description: Request number of images to return in each page
      - in: query
        name: phrase
        description: Filters to events related to this phrase
      responses:
        200:
          description: OK
      tags:
      - Images
      - Search
---