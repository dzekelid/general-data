---
swagger: "2.0"
x-collection-name: Stack Exchange
x-complete: 0
info:
  title: Stack Exchange Get User Reputation
  description: "Gets a subset of the reputation changes for users in {ids}.\n \nReputation
    changes are intentionally scrubbed of some data to make it difficult to correlate
    votes on particular posts with user reputation changes. That being said, this
    method returns enough data for reasonable display of reputation trends.\n \n{ids}
    can contain up to 100 semicolon delimited ids, to find ids programatically look
    for user_id on user or shallow_user objects.\n \nThis method returns a list of
    reputation objects."
  version: "2.0"
host: api.stackexchange.com
basePath: /2.2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /answers:
    get:
      summary: Get Answers
      description: "Returns all the undeleted answers in the system.\n \nThe sorts
        accepted by this method operate on the follow fields of the answer object:\n
        - activity - last_activity_date\n - creation - creation_date\n - votes - score\n
        \ activity is the default sort.\n \n It is possible to create moderately complex
        queries using sort, min, max, fromdate, and todate.\n \nThis method returns
        a list of answers."
      operationId: returns-all-the-undeleted-answers-in-the-system-the-sorts-accepted-by-this-method-operate-on-the-fol
      x-api-path-slug: answers-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: Filter the discussion
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Answers
  /answers/{ids}/comments:
    get:
      summary: Get Answer Comments
      description: "Gets the comments on a set of answers.\n \nIf you know that you
        have an answer id and need the comments, use this method. If you know you
        have a question id, use /questions/{id}/comments. If you are unsure, use /posts/{id}/comments.\n
        \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically
        look for answer_id on answer objects.\n \nThe sorts accepted by this method
        operate on the follow fields of the comment object:\n - creation - creation_date\n
        - votes - score\n  creation is the default sort.\n \n It is possible to create
        moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
        method returns a list of comments."
      operationId: gets-the-comments-on-a-set-of-answers-if-you-know-that-you-have-an-answer-id-and-need-the-comments-u
      x-api-path-slug: answersidscomments-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: max
        description: sort = creation => datesort = votes => number
      - in: query
        name: min
        description: sort = creation => datesort = votes => number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Answers
      - comments
  /comments:
    get:
      summary: Get Comments
      description: "Gets all the comments on the site.\n \nIf you're filtering for
        interesting comments (by score, creation date, etc.) make use of the sort
        paramter with appropriate min and max values.\n \nIf you're looking to query
        conversations between users, instead use the /users/{ids}/mentioned and /users/{ids}/comments/{toid}
        methods.\n \nThe sorts accepted by this method operate on the follow fields
        of the comment object:\n - creation - creation_date\n - votes - score\n  creation
        is the default sort.\n \n It is possible to create moderately complex queries
        using sort, min, max, fromdate, and todate.\n \nThis method returns a list
        of comments."
      operationId: gets-all-the-comments-on-the-site-if-youre-filtering-for-interesting-comments-by-score-creation-date
      x-api-path-slug: comments-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: max
        description: sort = creation => datesort = votes => number
      - in: query
        name: min
        description: sort = creation => datesort = votes => number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Comments
  /posts:
    get:
      summary: Get Posts
      description: "Fetches all posts (questions and answers) on the site.\n \nIn
        many ways this method is the union of /questions and /answers, returning both
        sets of data albeit only the common fields.\n \nMost applications should use
        the question or answer specific methods, but /posts is available for those
        rare cases where any activity is of intereset. Examples of such queries would
        be: \"all posts on Jan. 1st 2011\" or \"top 10 posts by score of all time\".\n
        \nThe sorts accepted by this method operate on the follow fields of the post
        object:\n - activity - last_activity_date\n - creation - creation_date\n -
        votes - score\n  activity is the default sort.\n \n It is possible to create
        moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
        method returns a list of posts."
      operationId: fetches-all-posts-questions-and-answers-on-the-site-in-many-ways-this-method-is-the-union-of-questio
      x-api-path-slug: posts-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Posts
  /posts/{ids}/comments:
    get:
      summary: Get Post Comments
      description: "Gets the comments on the posts identified in ids, regardless of
        the type of the posts.\n \nThis method is meant for cases when you are unsure
        of the type of the post id provided. Generally, this would be due to obtaining
        the post id directly from a user.\n \n{ids} can contain up to 100 semicolon
        delimited ids, to find ids programatically look for post_id, answer_id, or
        question_id on post, answer, and question objects respectively.\n \nThe sorts
        accepted by this method operate on the follow fields of the comment object:\n
        - creation - creation_date\n - votes - score\n  creation is the default sort.\n
        \n It is possible to create moderately complex queries using sort, min, max,
        fromdate, and todate.\n \nThis method returns a list of comments."
      operationId: gets-the-comments-on-the-posts-identified-in-ids-regardless-of-the-type-of-the-posts-this-method-is-
      x-api-path-slug: postsidscomments-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: max
        description: sort = creation => datesort = votes => number
      - in: query
        name: min
        description: sort = creation => datesort = votes => number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Posts
      - Comments
  /posts/{ids}/revisions:
    get:
      summary: Get Post Revisions
      description: "Returns edit revisions for the posts identified in ids.\n \n{ids}
        can contain up to 100 semicolon delimited ids, to find ids programatically
        look for post_id, answer_id, or question_id on post, answer, and question
        objects respectively.\n \nThis method returns a list of revisions."
      operationId: returns-edit-revisions-for-the-posts-identified-in-ids-ids-can-contain-up-to-100-semicolon-delimited
      x-api-path-slug: postsidsrevisions-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Posts
      - Revisions
  /questions:
    get:
      summary: Get Questions
      description: "Gets all the questions on the site.\n \nThis method allows you
        make fairly flexible queries across the entire corpus of questions on a site.
        For example, getting all questions asked in the the week of Jan 1st 2011 with
        scores of 10 or more is a single query with parameters sort=votes&min=10&fromdate=1293840000&todate=1294444800.\n
        \nTo constrain questions returned to those with a set of tags, use the tagged
        parameter with a semi-colon delimited list of tags. This is an and contraint,
        passing tagged=c;java will return only those questions with both tags. As
        such, passing more than 5 tags will always return zero results.\n \nThe sorts
        accepted by this method operate on the follow fields of the question object:\n
        - activity - last_activity_date\n - creation - creation_date\n - votes - score\n
        - hot - by the formula ordering the hot tab Does not accept min or max\n -
        week - by the formula ordering the week tab Does not accept min or max\n -
        month - by the formula ordering the month tab Does not accept min or max\n
        \ activity is the default sort.\n \n It is possible to create moderately complex
        queries using sort, min, max, fromdate, and todate.\n \nThis method returns
        a list of questions."
      operationId: gets-all-the-questions-on-the-site-this-method-allows-you-make-fairly-flexible-queries-across-the-en
      x-api-path-slug: questions-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          numbersort = hot => nonesort = week => nonesort = month => nonesort = relevance
          => none
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          numbersort = hot => nonesort = week => nonesort = month => nonesort = relevance
          => none
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: tagged
        description: String list (semicolon delimited)
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Questions
  /questions/no-answers:
    get:
      summary: Get Questions No Answers
      description: "Returns questions which have received no answers.\n \nCompare
        with /questions/unanswered which mearly returns questions that the sites consider
        insufficiently well answered.\n \nThis method corresponds roughly with the
        this site tab.\n \nTo constrain questions returned to those with a set of
        tags, use the tagged parameter with a semi-colon delimited list of tags. This
        is an and contraint, passing tagged=c;java will return only those questions
        with both tags. As such, passing more than 5 tags will always return zero
        results.\n \nThe sorts accepted by this method operate on the follow fields
        of the question object:\n - activity - last_activity_date\n - creation - creation_date\n
        - votes - score\n  activity is the default sort.\n \n It is possible to create
        moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
        method returns a list of questions."
      operationId: returns-questions-which-have-received-no-answers-compare-with-questionsunanswered-which-mearly-retur
      x-api-path-slug: questionsnoanswers-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: tagged
        description: String list (semicolon delimited)
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Questions
  /questions/{ids}:
    get:
      summary: Get Questions
      description: "Returns the questions identified in {ids}.\n \nThis is most useful
        for fetching fresh data when maintaining a cache of question ids, or polling
        for changes.\n \n{ids} can contain up to 100 semicolon delimited ids, to find
        ids programatically look for question_id on question objects.\n \nThe sorts
        accepted by this method operate on the follow fields of the question object:\n
        - activity - last_activity_date\n - creation - creation_date\n - votes - score\n
        \ activity is the default sort.\n \n It is possible to create moderately complex
        queries using sort, min, max, fromdate, and todate.\n \nThis method returns
        a list of questions."
      operationId: returns-the-questions-identified-in-ids-this-is-most-useful-for-fetching-fresh-data-when-maintaining
      x-api-path-slug: questionsids-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Questions
  /questions/{ids}/linked:
    get:
      summary: Get Question Linked
      description: "Gets questions which link to those questions identified in {ids}.\n
        \nThis method only considers questions that are linked within a site, and
        will never return questions from another Stack Exchange site.\n \nA question
        is considered \"linked\" when it explicitly includes a hyperlink to another
        question, there are no other heuristics.\n \n{ids} can contain up to 100 semicolon
        delimited ids, to find ids programatically look for question_id on question
        objects.\n \nThe sorts accepted by this method operate on the follow fields
        of the question object:\n - activity - last_activity_date\n - creation - creation_date\n
        - votes - score\n - rank - a priority sort by site applies, subject to change
        at any time Does not accept min or max\n  activity is the default sort.\n
        \n It is possible to create moderately complex queries using sort, min, max,
        fromdate, and todate.\n \nThis method returns a list of questions."
      operationId: gets-questions-which-link-to-those-questions-identified-in-ids-this-method-only-considers-questions-
      x-api-path-slug: questionsidslinked-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          numbersort = rank => none
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          numbersort = rank => none
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Questions
      - Linked
  /questions/{ids}/related:
    get:
      summary: Get Question Related
      description: "Returns questions that the site considers related to those identified
        in {ids}.\n \nThe algorithm for determining if questions are related is not
        documented, and subject to change at any time. Futhermore, these values are
        very heavily cached, and may not update immediately after a question has been
        editted. It is also not guaranteed that a question will be considered related
        to any number (even non-zero) of questions, and a consumer should be able
        to handle a variable number of returned questions.\n \n{ids} can contain up
        to 100 semicolon delimited ids, to find ids programatically look for question_id
        on question objects.\n \nThe sorts accepted by this method operate on the
        follow fields of the question object:\n - activity - last_activity_date\n
        - creation - creation_date\n - votes - score\n - rank - a priority sort by
        site applies, subject to change at any time Does not accept min or max\n  activity
        is the default sort.\n \n It is possible to create moderately complex queries
        using sort, min, max, fromdate, and todate.\n \nThis method returns a list
        of questions."
      operationId: returns-questions-that-the-site-considers-related-to-those-identified-in-ids-the-algorithm-for-deter
      x-api-path-slug: questionsidsrelated-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          numbersort = rank => none
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          numbersort = rank => none
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Questions
      - Related
  /revisions/{ids}:
    get:
      summary: Get Revisions
      description: "Returns edit revisions identified by ids in {ids}.\n \n{ids} can
        contain up to 20 semicolon delimited ids, to find ids programatically look
        for revision_guid on revision objects. Note that unlike most other id types
        in the API, revision_guid is a string.\n \nThis method returns a list of revisions."
      operationId: returns-edit-revisions-identified-by-ids-in-ids-ids-can-contain-up-to-20-semicolon-delimited-ids-to-
      x-api-path-slug: revisionsids-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: ids
        description: Guid list (semicolon delimited)
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Revisions
  /search:
    get:
      summary: Search
      description: "Searches a site for any questions which fit the given criteria.\n
        \nThis method is intentionally quite limited. For more general searching,
        you should use a proper internet search engine restricted to the domain of
        the site in question.\n \nAt least one of tagged or intitle must be set on
        this method. nottagged is only used if tagged is also set, for performance
        reasons.\n \ntagged and nottagged are semi-colon delimited list of tags. At
        least 1 tag in tagged will be on each returned question if it is passed, making
        it the OR equivalent of the AND version of tagged on /questions.\n \nThe sorts
        accepted by this method operate on the follow fields of the question object:\n
        - activity - last_activity_date\n - creation - creation_date\n - votes - score\n
        - relevance - matches the relevance tab on the site itself Does not accept
        min or max\n  activity is the default sort.\n \n It is possible to create
        moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
        method returns a list of questions."
      operationId: searches-a-site-for-any-questions-which-fit-the-given-criteria-this-method-is-intentionally-quite-li
      x-api-path-slug: search-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: intitle
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          numbersort = relevance => none
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          numbersort = relevance => none
      - in: query
        name: nottagged
        description: String list (semicolon delimited)
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: tagged
        description: String list (semicolon delimited)
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Search
  /search/advanced:
    get:
      summary: Advanced Search
      description: "Searches a site for any questions which fit the given criteria.\n
        \nSearch criteria are expressed using the following parameters:\n  - q - a
        free form text parameter, will match all question properties based on an undocumented
        algorithm.\n - accepted - true to return only questions with accepted answers,
        false to return only those without. Omit to elide constraint.\n - answers
        - the minimum number of answers returned questions must have.\n - body - text
        which must appear in returned questions' bodies.\n - closed - true to return
        only closed questions, false to return only open ones. Omit to elide constraint.\n
        - migrated - true to return only questions migrated away from a site, false
        to return only those not. Omit to elide constraint.\n - notice - true to return
        only questions with post notices, false to return only those without. Omit
        to elide constraint.\n - nottagged - a semicolon delimited list of tags, none
        of which will be present on returned questions.\n - tagged - a semicolon delimited
        list of tags, of which at least one will be present on all returned questions.\n
        - title - text which must appear in returned questions' titles.\n - user -
        the id of the user who must own the questions returned.\n - url - a url which
        must be contained in a post, may include a wildcard.\n - views - the minimum
        number of views returned questions must have.\n - wiki - true to return only
        community wiki questions, false to return only non-community wiki ones. Omit
        to elide constraint.\n  \nAt least one additional parameter must be set if
        nottagged is set, for performance reasons.\n \nThe sorts accepted by this
        method operate on the follow fields of the question object:\n - activity -
        last_activity_date\n - creation - creation_date\n - votes - score\n - relevance
        - matches the relevance tab on the site itself Does not accept min or max\n
        \ activity is the default sort.\n \n It is possible to create moderately complex
        queries using sort, min, max, fromdate, and todate.\n \nThis method returns
        a list of questions."
      operationId: searches-a-site-for-any-questions-which-fit-the-given-criteria-search-criteria-are-expressed-using-t
      x-api-path-slug: searchadvanced-get
      parameters:
      - in: query
        name: accepted
      - in: query
        name: answers
      - in: query
        name: body
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: closed
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          numbersort = relevance => none
      - in: query
        name: migrated
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          numbersort = relevance => none
      - in: query
        name: notice
      - in: query
        name: nottagged
        description: String list (semicolon delimited)
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: q
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: tagged
        description: String list (semicolon delimited)
      - in: query
        name: title
      - in: query
        name: todate
        description: Unix date
      - in: query
        name: url
      - in: query
        name: user
      - in: query
        name: views
      - in: query
        name: wiki
      responses:
        200:
          description: OK
      tags:
      - Search
  /similar:
    get:
      summary: Get Similar
      description: "Returns questions which are similar to a hypothetical one based
        on a title and tag combination.\n \nThis method is roughly equivalent to a
        site's related questions suggestion on the ask page.\n \nThis method is useful
        for correlating data outside of a Stack Exchange site with similar content
        within one.\n \nNote that title must always be passed as a parameter. tagged
        and nottagged are optional, semi-colon delimited lists of tags.\n \nIf tagged
        is passed it is treated as a preference, there is no guarantee that questions
        returned will have any of those tags. nottagged is treated as a requirement,
        no questions will be returned with those tags.\n \nThe sorts accepted by this
        method operate on the follow fields of the question object:\n - activity -
        last_activity_date\n - creation - creation_date\n - votes - score\n - relevance
        - order by \"how similar\" the questions are, most likely candidate first
        with a descending order Does not accept min or max\n  activity is the default
        sort.\n \n It is possible to create moderately complex queries using sort,
        min, max, fromdate, and todate.\n \nThis method returns a list of questions."
      operationId: returns-questions-which-are-similar-to-a-hypothetical-one-based-on-a-title-and-tag-combination-this-
      x-api-path-slug: similar-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          numbersort = relevance => none
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          numbersort = relevance => none
      - in: query
        name: nottagged
        description: String list (semicolon delimited)
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: tagged
        description: String list (semicolon delimited)
      - in: query
        name: title
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Similar
  /tags:
    get:
      summary: Get Tags
      description: "Returns the tags found on a site.\n \nThe inname parameter lets
        a consumer filter down to tags that contain a certain substring. For example,
        inname=own would return both \"download\" and \"owner\" amongst others.\n
        \nThis method returns a list of tags.\n \nThe sorts accepted by this method
        operate on the follow fields of the tag object:\n - popular - count\n - activity
        - the creation_date of the last question asked with the tag\n - name - name\n
        \ popular is the default sort.\n \n It is possible to create moderately complex
        queries using sort, min, max, fromdate, and todate."
      operationId: returns-the-tags-found-on-a-site-the-inname-parameter-lets-a-consumer-filter-down-to-tags-that-conta
      x-api-path-slug: tags-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: inname
      - in: query
        name: max
        description: sort = popular => numbersort = activity => datesort = name =>
          string
      - in: query
        name: min
        description: sort = popular => numbersort = activity => datesort = name =>
          string
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Tags
  /tags/required:
    get:
      summary: Get Tags Requred
      description: "Returns the tags found on a site that fulfill required tag constraints
        on questions.\n \nThe inname parameter lets a consumer filter down to tags
        that contain a certain substring. For example, inname=own would return both
        \"download\" and \"owner\" amongst others.\n \nThis method returns a list
        of tags.\n \nThe sorts accepted by this method operate on the follow fields
        of the tag object:\n - popular - count\n - activity - the creation_date of
        the last question asked with the tag\n - name - name\n  popular is the default
        sort.\n \n It is possible to create moderately complex queries using sort,
        min, max, fromdate, and todate."
      operationId: returns-the-tags-found-on-a-site-that-fulfill-required-tag-constraints-on-questions-the-inname-param
      x-api-path-slug: tagsrequired-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: inname
      - in: query
        name: max
        description: sort = popular => numbersort = activity => datesort = name =>
          string
      - in: query
        name: min
        description: sort = popular => numbersort = activity => datesort = name =>
          string
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Tags
      - Required
  /tags/synonyms:
    get:
      summary: Get Tags Synonyms
      description: "Returns all tag synonyms found a site.\n \nWhen searching for
        synonyms of specific tags, it is better to use /tags/{tags}/synonyms over
        this method.\n \nThe sorts accepted by this method operate on the follow fields
        of the tag_synonym object:\n - creation - creation_date\n - applied - applied_count\n
        - activity - last_applied_date\n  creation is the default sort.\n \n It is
        possible to create moderately complex queries using sort, min, max, fromdate,
        and todate.\n \nThis method returns a list of tag_synonyms."
      operationId: returns-all-tag-synonyms-found-a-site-when-searching-for-synonyms-of-specific-tags-it-is-better-to-u
      x-api-path-slug: tagssynonyms-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: max
        description: sort = creation => datesort = applied => numbersort = activity
          => date
      - in: query
        name: min
        description: sort = creation => datesort = applied => numbersort = activity
          => date
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Tags
      - Synonyms
  /tags/{tags}/info:
    get:
      summary: Get Tags Info
      description: "Returns tag objects representing the tags in {tags} found on the
        site.\n \nThis method diverges from the standard naming patterns to avoid
        to conflicting with existing methods, due to the free form nature of tag names.\n
        \nThis method returns a list of tags.\n \nThe sorts accepted by this method
        operate on the follow fields of the tag object:\n - popular - count\n - activity
        - the creation_date of the last question asked with the tag\n - name - name\n
        \ popular is the default sort.\n \n It is possible to create moderately complex
        queries using sort, min, max, fromdate, and todate."
      operationId: returns-tag-objects-representing-the-tags-in-tags-found-on-the-site-this-method-diverges-from-the-st
      x-api-path-slug: tagstagsinfo-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: max
        description: sort = popular => numbersort = activity => datesort = name =>
          string
      - in: query
        name: min
        description: sort = popular => numbersort = activity => datesort = name =>
          string
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: path
        name: tags
        description: String list (semicolon delimited)
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Tags
      - Information
  /tags/{tags}/synonyms:
    get:
      summary: Get Tags Synonyms
      description: "Gets all the synonyms that point to the tags identified in {tags}.
        If you're looking to discover all the tag synonyms on a site, use the /tags/synonyms
        methods instead of call this method on all tags.\n \n{tags} can contain up
        to 20 individual tags per request.\n \nThe sorts accepted by this method operate
        on the follow fields of the tag_synonym object:\n - creation - creation_date\n
        - applied - applied_count\n - activity - last_applied_date\n  creation is
        the default sort.\n \n It is possible to create moderately complex queries
        using sort, min, max, fromdate, and todate.\n \nThis method returns a list
        of tag synonyms."
      operationId: gets-all-the-synonyms-that-point-to-the-tags-identified-in-tags-if-youre-looking-to-discover-all-the
      x-api-path-slug: tagstagssynonyms-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: max
        description: sort = creation => datesort = applied => numbersort = activity
          => date
      - in: query
        name: min
        description: sort = creation => datesort = applied => numbersort = activity
          => date
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: path
        name: tags
        description: String list (semicolon delimited)
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Tags
      - Synonyms
  /users:
    get:
      summary: Get Users
      description: "Returns all users on a site.\n \nThis method returns a list of
        users.\n \nThe sorts accepted by this method operate on the follow fields
        of the user object:\n - reputation - reputation\n - creation - creation_date\n
        - name - display_name\n - modified - last_modified_date\n  reputation is the
        default sort.\n \n It is possible to create moderately complex queries using
        sort, min, max, fromdate, and todate.\n \nThe inname parameter lets consumers
        filter the results down to just those users with a certain substring in their
        display name. For example, inname=kevin will return all users with both users
        named simply \"Kevin\" or those with Kevin as one of (or part of) their names;
        such as \"Kevin Montrose\"."
      operationId: returns-all-users-on-a-site-this-method-returns-a-list-of-users-the-sorts-accepted-by-this-method-op
      x-api-path-slug: users-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: inname
      - in: query
        name: max
        description: sort = reputation => numbersort = creation => datesort = name
          => stringsort = modified => date
      - in: query
        name: min
        description: sort = reputation => numbersort = creation => datesort = name
          => stringsort = modified => date
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Users
  /users/moderators:
    get:
      summary: Get User Moderators
      description: "Gets those users on a site who can exercise moderation powers.\n
        \nNote, employees of Stack Exchange Inc. will be returned if they have been
        granted moderation powers on a site even if they have never been appointed
        or elected explicitly. This method checks abilities, not the manner in which
        they were obtained.\n \nThe sorts accepted by this method operate on the follow
        fields of the user object:\n - reputation - reputation\n - creation - creation_date\n
        - name - display_name\n - modified - last_modified_date\n  reputation is the
        default sort.\n \n It is possible to create moderately complex queries using
        sort, min, max, fromdate, and todate.\n \nThis method returns a list of users."
      operationId: gets-those-users-on-a-site-who-can-exercise-moderation-powers-note-employees-of-stack-exchange-inc-w
      x-api-path-slug: usersmoderators-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: max
        description: sort = reputation => numbersort = creation => datesort = name
          => stringsort = modified => date
      - in: query
        name: min
        description: sort = reputation => numbersort = creation => datesort = name
          => stringsort = modified => date
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Users
      - Moderators
  /users/moderators/elected:
    get:
      summary: Get Users Moderators Elected
      description: "Returns those users on a site who both have moderator powers,
        and were actually elected.\n \nThis method excludes Stack Exchange Inc. employees,
        unless they were actually elected moderators on a site (which can only have
        happened prior to their employment).\n \nThe sorts accepted by this method
        operate on the follow fields of the user object:\n - reputation - reputation\n
        - creation - creation_date\n - name - display_name\n - modified - last_modified_date\n
        \ reputation is the default sort.\n \n It is possible to create moderately
        complex queries using sort, min, max, fromdate, and todate.\n \nThis method
        returns a list of users."
      operationId: returns-those-users-on-a-site-who-both-have-moderator-powers-and-were-actually-elected-this-method-e
      x-api-path-slug: usersmoderatorselected-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: max
        description: sort = reputation => numbersort = creation => datesort = name
          => stringsort = modified => date
      - in: query
        name: min
        description: sort = reputation => numbersort = creation => datesort = name
          => stringsort = modified => date
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Users
      - Moderators
  /users/{ids}:
    get:
      summary: Get User
      description: "Gets the users identified in ids in {ids}.\n \nTypically this
        method will be called to fetch user profiles when you have obtained user ids
        from some other source, such as /questions.\n \n{ids} can contain up to 100
        semicolon delimited ids, to find ids programatically look for user_id on user
        or shallow_user objects.\n \nThe sorts accepted by this method operate on
        the follow fields of the user object:\n - reputation - reputation\n - creation
        - creation_date\n - name - display_name\n - modified - last_modified_date\n
        \ reputation is the default sort.\n \n It is possible to create moderately
        complex queries using sort, min, max, fromdate, and todate.\n \nThis method
        returns a list of users."
      operationId: gets-the-users-identified-in-ids-in-ids-typically-this-method-will-be-called-to-fetch-user-profiles-
      x-api-path-slug: usersids-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: max
        description: sort = reputation => numbersort = creation => datesort = name
          => stringsort = modified => date
      - in: query
        name: min
        description: sort = reputation => numbersort = creation => datesort = name
          => stringsort = modified => date
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Users
  /users/{ids}/answers:
    get:
      summary: Get User Answers
      description: "Returns the answers the users in {ids} have posted.\n \n{ids}
        can contain up to 100 semicolon delimited ids, to find ids programatically
        look for user_id on user or shallow_user objects.\n \nThe sorts accepted by
        this method operate on the follow fields of the answer object:\n - activity
        - last_activity_date\n - creation - creation_date\n - votes - score\n  activity
        is the default sort.\n \n It is possible to create moderately complex queries
        using sort, min, max, fromdate, and todate.\n \nThis method returns a list
        of answers."
      operationId: returns-the-answers-the-users-in-ids-have-posted-ids-can-contain-up-to-100-semicolon-delimited-ids-t
      x-api-path-slug: usersidsanswers-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Users
      - Answers
  /users/{ids}/badges:
    get:
      summary: Get User Badges
      description: "Get the badges the users in {ids} have earned.\n \nBadge sorts
        are a tad complicated. For the purposes of sorting (and min/max) tag_based
        is considered to be greater than named.\n \nThis means that you can get a
        list of all tag based badges a user has by passing min=tag_based, and conversely
        all the named badges by passing max=named, with sort=type.\n \nFor ranks,
        bronze is greater than silver which is greater than gold. Along with sort=rank,
        set max=gold for just gold badges, max=silver&min=silver for just silver,
        and min=bronze for just bronze.\n \nrank is the default sort.\n \n{ids} can
        contain up to 100 semicolon delimited ids, to find ids programatically look
        for user_id on user or shallow_user objects.\n \nThis method returns a list
        of badges."
      operationId: get-the-badges-the-users-in-ids-have-earned-badge-sorts-are-a-tad-complicated-for-the-purposes-of-so
      x-api-path-slug: usersidsbadges-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: max
        description: sort = rank => stringsort = name => stringsort = type => stringsort
          = awarded => date
      - in: query
        name: min
        description: sort = rank => stringsort = name => stringsort = type => stringsort
          = awarded => date
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Users
      - Badges
  /users/{ids}/comments:
    get:
      summary: Get User Comments
      description: "Get the comments posted by users in {ids}.\n \n{ids} can contain
        up to 100 semicolon delimited ids, to find ids programatically look for user_id
        on user or shallow_user objects.\n \nThe sorts accepted by this method operate
        on the follow fields of the comment object:\n - creation - creation_date\n
        - votes - score\n  creation is the default sort.\n \n It is possible to create
        moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
        method returns a list of comments."
      operationId: get-the-comments-posted-by-users-in-ids-ids-can-contain-up-to-100-semicolon-delimited-ids-to-find-id
      x-api-path-slug: usersidscomments-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: max
        description: sort = creation => datesort = votes => number
      - in: query
        name: min
        description: sort = creation => datesort = votes => number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Users
      - Comments
  /users/{ids}/favorites:
    get:
      summary: Get User Favorites
      description: "Get the questions that users in {ids} have favorited.\n \nThis
        method is effectively a view onto a user's favorites tab.\n \n{ids} can contain
        up to 100 semicolon delimited ids, to find ids programatically look for user_id
        on user or shallow_user objects.\n \nThe sorts accepted by this method operate
        on the follow fields of the question object:\n - activity - last_activity_date\n
        - creation - creation_date\n - votes - score\n - added - when the user favorited
        the question\n  activity is the default sort.\n \n It is possible to create
        moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
        method returns a list of questions."
      operationId: get-the-questions-that-users-in-ids-have-favorited-this-method-is-effectively-a-view-onto-a-users-fa
      x-api-path-slug: usersidsfavorites-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          numbersort = added => date
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          numbersort = added => date
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Users
      - Favorites
  /users/{ids}/mentioned:
    get:
      summary: Get User Mentioned
      description: "Gets all the comments that the users in {ids} were mentioned in.\n
        \nNote, to count as a mention the comment must be considered to be \"in reply
        to\" a user. Most importantly, this means that a comment can only be in reply
        to a single user.\n \n{ids} can contain up to 100 semicolon delimited ids,
        to find ids programatically look for user_id on user or shallow_user objects.\n
        \nThe sorts accepted by this method operate on the follow fields of the comment
        object:\n - creation - creation_date\n - votes - score\n  It is possible to
        create moderately complex queries using sort, min, max, fromdate, and todate.\n
        \nThis method returns a list of comments."
      operationId: gets-all-the-comments-that-the-users-in-ids-were-mentioned-in-note-to-count-as-a-mention-the-comment
      x-api-path-slug: usersidsmentioned-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: max
        description: sort = creation => datesort = votes => number
      - in: query
        name: min
        description: sort = creation => datesort = votes => number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Users
      - Mentioned
  /users/{ids}/questions:
    get:
      summary: Get User Questions
      description: "Gets the questions asked by the users in {ids}.\n \n{ids} can
        contain up to 100 semicolon delimited ids, to find ids programatically look
        for user_id on user or shallow_user objects.\n \nThe sorts accepted by this
        method operate on the follow fields of the question object:\n - activity -
        last_activity_date\n - creation - creation_date\n - votes - score\n  activity
        is the default sort.\n \n It is possible to create moderately complex queries
        using sort, min, max, fromdate, and todate.\n \nThis method returns a list
        of questions."
      operationId: gets-the-questions-asked-by-the-users-in-ids-ids-can-contain-up-to-100-semicolon-delimited-ids-to-fi
      x-api-path-slug: usersidsquestions-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Users
      - Questions
  /users/{ids}/questions/featured:
    get:
      summary: Get User Questions Featured
      description: "Gets the questions on which the users in {ids} have active bounties.\n
        \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically
        look for user_id on user or shallow_user objects.\n \nThe sorts accepted by
        this method operate on the follow fields of the question object:\n - activity
        - last_activity_date\n - creation - creation_date\n - votes - score\n  activity
        is the default sort.\n \n It is possible to create moderately complex queries
        using sort, min, max, fromdate, and todate.\n \nThis method returns a list
        of questions."
      operationId: gets-the-questions-on-which-the-users-in-ids-have-active-bounties-ids-can-contain-up-to-100-semicolo
      x-api-path-slug: usersidsquestionsfeatured-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Users
      - Featured
  /users/{ids}/questions/no-answers:
    get:
      summary: Get User Questions No Answers
      description: "Gets the questions asked by the users in {ids} which have no answers.\n
        \nQuestions returns by this method actually have zero undeleted answers. It
        is completely disjoint /users/{ids}/questions/unanswered and /users/{ids}/questions/unaccepted,
        which only return questions with at least one answer, subject to other contraints.\n
        \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically
        look for user_id on user or shallow_user objects.\n \nThe sorts accepted by
        this method operate on the follow fields of the question object:\n - activity
        - last_activity_date\n - creation - creation_date\n - votes - score\n  activity
        is the default sort.\n \n It is possible to create moderately complex queries
        using sort, min, max, fromdate, and todate.\n \nThis method returns a list
        of questions."
      operationId: gets-the-questions-asked-by-the-users-in-ids-which-have-no-answers-questions-returns-by-this-method-
      x-api-path-slug: usersidsquestionsnoanswers-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Users
      - Answers
  /users/{ids}/questions/unaccepted:
    get:
      summary: Get User Questions Unnacepted
      description: "Gets the questions asked by the users in {ids} which have at least
        one answer, but no accepted answer.\n \nQuestions returned by this method
        have answers, but the owner has not opted to accept any of them.\n \n{ids}
        can contain up to 100 semicolon delimited ids, to find ids programatically
        look for user_id on user or shallow_user objects.\n \nThe sorts accepted by
        this method operate on the follow fields of the question object:\n - activity
        - last_activity_date\n - creation - creation_date\n - votes - score\n  activity
        is the default sort.\n \n It is possible to create moderately complex queries
        using sort, min, max, fromdate, and todate.\n \nThis method returns a list
        of questions."
      operationId: gets-the-questions-asked-by-the-users-in-ids-which-have-at-least-one-answer-but-no-accepted-answer-q
      x-api-path-slug: usersidsquestionsunaccepted-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Users
      - Unaccepted
  /users/{ids}/questions/unanswered:
    get:
      summary: Get User Questions Unanswered
      description: "Gets the questions asked by the users in {ids} which the site
        consideres unanswered, while still having at least one answer posted.\n \nThese
        rules are subject to change, but currently any question without at least one
        upvoted or accepted answer is considered unanswered.\n \nTo get the set of
        questions that a user probably considers unanswered, the returned questions
        should be unioned with those returned by /users/{id}/questions/no-answers.
        These methods are distinct so that truly unanswered (that is, zero posted
        answers) questions can be easily separated from mearly poorly or inadequately
        answered ones.\n \n{ids} can contain up to 100 semicolon delimited ids, to
        find ids programatically look for user_id on user or shallow_user objects.\n
        \nThe sorts accepted by this method operate on the follow fields of the question
        object:\n - activity - last_activity_date\n - creation - creation_date\n -
        votes - score\n  activity is the default sort.\n \n It is possible to create
        moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
        method returns a list of questions."
      operationId: gets-the-questions-asked-by-the-users-in-ids-which-the-site-consideres-unanswered-while-still-having
      x-api-path-slug: usersidsquestionsunanswered-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Users
      - Unanswerd
  /users/{ids}/reputation:
    get:
      summary: Get User Reputation
      description: "Gets a subset of the reputation changes for users in {ids}.\n
        \nReputation changes are intentionally scrubbed of some data to make it difficult
        to correlate votes on particular posts with user reputation changes. That
        being said, this method returns enough data for reasonable display of reputation
        trends.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids
        programatically look for user_id on user or shallow_user objects.\n \nThis
        method returns a list of reputation objects."
      operationId: gets-a-subset-of-the-reputation-changes-for-users-in-ids-reputation-changes-are-intentionally-scrubb
      x-api-path-slug: usersidsreputation-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Users
      - Reputation
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