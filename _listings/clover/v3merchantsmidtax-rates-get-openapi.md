---
swagger: "2.0"
x-collection-name: Clover
x-complete: 0
info:
  title: Clover Get all tax rates
  version: 1.0.0
  description: Get all tax rates.
host: /merchants
basePath: https://api.clover.com
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/merchants/{mId}/tax_rates:
    get:
      summary: Get all tax rates
      description: Get all tax rates.
      operationId: GetTaxRates
      x-api-path-slug: v3merchantsmidtax-rates-get
      parameters:
      - in: query
        name: expand
        description: 'Expandable fields: [items]'
      - in: query
        name: filter
        description: 'Filter fields: [isDefault, rate, items'
      - in: path
        name: mId
        description: Merchant Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Tax
      - Rates
    post:
      summary: Create a tax rate for a merchant
      description: Create a tax rate for a merchant.
      operationId: CreateTaxRate
      x-api-path-slug: v3merchantsmidtax-rates-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: expand
        description: 'Expandable fields: [items]'
      - in: path
        name: mId
        description: Merchant Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Tax
      - Rates
  /v3/merchants/{mId}/tax_rates/{taxId}:
    get:
      summary: Get a single tax rate
      description: Get a single tax rate.
      operationId: GetTaxRate
      x-api-path-slug: v3merchantsmidtax-ratestaxid-get
      parameters:
      - in: query
        name: expand
        description: 'Expandable fields: [items]'
      - in: path
        name: mId
        description: Merchant Id
      - in: path
        name: taxId
        description: Tax Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Tax
      - Rates
      - TaxId
    post:
      summary: Update a single tax rate
      description: Update a single tax rate.
      operationId: UpdateTaxRate
      x-api-path-slug: v3merchantsmidtax-ratestaxid-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: mId
        description: Merchant Id
      - in: path
        name: taxId
        description: Tax Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Tax
      - Rates
      - TaxId
    delete:
      summary: Delete a single tax rate
      description: Delete a single tax rate.
      operationId: DeleteTaxRate
      x-api-path-slug: v3merchantsmidtax-ratestaxid-delete
      parameters:
      - in: path
        name: mId
        description: Merchant Id
      - in: path
        name: taxId
        description: Tax Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Tax
      - Rates
      - TaxId
  /v3/merchants/{mId}/tax_rate_items:
    post:
      summary: Create or delete a tax rate item
      description: Create or delete a tax rate item.
      operationId: CreateOrDeleteTaxRateItems
      x-api-path-slug: v3merchantsmidtax-rate-items-post
      parameters:
      - in: path
        name: mId
        description: Merchant Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Tax
      - Rate
      - Items
  /v3/merchants/{mId}/tax_rates/{taxId}/items:
    get:
      summary: Get items by tax rate
      description: Get items by tax rate.
      operationId: GetItemsByTaxRate
      x-api-path-slug: v3merchantsmidtax-ratestaxiditems-get
      parameters:
      - in: query
        name: expand
        description: 'Expandable fields: [items]'
      - in: query
        name: filter
        description: 'Filter fields: [id, name, sku, modifiedTime, deleted, hidden,
          price, alternateName, itemCode, item'
      - in: path
        name: mId
        description: Merchant Id
      - in: path
        name: taxId
        description: Tax Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Tax
      - Rates
      - TaxId
      - Items
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