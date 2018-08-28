swagger: "2.0"
x-collection-name: School Digger
x-complete: 1
info:
  title: School Digger API V1
  description: get-detailed-data-on-over-120000-schools-and-18500-districts-in-the-u-s-
  termsOfService: https://developer.schooldigger.com/termsofservice
  contact:
    name: SchoolDigger
    email: api@schooldigger.com
  version: v1
host: api.schooldigger.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/rankings/districts/{st}:
    get:
      summary: Returns a SchoolDigger district ranking list
      description: ""
      operationId: v1.rankings.districts.st.get
      x-api-path-slug: v1rankingsdistrictsst-get
      parameters:
      - in: query
        name: appID
        description: Your API app id
      - in: query
        name: appKey
        description: Your API app key
      - in: query
        name: page
        description: 'Page number to retrieve (optional, default: 1)'
      - in: query
        name: perPage
        description: 'Number of districts to retrieve on a page (50 max) (optional,
          default: 10)'
      - in: path
        name: st
        description: Two character state (e
      - in: query
        name: year
        description: The ranking year (leave blank for most recent year)
      responses:
        200:
          description: OK
      tags:
      - ""