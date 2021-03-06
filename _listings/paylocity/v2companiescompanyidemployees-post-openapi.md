---
swagger: "2.0"
x-collection-name: Paylocity
x-complete: 0
info:
  title: Paylocity Add new employee
  description: New Employee API sends new employee data directly to Web Pay. Companies
    who use the New Hire Template in Web Pay may require additional fields when hiring
    employees. New Employee API Requests will honor these required fields.
  termsOfService: WebLink.OpenApiDoc.TermsOfService
  version: "2"
host: api.paylocity.com
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v2/companies/{companyId}/employees:
    post:
      summary: Add new employee
      description: New Employee API sends new employee data directly to Web Pay. Companies
        who use the New Hire Template in Web Pay may require additional fields when
        hiring employees. New Employee API Requests will honor these required fields.
      operationId: v2.companies.companyId.employees.post
      x-api-path-slug: v2companiescompanyidemployees-post
      parameters:
      - in: header
        name: Authorization
        description: Bearer + JWT
      - in: path
        name: companyId
        description: Company Id
      - in: body
        name: json
        description: Employee Model
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - V2
      - Companies
      - CompanyId
      - Employees
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