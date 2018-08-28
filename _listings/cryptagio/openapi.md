swagger: "2.0"
x-collection-name: Cryptagio
x-complete: 1
info:
  title: Cryptagio API
  description: -public--private-methodstable--thead--tr-----td-bpublic-methodsb-td----td-bprivate-methodsb-td--tr--thead--tr-----td-no-authorization-required-td----td-authorization-required-td--trtable-authorization--to-use-private-methods-you-need-to-get-your-accesssecret-key-first-on-cryptagio-comhttpscryptagio-com--after-signed-up-and-verified-visit-api-tokens-page-to-get-your-keys----p-all-requests-to-the-private-methods-require-these-headershr--table--tr-----td-bxpublickeyb-td----td-your-access-key-td--tr--tr-----td-bxtonceb-td----td-tonce-is-a-timestamp-in-integer-stands-for-microseconds-elapsed-since-unix-epoch--tonce-must-be-within-30-seconds-of-servers-current-time--each-tonce-can-only-be-used-once-td--tr--tr-----td-bxsignatureb-td----td-signature-of-the-api-request-generated-by-you-use-your-secret-key-td--tr--table--hr----signaturefor-signature-use-ed25519httped25519-cr-yp-to--sign-the-message-using-your-secret-key-and-return-a-signed-message-----signature--signmessage-secret-key-message-is-a-combination-of-requestbody-uri-and-tonce-string----message--requestbodyuritonce--table--tr-----td-irequestbodyi-td----td-requestbody-in-the-json-format--required-only-for-post-methods-td--tr--tr-----td-iurii-td----td-request-path-like-ordersmylimit50orderdesc-td--tr--tr-----td-itonce-i-td----td-timestamp-in-integer-stands-for-microseconds-elapsed-since-unix-epoch-td--tr--tablemessage-examples-p-post-message-marketethbtcsidebidamount1price0-07typelimitorders1531816217872000000-p-get-message-ordersmylimit50orderdesc1531816217872000000hr--examplesp-curl-x-post-httpsapi-cryptagio-comorders-h-accept-applicationjson-h-xtonce-1531816217872000000-h-xsignature-signature-h-xpublickey-your-access-key-h-contenttype-applicationjson-d-marketbtcethsidebidamount1price0-07typelimit-p-curl-x-get-httpsapi-cryptagio-comordersmylimit50orderdesc-h-accept-applicationjson-h-xtonce-1531816217872000000-h-xsignature-signature-h-xpublickey-your-access-key
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json