---
name: Geneea
x-slug: geneea
description: Geneea helps you analyze large amounts of text. Whether it is Facebook,
  blogs, e-mails or legal documents in your archives. Within seconds.     Dont change
  your business processes. Simply plug in the output of The Interpretor, our powerful
  software p...
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/geneea-logo.png
x-kinRank: "7"
x-alexaRank: "11275166"
tags: General Data
created: "2018-08-23"
modified: "2018-08-23"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/geneea/apis.md
specificationVersion: "0.14"
apis:
- name: Geneea Natural Language Processing
  x-api-slug: geneea-natural-language-processing
  description: div-classapidescription----h2authenticationh2----pfor-all-calls-supply-your-api-key--a-hrefhttpswww-geneea-compricingsign-up-to-emobtain-the-keyema-p----p--------our-api-supports-both-emunencrypted-httpem-and-emencrypted-httpsem-protocols---------however-for-security-reasons-we-strongly-encourage-using-only-the-encrypted-version-----p----pthe-api-key-should-be-supplied-as-either-a-request-parameter-codeuser-keycode-or-in-codeauthorizationcode-header-p----precodeauthorization-user-key-ltyour-api-keygtcodepre----h2api-operationsh2----p--------all-api-operations-can-perform-analysis-on-supplied-raw-text-or-on-text-extracted-from-a-given-url---------optionally-one-can-supply-additional-information-which-can-make-the-result-more-precise--an-example--------of-such-information-would-be-the-language-of-text-or-a-particular-text-extractor-for-url-resources-----p----pthe-supported-types-of-analyses-arep----ul--------listronglemmatizationstrong-longrightarrow------------finds-out-lemmata-basic-forms-of-all-the-words-in-the-document---------li--------listrongcorrectionstrong-longrightarrow------------performs-correction-diacritization-on-all-the-words-in-the-document---------li--------listrongtopic-detectionstrong-longrightarrow------------determines-a-topic-of-the-document-e-g--finance-or-sports---------li--------listrongsentiment-analysisstrong-longrightarrow------------determines-a-sentiment-of-the-document-i-e--how-positive-or-negative-the-document-is---------li--------listrongnamed-entity-recognitionstrong-longrightarrow------------finds-named-entities-like-person-location-date-etc--mentioned-the-the-document---------li----ul----h2encodingh2----pthe-supplied-text-is-expected-to-be-in-utf8-encoding-this-is-especially-important-for-nonenglish-texts-p----h2returned-valuesh2----pthe-api-calls-always-return-objects-in-serialized-json-format-in-utf8-encoding-p----p--------if-any-error-occurs-the-http-response-code-will-be-in-the-range-code4xxcode-clientside-error-or--------code5xxcode-serverside-error--in-this-situation-the-body-of-the-response-will-contain-information--------about-the-error-in-json-format-with-codeexceptioncode-and-codemessagecode-values-----p----h2url-limitationsh2----p--------all-the-requests-are-semantically-codegetcode--however-for-longer-texts-you-may-run-into-issues--------with-url-length-limit--therefore-its-possible-to-always-issue-a-codepostcode-request-with-all--------the-parameters-encoded-as-a-json-in-the-request-body-----p----pexamplep----precode--------post-s1sentiment--------contenttype-applicationjson--------textthere-is-no-harm-in-being-sometimes-wrong--especially-if-one-is-promptly-found-out-----codepre----pthis-is-equivalent-to-codeget-s1sentimenttextthere20is20no20harm---codep----h2request-limitationsh2----p--------the-api-has-other-limitations-concerning-the-size-of-the-http-requests--the-maximum-allowed-size-of-any--------post-request-body-is-em512-kibem--for-request-with-a-url-resource-the-maximum-allowed-number-of--------extracted-characters-from-each-such-resource-is-em100000em-----p----h2more-informationh2----p--------a-hrefhttpsgeneea-atlassian-netwikidisplayipdtheinterpretorapipublicdocumentation-target-blank--------the-interpretor-public-documentation--------a----pdiv
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/geneea-logo.png
  humanURL: https://www.geneea.com
  baseURL: https://api.geneea.com//
  tags: SaaS, Technology, API Provider, Machine Learning, Sentiment Analysis, Topic
    Identification, Tags, Tags, Languages, Entities, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/geneea/s1entities-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/geneea/s1entities-get-openapi.md
- name: Geneea Natural Language Processing
  x-api-slug: geneea-natural-language-processing
  description: Geneea helps you analyze large amounts of text. Whether it is Facebook,
    blogs, e-mails or legal documents in your archives. Within seconds.     Dont change
    your business processes. Simply plug in the output of The Interpretor, our powerful
    software p...
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/geneea-logo.png
  humanURL: https://www.geneea.com
  baseURL: https://api.geneea.com//
  tags: General Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/general-data/master/_listings/geneea/openapi.md
x-common:
- type: x-website
  url: https://www.geneea.com
- type: x-api-gallery
  url: http://ge.tt.api.gallery.streamdata.io
- type: x-api-stack
  url: http://geneea.stack.network
- type: x-crunchbase
  url: https://crunchbase.com/organization/geneea
- type: x-email
  url: info@geneea.com
- type: x-github
  url: https://github.com/Geneea
- type: x-twitter
  url: https://twitter.com/GeneeaAnalytics
- type: x-website
  url: http://geneea.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---