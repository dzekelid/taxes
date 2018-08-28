---
swagger: "2.0"
x-collection-name: Paylocity
x-complete: 0
info:
  title: Paylocity Delete local tax by tax code
  description: Delete local tax by tax code
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
  /v2/companies/{companyId}/employees/{employeeId}/localTaxes/{taxCode}:
    delete:
      summary: Delete local tax by tax code
      description: Delete local tax by tax code
      operationId: v2.companies.companyId.employees.employeeId.localTaxes.taxCode.delete
      x-api-path-slug: v2companiescompanyidemployeesemployeeidlocaltaxestaxcode-delete
      parameters:
      - in: header
        name: Authorization
        description: Bearer + JWT
      - in: path
        name: companyId
        description: Company Id
      - in: path
        name: employeeId
        description: Employee Id
      - in: path
        name: taxCode
        description: Tax Code
      responses:
        200:
          description: OK
      tags:
      - V2
      - Companies
      - CompanyId
      - Employees
      - EmployeeId
      - LocalTaxes
      - TaxCode
    get:
      summary: Get local taxes by tax code
      description: Returns all local taxes with the provided tax code for the selected
        employee.
      operationId: v2.companies.companyId.employees.employeeId.localTaxes.taxCode.get
      x-api-path-slug: v2companiescompanyidemployeesemployeeidlocaltaxestaxcode-get
      parameters:
      - in: header
        name: Authorization
        description: Bearer + JWT
      - in: path
        name: companyId
        description: Company Id
      - in: path
        name: employeeId
        description: Employee Id
      - in: path
        name: taxCode
        description: Tax Code
      responses:
        200:
          description: OK
      tags:
      - V2
      - Companies
      - CompanyId
      - Employees
      - EmployeeId
      - LocalTaxes
      - TaxCode
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