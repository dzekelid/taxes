swagger: "2.0"
x-collection-name: Shopify
x-complete: 1
info:
  title: Shopify API
  description: todo-add-description
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