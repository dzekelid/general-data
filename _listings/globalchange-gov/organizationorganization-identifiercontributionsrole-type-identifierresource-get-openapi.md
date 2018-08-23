---
swagger: "2.0"
x-collection-name: GlobalChange.gov
x-complete: 0
info:
  title: Global Change Information System API Show contributions of a certain type
    by an organization
  description: Given a resource (dataset, report, etc.) and a role (editor, etc),
    and an identifier for an organization, show the resources to which the organization
    has contributed in that role.
  version: v1
host: data.globalchange.gov
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /organization/{organization_identifier}:
    get:
      summary: Get a representation of an organization.
      description: Get JSON which represents the structure of an organization.
      operationId: get-json-which-represents-the-structure-of-an-organization
      x-api-path-slug: organizationorganization-identifier-get
      parameters:
      - in: path
        name: organization_identifier
        description: organization_identifier description
      responses:
        200:
          description: OK
      tags:
      - Representation
      - Organization
  /organization/{organization_identifier}/contributions/{role_type_identifier}/{resource}:
    get:
      summary: Show contributions of a certain type by an organization
      description: Given a resource (dataset, report, etc.) and a role (editor, etc),
        and an identifier for an organization, show the resources to which the organization
        has contributed in that role.
      operationId: given-a-resource-dataset-report-etc-and-a-role-editor-etc-and-an-identifier-for-an-organization-show
      x-api-path-slug: organizationorganization-identifiercontributionsrole-type-identifierresource-get
      parameters:
      - in: path
        name: organization_identifier
        description: organization_identifier description
      - in: path
        name: resource
        description: resource description
      - in: path
        name: role_type_identifier
        description: role_type_identifier description
      responses:
        200:
          description: OK
      tags:
      - Show
      - Contributions
      - Certain
      - Type
      - By
      - Organization
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