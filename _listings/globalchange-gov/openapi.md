swagger: "2.0"
x-collection-name: GlobalChange.gov
x-complete: 1
info:
  title: Global Change Information System API
  description: who-we-are-what-the-gcis-is-and-how-we-use-identifiers-and-semantic-information-to-provide-points-of-reference-and-traceability--examples-and-tutorials-for-using-this-system-as-a-researcher-citizen-scientist-application-developer-or-information-theorist--a-description-of-how-the-information-is-structured-including-the-overlaps-between-relational-and-semantic-representations-of-the-information--complete-documentation-for-the-api-including-methods-for-browsing-and-finding-resources-
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