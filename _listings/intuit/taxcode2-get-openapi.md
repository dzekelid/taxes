---
swagger: "2.0"
x-collection-name: Intuit
x-complete: 0
info:
  title: QuickBooks Online V3 API Get Tax Code
  description: |-
    Read a taxcode by Id
    Method : POST
  version: 1.0.0
host: DefaultParameterValue
basePath: /v3/company/DefaultParameterValue
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /taxservice/taxcode:
    post:
      summary: Post Tax Service Tax Code
      description: |-
        Use TaxService to create taxcode and corresponding taxrates
        Method : POST
      operationId: postTaxserviceTaxcode
      x-api-path-slug: taxservicetaxcode-post
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: query
        name: minorversion
      - in: header
        name: User-Agent
      responses:
        200:
          description: OK
      tags:
      - Accounting
      - Accounting
      - Tax
      - Service
      - Tax
      - Code
  /taxagency/3:
    get:
      summary: Get Tax Agency
      description: |-
        Get a tax-agency object by ID
        Method : GET
      operationId: getTaxagency3
      x-api-path-slug: taxagency3-get
      parameters:
      - in: header
        name: Accept
      - in: query
        name: minorversion
      - in: header
        name: User-Agent
      responses:
        200:
          description: OK
      tags:
      - Accounting
      - Accounting
      - Tax
      - Agency
  /taxrate/1:
    get:
      summary: Get Tax Rate
      description: |-
        Read a taxRate by Id
        Method : POST
      operationId: getTaxrate1
      x-api-path-slug: taxrate1-get
      parameters:
      - in: header
        name: Accept
      - in: query
        name: minorversion
      - in: header
        name: User-Agent
      responses:
        200:
          description: OK
      tags:
      - Accounting
      - Accounting
      - Tax
      - Rate
  /taxcode/2:
    get:
      summary: Get Tax Code
      description: |-
        Read a taxcode by Id
        Method : POST
      operationId: getTaxcode2
      x-api-path-slug: taxcode2-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: query
        name: minorversion
      - in: header
        name: User-Agent
      responses:
        200:
          description: OK
      tags:
      - Accounting
      - Accounting
      - Tax
      - Code
  /taxagency:
    post:
      summary: Post Taxagency
      description: |-
        Create a tax-agency object
        Method : POST

        Sample response payload

        {
          "SalesReceipt": {
            "domain": "QBO",
            "status": "Deleted",
            "Id": "181"
          },
          "time": "2016-09-02T02:17:24.353-07:00"
        }
      operationId: postTaxagency
      x-api-path-slug: taxagency-post
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: query
        name: minorversion
      - in: header
        name: User-Agent
      responses:
        200:
          description: OK
      tags:
      - Accounting
      - Accounting
      - Taxagency
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