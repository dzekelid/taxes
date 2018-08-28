---
swagger: "2.0"
x-collection-name: Xero
x-complete: 0
info:
  title: Clarity Accounting Put Taxrates
  description: Put taxrates.
  contact:
    name: Xero Developer Team
    url: https://developer.xero.com
  version: "2.0"
host: api.xero.com
basePath: /api.xro/2.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /TaxRates:
    get:
      summary: Get Taxrates
      description: Get taxrates.
      operationId: getTaxrates
      x-api-path-slug: taxrates-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - TaxRates
    post:
      summary: Post Taxrates
      description: Post taxrates.
      operationId: postTaxrates
      x-api-path-slug: taxrates-post
      parameters:
      - in: query
        name: No Name
      - in: body
        name: TaxRates
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - TaxRates
    put:
      summary: Put Taxrates
      description: Put taxrates.
      operationId: putTaxrates
      x-api-path-slug: taxrates-put
      parameters:
      - in: query
        name: No Name
      - in: body
        name: TaxRates
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - TaxRates
    x-related-model:
      summary: X-related-model Taxrates
      description: X-related-model taxrates.
      operationId: x-related-modelTaxrates
      x-api-path-slug: taxrates-xrelatedmodel
      responses:
        200:
          description: OK
      tags:
      - TaxRates
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