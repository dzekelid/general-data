swagger: "2.0"
x-collection-name: Ship Station
x-complete: 1
info:
  title: Ship Station Developer Portal
  description: -integrating-with-shipstationshipstation-strives-to-streamline-shipping-for-online-sellers-no-matter-where-they-sell-their-products-online--we-are-continuously-adding-new-marketplaces-shopping-carts-and-integration-tools-because-we-know-the-ecommerce-space-is-growing--as-a-result-weve-worked-hard-to-provide-developer-resources-to-build-custom-integrations-with-shipstation---if-youre-interested-in-becoming-a-partner-of-ours-drop-us-a-line-by-filling-out-this-formhttpwww-shipstation-compartnersshipstationapicustomstore-and-well-get-in-touch-there-are-two-methods-to-integrate-with-shipstation-custom-store-integration-shipstation-api-custom-store-integrationlooking-for-a-more-1to1-relationship-between-shipstation-and-your-chosen-selling-platform-the-custom-store-integration-is-the-ticket--our-custom-store-integration-is-just-like-any-of-our-other-selling-channel-integration-and-could-be-eligible-based-on-internal-review-as-a-branded-option-within-the-shipstation-admin--it-also-allows-the-user-to-sync-orders-within-shipstation-in-a-single-click-in-addition-to-shipstation-automatically-sending-shipment-status-and-tracking-information-updates-back-to-your-cart-or-marketplace-once-a-label-is-created--its-the-best-way-to-sync-up-orders-with-shipstation-and-have-the-most-seamless-experience-the-custom-store-allows-you-to-perform-two-major-functions-provide-order-information-to-shipstation-including-recipient-address-products-customers-etc--receive-tracking-information-when-an-order-is-shipped-including-shipping-method-shipping-status-tracking-number-and-moreto-integrate-with-the-custom-store-you-must-expose-a-web-page-that-renders-xml-that-adheres-to-the-specification-defined-in-the-custom-store-integration-guide--we-refer-to-this-page-as-your-xml-endpoint--if-you-can-provide-us-an-xml-endpoint-we-can-pull-data-from-your-endpoint-just-like-we-do-with-other-marketplaces-like-ebay-and-amazon-to-find-out-more-about-our-custom-store-integration-click-here-custom-store-integration-guidehttpshelp-shipstation-comhcenusarticles205928478-shipstation-apiour-api-is-available-for-any-plan-and-allows-for-read-access-to-almost-all-data-in-your-account-and-write-access-to-create-specific-objects-like-orders-customers-and-products--the-api-is-a-great-way-to-get-data-directly-to-and-from-shipstation-like-creating-products-customers-and-querying-order--shipping-data--please-note-that-an-api-integration-will-not-allow-you-to-use-your-own-marketplaceid-that-could-eventually-be-branded-with-your-companys-logo-see-the-custom-store-integration-above-for-that-functionality-this-api-allows-developers-to-build-applications-that-interface-with-the-shipstation-platform--the-api-can-be-used-to-automate-many-tasks-including-managing-orders-managing-shipments-creating-shipping-labels-retrieving-shipping-rates-and-moreto-learn-more-about-our-api-please-review-our-api-documentation-below--which-one-should-i-pickthe-method-thats-right-for-your-integration-very-much-depends-on-the-type-of-integration-youre-planning-on-implementing--a-custom-store-allows-shipstation-to-pull-order-information-from-your-platform-the-very-same-way-we-pull-data-from-marketplaces-such-as-ebay-amazon-and-shopify--once-an-order-has-been-shipped-in-shipstation-shipstation-automatically-pushes-tracking-information-back-to-your-custom-store--though-the-functionality-afforded-by-this-approach-is-limited-to-these-2-main-functions-much-of-the-heavy-lifting-is-performed-by-shipstation--importing-orders-and-sending-tracking-information-is-performed-automatically-by-shipstation-as-long-as-your-xml-endpoint-is-available-to-receive-our-data-an-api-integration-on-the-other-hand-exposes-much-more-functionality-but-requires-that-the-developer-do-much-of-the-heavy-lifting--orders-must-be-pushed-to-shipstation-by-using-our-orderscreateorder-endpoint---the-api-allows-developers-to-perform-functions-such-as-tagging-an-order-shipping-an-order-creating-a-shipping-label-without-an-order-retrieving-shipping-rates-adding-funds-to-a-carrier-account-creating-a-warehouse-listing-products-and-much-more---the-functionality-the-api-affords-are-typical-actions-that-a-user-would-perform-if-using-the-web-app--considerations-will-your-integration-be-the-main-order-management-tool-for-the-online-seller--if-so-the-apis-broader-range-of-functionality-may-be-the-best-option--would-you-like-your-store-integration-to-be-a-branded-marketplace-within-the-shipstation-admin-when-you-integrate-using-the-custom-store-integration-you-could-be-eligible-to-have-your-company-branded-within-the-shipstation-admin--a-branded-store-could-have-the-plugins-logo-in-the-appas-well-as-an-easier-store-setup-order-sync-and-reporting--please-note-shipstation-makes-the-final-decision-based-on-integration-and-partner-requirements-on-which-custom-stores-are-branded-within-our-application--shipstation-api-requirements-end-pointendpoints-are-located-at-the-following-domain-httpsssapi-shipstation-com-and-will-need-to-have-a-specific-reference-added-to-return-data--please-note-you-cannot-access-this-url-directly-and-must-reference-one-of-the-specific-endpoints-below--authenticationthe-shipstation-api-uses-basic-http-authenticationhttpen-wikipedia-orgwikibasic-access-authentication--use-your-shipstation-api-key-as-the-username-and-api-secret-as-the-password---you-can-find-your-api-key-as-the-username-and-api-secret-under-settings-at-httpsss-shipstation-comsettingsapi--the-authorization-header-is-constructed-as-follows-username-api-key-and-password-api-secret-are-combined-into-a-string-usernamepassword-the-resulting-string-is-then-encoded-using-the-rfc2045mime-variant-of-base64-except-not-limited-to-76-charline-the-authorization-method-and-a-space-i-e--basic--is-then-put-before-the-encoded-string-for-example-if-the-api-key-given-is-shipstation-and-the-api-secret-is-rocks-then-the-header-is-formed-as-follows-authorization-basic-u2hpcfn0yxrpb246um9ja3m-api-rate-limitsin-an-effort-to-ensure-consistent-application-performance-and-increased-scalability-we-have-implemented-rate-limiting-on-the-shipstation-api---your-integration-will-need-to-be-able-to-handle-http-rate-limiting-status-messages-as-defined-belowresponse-headersall-responses-will-include-headers-with-status-information-about-rate-limiting-1--xratelimitlimit-the-maximum-number-of-requests-per-minute-to-the-endpoint2--xratelimitremaining-the-available-requests-remaining-in-the-current-window3--xratelimitreset-the-number-of-seconds-remaining-until-the-next-window-beginshitting-the-limitif-your-application-hits-the-rate-limit-an-http-429-will-be-returned-with-this-body----message-too-many-requestsand-these-headers-assuming-it-is-40-seconds-into-the-current-window----xratelimitlimit-60----xratelimitremaining-0----xratelimitreset-20when-the-limit-is-reached-your-application-should-stop-making-requests-until-xratelimitreset-seconds-have-elapsed--the-current-rate-limit-for-each-set-of-the-api-key-and-secret-is-40-requests-per-minute-if-you-have-any-issues-with-the-api-please-email-us-at-apisupportshipstation-com-server-responsesstatus-code--description200--ok--the-request-was-successful-some-api-calls-may-return-201-instead-201--created--the-request-was-successful-and-a-resource-was-created-204--no-content--the-request-was-successful-but-there-is-no-representation-to-return-that-is-the-response-is-empty-400--bad-request---the-request-could-not-be-understood-or-was-missing-required-parameters-401--unauthorized---authentication-failed-or-user-does-not-have-permissions-for-the-requested-operation-403--forbidden--access-denied-404--not-found---resource-was-not-found-405--method-not-allowed---requested-method-is-not-supported-for-the-specified-resource-429--too-many-requests--exceeded-shipstation-api-limits--when-the-limit-is-reached-your-application-should-stop-making-requests-until-xratelimitreset-seconds-have-elapsed-500--internal-server-error--shipstation-has-encountered-an-error--datetime-format-and-time-zoneshipstation-uses-the-iso-8601-combined-format-for-datetime-stamps-being-submitted-to-and-returned-from-the-api--please-be-sure-to-submit-all-datetime-values-as-followsyyyymmdd-hhmmss-24-hour-notation--example--20161129-235959the-time-zone-represented-in-all-api-responses-is-pstpdt--similarly-shipstation-asks-that-you-make-all-time-zone-convertions-and-submit-any-datetime-requests-in-pstpdt-
  version: 1.0.0
host: ssapi.shipstation.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? /fulfillments?fulfillmentId={fulfillmentId}&orderId={orderId}&orderNumber={orderNumber}&trackingNumber={trackingNumber}&recipientName={recipientName}&createDateStart={createDateStart}&createDateEnd={createDateEnd}&shipDateStart={shipDateStart}&shipDa
  : get:
      summary: List Fulfillments with parameters
      description: |-
        Obtains a list of fulfillments that match the specified criteria.  Please note the following:

        - Orders that have been marked as shipped either through the UI or the API will appear in the response as they are considered fulfillments.

        All of the available filters are optional.  They do not need to be included in the URL.  If you do include them, here's what the URL may look like:

        Url format with filters:

        ```
        fulfillments?fulfillmentId={fulfillmentId}
        &orderId={orderId}
        &orderNumber={orderNumber}
        &trackingNumber={trackingNumber}
        &recipientName={recipientName}
        &createDateStart={createDateStart}
        &createDateEnd={createDateEnd}
        &shipDateStart={shipDateStart}
        &shipDateEnd={shipDateEnd}
        &sortBy={sortBy}
        &sortDir={sortDir}
        &page={page}
        &pageSize={pageSize}
        ```
      operationId: fulfillments_fulfillmentId_fulfillmentId_orderId_orderId_orderNumber_orderNumber_trackingNumber_trac
      x-api-path-slug: fulfillmentsfulfillmentidfulfillmentidorderidorderidordernumberordernumbertrackingnumbertrackingnumberrecipientnamerecipientnamecreatedatestartcreatedatestartcreatedateendcreatedateendshipdatestartshipdatestartshipda-get
      parameters:
      - in: path
        name: createDateEnd
        description: Returns fulfillments created on or before the specified ``createDate``
      - in: path
        name: createDateStart
        description: Returns fulfillments created on or after the specified ``createDate``
      - in: path
        name: fulfillmentId
        description: Returns the fulfillment with the specified fulfillment ID
      - in: path
        name: orderId
        description: Returns fulfillments whose orders have the specified order ID
      - in: path
        name: orderNumber
        description: Returns fulfillments whose orders have the specified order number
      - in: path
        name: page
        description: page number
      - in: path
        name: pageSize
        description: page size
      - in: path
        name: recipientName
        description: Returns fulfillments shipped to the specified recipient name
      - in: path
        name: shipDateEnd
        description: Returns fulfillments with the ``shipDate`` on or before the specified
          date
      - in: path
        name: shipDateStart
        description: Returns fulfillments with the ``shipDate`` on or after the specified
          date
      - in: path
        name: sortBy
        description: Sort the responses by a set value
      - in: path
        name: sortDir
        description: Sets the direction of the sort order
      - in: path
        name: trackingNumber
        description: Returns fulfillments with the specified tracking number
      responses:
        200:
          description: OK
      tags:
      - List
      - Fulfillments
      - Parameters
  ? /products?sku={sku}&name={name}&productCategoryId={productCategoryId}&productTypeId={productTypeId}&tagId={tagId}&startDate={startDate}&endDate={endDate}&showInactive={showInactive}&sortBy={sortBy}&sortDir={sortDir}&page={page}&pageSize={pageSize}
  : get:
      summary: List Products with parameters
      description: |-
        Obtains a list of products that match the specified criteria.  All of the available filters are optional.  They do not need to be included in the URL.  If you do include them, here's what the URL may look like:

        Url format with filters:

        ```
        /products?sku={sku}
        &name={name}
        &productCategoryId={productCategoryId}
        &productTypeId={productTypeId}
        &tagId={tagId}
        &startDate={startDate}
        &endDate={endDate}
        &showInactive={showInactive}
        &sortBy={sortBy}
        &sortDir={sortDir}
        &page={page}
        &pageSize={pageSize}
        ```
      operationId: products_sku_sku_name_name_productCategoryId_productCategoryId_productTypeId_productTypeId_tagId_tag
      x-api-path-slug: productsskuskunamenameproductcategoryidproductcategoryidproducttypeidproducttypeidtagidtagidstartdatestartdateenddateenddateshowinactiveshowinactivesortbysortbysortdirsortdirpagepagepagesizepagesize-get
      parameters:
      - in: path
        name: endDate
        description: Returns products that were created before the specified date
      - in: path
        name: name
        description: Returns products that match the specified product name
      - in: path
        name: page
        description: Page number
      - in: path
        name: pageSize
        description: Requested page size
      - in: path
        name: productCategoryId
        description: Returns products that match the specified productCategoryId
      - in: path
        name: productTypeId
        description: Returns products that match the specified productTypeId
      - in: path
        name: showInactive
        description: Specifies whether the list should include inactive products
      - in: path
        name: sku
        description: Returns products that match the specified SKU
      - in: path
        name: sortBy
        description: Sorts the order of the response based off the specified value
      - in: path
        name: sortDir
        description: Sets the direction of the sort order
      - in: path
        name: startDate
        description: Returns products that were created after the specified date
      - in: path
        name: tagId
        description: Returns products that match the specified tagId
      responses:
        200:
          description: OK
      tags:
      - List
      - Products
      - Parameters