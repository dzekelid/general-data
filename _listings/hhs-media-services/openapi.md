---
swagger: "2.0"
x-collection-name: HHS Media Services
x-complete: 1
info:
  title: HHS Media Services
  description: div-classswaggeruiwrap-extrafooterh3common-features--behaviorsh3----div-classfeatures--------ul------------listrong-sort-paramstrong-supports-multi-column-sorting-through-the-use-of-commas-as-delimiters-and-a-hyphen-to-denote-descending-order-----------------br----------------strongspanexamplesspanstrong----------------ul--------------------lispan-classexamplenamespanspan-classdescriptionsort-results-by-name-ascendingspanli--------------------lispan-classexamplenamespanspan-classdescriptionsort-results-by-name-descendingspanli--------------------lispan-classexamplenameidspanspan-classdescriptionsort-results-by-name-descending-and-then-by-id-ascendingspanli--------------------lispan-classexampleiddatecontentauthoredspanspan-classdescriptionsort-results-by-id-ascending-and-then-date-descendingspanli----------------ul------------li------------listrongdate-formatsstrong-date-input-format-is-expected-to-be-based-on-a-hrefhttpwww-ietf-orgrfcrfc3339-txtrfc-3339a--br----------------spanstrongexamplestrongspan----------------ulli20131118t184301zliul------------li--------ul----divdiv
  termsOfService: http://www.hhs.gov/web/socialmedia/policies/tos.html#ready
  version: "2"
host: api.digitalmedia.hhs.gov
basePath: /api/v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /resources/media.json:
    get:
      summary: Get MediaItems
      description: Returns the list of MediaItems matching the specified query parameters.
      operationId: getMedia
      x-api-path-slug: resourcesmedia-json-get
      parameters:
      - in: query
        name: collectionId
        description: Restrict filtering to media items in a specific collection
      - in: query
        name: contentAuthoredBeforeDate
        description: Find all media items authored before the provided day (RFC 3339,
          time ignored)
      - in: query
        name: contentAuthoredInRange
        description: Find all media items authored between the provided start and
          end days (RFC 3339, comma separated, time ignored)
      - in: query
        name: contentAuthoredSinceDate
        description: Find all media items authored since the provided day (RFC 3339,
          time ignored)
      - in: query
        name: contentPublishedBeforeDate
        description: Find all media items published before the provided day (RFC 3339,
          time ignored)
      - in: query
        name: contentPublishedInRange
        description: Find all media items published between the provided start and
          end days (RFC 3339, comma separated, time ignored)
      - in: query
        name: contentPublishedSinceDate
        description: Find all media items published since the provided day (RFC 3339,
          time ignored)
      - in: query
        name: contentReviewedBeforeDate
        description: Find all media items reviewed before the provided day (RFC 3339,
          time ignored)
      - in: query
        name: contentReviewedInRange
        description: Find all media items reviewed between the provided start and
          end days (RFC 3339, comma separated, time ignored)
      - in: query
        name: contentReviewedSinceDate
        description: Find all media items reviewed since the provided day (RFC 3339,
          time ignored)
      - in: query
        name: contentUpdatedBeforeDate
        description: Find all media items updated before the provided day (RFC 3339,
          time ignored)
      - in: query
        name: contentUpdatedInRange
        description: Find all media items updated between the provided start and end
          days (RFC 3339, comma separated, time ignored)
      - in: query
        name: contentUpdatedSinceDate
        description: Find all media items updated since the provided day (RFC 3339,
          time ignored)
      - in: query
        name: createdBy
        description: Find all media items containing the createdBy value
      - in: query
        name: customThumbnailUrl
        description: Find all media items which have the provided customThumbnailUrl,
          case insensitive
      - in: query
        name: customThumbnailUrlContains
        description: Find all media items which contain the provided partial customThumbnailUrl,
          case insensitive
      - in: query
        name: dateContentAuthored
        description: Find all media items authored on the provided day (RFC 3339,
          time ignored)
      - in: query
        name: dateContentPublished
        description: Find all media items published on the provided day (RFC 3339,
          time ignored)
      - in: query
        name: dateContentReviewed
        description: Find all media items reviewed on the provided day (RFC 3339,
          time ignored)
      - in: query
        name: dateContentUpdated
        description: Find all media items updated on the provided day (RFC 3339, time
          ignored)
      - in: query
        name: dateSyndicationCaptured
        description: Find all media items authored on the provided day (RFC 3339,
          time ignored)
      - in: query
        name: dateSyndicationUpdated
        description: Find all media items updated on the provided day, (RFC 3339,
          time ignored)
      - in: query
        name: descriptionContains
        description: Find all media items containing the provided partial description,
          case insensitive
      - in: query
        name: hash
        description: Find all media items which match the provided hash, case insensitive
      - in: query
        name: hashContains
        description: Find all media items which match the provided partial hash, case
          insensitive
      - in: query
        name: languageId
        description: Find all media items written in the language specified by Id
      - in: query
        name: languageIsoCode
        description: Find all media items written in the language specified by 639-2
          isoCode , case insensitive
      - in: query
        name: languageName
        description: Find all media items written in the language specified by name,
          case insensitive
      - in: query
        name: max
        description: The maximum number of records to return
      - in: query
        name: mediaTypes
        description: Find all media items belonging to the specified media type[s]
      - in: query
        name: name
        description: Find all media items containing the provided name, case insensitive
      - in: query
        name: nameContains
        description: Find all media items containing the partial name, case insensitive
      - in: query
        name: offset
        description: The offset of the records set to return for pagination
      - in: query
        name: order
        description: '* The ascending or descending order'
      - in: query
        name: restrictToSet
        description: Find only media from within the supplied list of Ids
      - in: query
        name: sort
        description: '* Set of fields to sort the records by'
      - in: query
        name: sourceAcronym
        description: Find all media items that belong to the source specified by acronym,
          case insensitive
      - in: query
        name: sourceAcronymContains
        description: Find all media items that belong to the source specified by partial
          acronym, case insensitive
      - in: query
        name: sourceId
        description: Find all media items that belong to the source specified by Id
      - in: query
        name: sourceName
        description: Find all media items that belong to the source specified by name,
          case insensitive
      - in: query
        name: sourceNameContains
        description: Find all media items that belong to the source specified by partial
          name, case insensitive
      - in: query
        name: sourceUrl
        description: Find all media items which have the provided sourceUrl, case
          insensitive
      - in: query
        name: sourceUrlContains
        description: Find all media items which contain the provided partial sourceUrl,
          case insensitive
      - in: query
        name: syndicationCapturedBeforeDate
        description: Find all media items authored before the provided day (RFC 3339,
          time ignored)
      - in: query
        name: syndicationCapturedInRange
        description: Find all media items authored between the provided start and
          end days (RFC 3339, comma separated, time ignored)
      - in: query
        name: syndicationCapturedSinceDate
        description: Find all media items authored since the provided day (RFC 3339,
          time ignored)
      - in: query
        name: syndicationUpdatedBeforeDate
        description: Find all media items updated before the provided day, (RFC 3339,
          time ignored)
      - in: query
        name: syndicationUpdatedInRange
        description: Find all media items updated between the provided start and end
          days, (RFC 3339, comma separated, time ignored)
      - in: query
        name: syndicationUpdatedSinceDate
        description: Find all media items updated since the provided day, (RFC 3339,
          time ignored)
      - in: query
        name: syndicationVisibleBeforeDate
        description: Find all media items visible before the provided day, (RFC 3339,
          time ignored)
      - in: query
        name: syndicationVisibleInRange
        description: Find all media items visible between the provided start and end
          days, (RFC 3339, comma separated, time ignored)
      - in: query
        name: syndicationVisibleSinceDate
        description: Find all media items visible since the provided day, (RFC 3339,
          time ignored)
      - in: query
        name: tagIds
        description: Find only media items tagged with the specified tag Ids
      responses:
        200:
          description: OK
      tags:
      - Resources
      - Media
---