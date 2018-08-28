swagger: "2.0"
x-collection-name: Xero
x-complete: 1
info:
  title: Xero oAuth 1a
  description: a-collection-to-authenticate-to-the-xero-api-using-oauth1-0a
  version: 1.0.0
host: api.xero.com
basePath: /
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