---
swagger: "2.0"
x-collection-name: GitHub
x-complete: 0
info:
  title: Github Get Orgs Org Public Members
  description: |-
    Public members list.
    Members of an organization can choose to have their membership publicized
    or not.
  termsOfService: https://help.github.com/articles/github-terms-of-service/#b-api-terms
  version: 1.0.0
host: api.github.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /orgs/{org}:
    get:
      summary: Get Orgs Org
      description: Get an Organization.
      operationId: get-an-organization
      x-api-path-slug: orgsorg-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: org
        description: Name of organisation
      responses:
        200:
          description: OK
      tags:
      - Orgs
      - Org
  /orgs/{org}/events:
    get:
      summary: Get Orgs Org Events
      description: List public events for an organization.
      operationId: list-public-events-for-an-organization
      x-api-path-slug: orgsorgevents-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: org
        description: Name of organisation
      responses:
        200:
          description: OK
      tags:
      - Orgs
      - Org
      - Events
  /orgs/{org}/issues:
    get:
      summary: Get Orgs Org Issues
      description: |-
        List issues.
        List all issues for a given organization for the authenticated user.
      operationId: list-issueslist-all-issues-for-a-given-organization-for-the-authenticated-user
      x-api-path-slug: orgsorgissues-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: query
        name: direction
      - in: query
        name: filter
        description: Issues assigned to you / created by you / mentioning you / youresubscribed
          to updates for / All issues the authenticated user can see
      - in: query
        name: labels
        description: String list of comma separated Label names
      - in: path
        name: org
        description: Name of organisation
      - in: query
        name: since
        description: 'Optional string of a timestamp in ISO 8601 format: YYYY-MM-DDTHH:MM:SSZ'
      - in: query
        name: sort
      - in: query
        name: state
      responses:
        200:
          description: OK
      tags:
      - Orgs
      - Org
      - Issues
  /orgs/{org}/members:
    get:
      summary: Get Orgs Org Members
      description: |-
        Members list.
        List all users who are members of an organization. A member is a user tha
        belongs to at least 1 team in the organization. If the authenticated user
        is also an owner of this organization then both concealed and public members
        will be returned. If the requester is not an owner of the organization the
        query will be redirected to the public members list.
      operationId: members-listlist-all-users-who-are-members-of-an-organization-a-member-is-a-user-thabelongs-to-at-le
      x-api-path-slug: orgsorgmembers-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: org
        description: Name of organisation
      responses:
        200:
          description: OK
      tags:
      - Orgs
      - Org
      - Members
  /orgs/{org}/members/{username}:
    get:
      summary: Get Orgs Org Members Username
      description: Check if a user is, publicly or privately, a member of the organization.
      operationId: check-if-a-user-is-publicly-or-privately-a-member-of-the-organization
      x-api-path-slug: orgsorgmembersusername-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: org
        description: Name of organisation
      - in: path
        name: username
        description: Name of the user
      responses:
        200:
          description: OK
      tags:
      - Orgs
      - Org
      - Members
      - Username
  /orgs/{org}/public_members:
    get:
      summary: Get Orgs Org Public Members
      description: |-
        Public members list.
        Members of an organization can choose to have their membership publicized
        or not.
      operationId: public-members-listmembers-of-an-organization-can-choose-to-have-their-membership-publicizedor-not
      x-api-path-slug: orgsorgpublic-members-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: org
        description: Name of organisation
      responses:
        200:
          description: OK
      tags:
      - Orgs
      - Org
      - Public
      - Members
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