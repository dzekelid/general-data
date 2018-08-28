swagger: "2.0"
x-collection-name: Rite Kit
x-complete: 1
info:
  title: Rite Kit
  description: ritekit-api-is-based-on-rest-principles-authentication-uses-standard-oauth-2-0-processgetting-started1--sign-up-for-ritekithttpsritekit-com1--go-to-developer-dashboardhttpsritekit-comdeveloperdashboard1--click-create-a-token-button-to-get-your-client-id-and-client-secret1--study-the-documentation-below-for-more-info-on-oauth-go-to-httpoauth-net1--when-you-reach-your-free-limit-of-calls-per-month-upgrade-to-paid-tiershttpsritekit-comdeveloper-options-for-authorizing-api-calls-a-using-client-id-directlyyou-can-directly-connect-to-our-api-using-your-client-id-by-sending-it-as-a-get-query-parameter--this-option-is-simple-no-need-for-oauth-but-it-should-be-used-only-in-case-the-client-id-is-not-exposed-publicly-get--httpsapi-ritekit-comv1statsmultiplehashtagstagsphpclient-id292c6912e7710c838347ae178b4a-b-using-access-token-oauth-2-0once-you-have-valid-access-token-you-can-access-our-api-by-sending-the-token-in-the-authorization-header-bearer-or-as-a-query-access-token--see-the-oauth-2-0-section-to-learn-how-to-get-access-token-and-keep-refreshing-it-authorization-bearer-xxxxorget--httpsapi-ritekit-comv1statsmultiplehashtagstagsphpaccess-token292c6912e7710c838347ae178b4a-oauth-2-0oauthschemahttpscdn-ritekit-comassetsmedia1oauthsimple-png-get-access-tokenuse-your-client-credentials-to-get-the-token-post---httpsritekit-comoauthtoken-----------grant-typeclient-credentials-----------client-idclient-id-----------client-secretclient-secret-----------scopedata-required-grant-type--client-credentials-required-client-id-client-id-required-client-secret-client-secret-required-always-use-scopedata-response--------access-token292c6912e7710c838347ae178b4a--------token-typebearer--------expires-in-3600--------refresh-token292c6912e7710c838347ae178b4a-----refresh-tokenevery-access-token-has-a-lifetime--you-can-use-refresh-token-to-request-a-new-access-token-post---httpsritekit-comoauthtoken-----------grant-typerefresh-token-----------refresh-tokenrefresh-token-----------client-idclient-id-----------scopedata-required-grant-type--refresh-token-required-refresh-token--refresh-token-the-refresh-token-you-got-from-the-expired-token-required-client-id-client-id-required-client-secret-client-secret-required-scope-always-use-scopedata-response--------access-token292c6912e7710c838347ae178b4a--------token-typebearer--------expires-in-3600--------refresh-token292c6912e7710c838347ae178b4a----
  version: 1.0.0
host: api.ritekit.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json