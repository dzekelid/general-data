swagger: "2.0"
x-collection-name: Coord
x-complete: 1
info:
  title: Users API
  description: the-users-api-allows-you-to-manage-user-data-on-the-coord-platform--sending-user-data-to-coordallows-you-to-perform-transactions-with-mobility-systems-like-renting-a-bike-parking-ina-parking-lot-or-booking-a-ridehail-trip-on-behalf-of-that-user-using-the-coord-platform-the-requirements-for-performing-a-transaction-for-a-given-user-vary-depending-on-the-systemyoure-connecting-with--some-systems-require-particular-data-about-a-user-in-order-for-thetransaction-to-take-place-and-some-systems-require-you-to-link-a-users-account--alltransactions-require-you-to-authenticate-the-user-using-a-jwt-every-coord-api-that-supports-transactions-has-an-endpoint-for-getting-information-aboutthat-apis-systems-along-with-what-you-need-to-provide-for-a-user-in-order-to-perform-atransaction-for-them--the-users-api-provides-tools-that-help-you-enable-users-to-performtransactions-as-well-as-tools-for-learning-about-the-transactions-that-a-user-can-alreadyperform-read-on-for-more-information-about-authenticating-users-linking-accounts-and-managing-userdata--authenticating-users-with-jwtsall-coord-api-endpoints-that-either-manipulate-data-or-perform-a-transaction-on-behalf-of-alogged-in-user-require-http-calls-to-include-an-authorization-bearer-jwt-token-so-thatthe-current-user-can-be-identified--all-endpoints-in-the-users-api-fall-into-this-categoryexcept-for-the-test-jwt-creation-endpoint-which-is-designed-to-allow-you-to-create-test-tokensfor-use-in-such-requests-for-information-on-how-to-create-nontest-user-authorization-tokensplease-contact-a-hrefmailtosalescoord-co-target-blanksalescoord-coaas-this-is-available-only-for-transaction-enabled-partners-see-post-v1userstestinguser-and-jwtreference0testjwtcreation-for-information-onhow-to-create-jwts-for-testing--linking-accountsmany-systems-require-you-to-link-a-user-in-order-to-perform-a-transaction--you-can-do-this-byredirecting-the-users-browser-or-webview-to-theget-v1userslink-accountreference0linkauseraccounttoenabletransactions-endpoint-this-will-allow-the-user-to-link-to-an-existing-account-with-that-system-if-they-have-one-orwill-create-a-new-one-for-them--if-you-call-this-endpoint-with-a-test-jwt-we-will-simulateaccount-linking-by-redirecting-the-user-to-a-demo-permission-page-you-can-also-simulate-linking-or-unlinking-test-users-accounts-serverside-by-calling-thepost-v1userstestingusercurrenttransactable-systemsreference0simulateaccountlinkingfortestingendpoint-remember-that-not-all-systems-are-transactable-and-not-all-transactable-systems-requireaccount-linking--getting-and-setting-user-infowe-automatically-ingest-user-information-like-email-addresses-and-names-from-the-jwtauthorization-token-you-send-us--information-about-a-users-vehicle-like-their-license-plateneeds-to-be-set-through-our-api--we-require-this-in-order-for-the-user-to-transact-with-certainparking-operators-you-can-call-get-v1usersusercurrentreference0getuserinfo-to-get-all-theinformation-we-have-about-a-user-including-the-fields-we-deduce-from-their-jwt-and-those-thatyou-have-already-set-through-our-api-you-can-call-v1usersusercurrentupdate-vehiclereference0updateuservehicle-toupdate-the-vehicle-thats-associated-with-a-users-account-
  version: 1.0.0
host: api.coord.co
basePath: /v1/users
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /location:
    get:
      summary: Get a list of off-street parking locations.
      description: |-
        Find all of the locations within a given are and return their pricing information and
        (when present) availability. If the `duration_m` parameter is set, total cost for a stay
        of that duration will also be returned.
      operationId: get_locations
      x-api-path-slug: location-get
      parameters:
      - in: query
        name: access_key
        description: The API access key for the request
      - in: query
        name: duration_m
        description: The expected length of time, in minutes, that the car will remainparked
          for
      - in: query
        name: latitude
        description: Latitude to return results for
      - in: query
        name: location_ids
        description: Comma separated list of the location IDs to include in the search
      - in: query
        name: longitude
        description: Longitude to return results for
      - in: query
        name: parking_start_time
        description: The ISO-8601 formatted string representing the time when the
          vehicle will arrive atthe parking location
      - in: query
        name: radius_km
        description: Distance, in kilometers, from (latitude, longitude) we will returnresults
          for
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Off-street
      - Parking
      - Locations
  /location/{id}:
    get:
      summary: Get a list of off-street parking locations.
      description: |-
        Find a single locations within a given are and return their pricing information and
        (when present) availability. If the `duration_m` parameter is set, total cost for a stay
        of that duration will also be returned.
      operationId: get_location
      x-api-path-slug: locationid-get
      parameters:
      - in: query
        name: access_key
        description: The API access key for the request
      - in: query
        name: duration_m
        description: The expected length of time, in minutes, that the car will remainparked
          for
      - in: path
        name: id
        description: The ID of the parking location to retrieve
      - in: query
        name: parking_start_time
        description: The ISO-8601 formatted string representing the time when the
          vehicle will arrive atthe parking location
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Off-street
      - Parking
      - Locations