---
swagger: "2.0"
x-collection-name: Shopify
x-complete: 0
info:
  title: Shopify Update a province's tax rate
  description: Update a province's tax rate.
  version: 1.0.0
host: DefaultParameterValue:DefaultParameterValue@DefaultParameterValue.myshopify.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /admin/countries/261414723/provinces/4003640003.json:
    put:
      summary: Update a province's tax rate
      description: Update a province's tax rate.
      operationId: putAdminCountries261414723Provinces4003640003.json
      x-api-path-slug: admincountries261414723provinces4003640003-json-put
      parameters:
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Provinces
      - Tax
      - Rate
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