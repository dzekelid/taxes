---
swagger: "2.0"
x-collection-name: Taxamo
x-complete: 0
info:
  title: Taxamo Settlement By Tax Type
  description: Settlement by tax type.
  version: "1"
host: api.taxamo.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v1/stats/settlement/by_taxation_type:
    get:
      summary: Settlement By Tax Type
      description: Settlement by tax type.
      operationId: getSettlementStatsByTaxationType
      x-api-path-slug: apiv1statssettlementby-taxation-type-get
      parameters:
      - in: query
        name: date_from
        description: Date from in yyyy-MM format
      - in: query
        name: date_to
        description: Date to in yyyy-MM format
      responses:
        200:
          description: OK
      tags:
      - Settlement
      - Tax
      - Type
  /api/v1/tax/calculate:
    get:
      summary: Simple Tax
      description: Simple tax.
      operationId: calculateSimpleTax
      x-api-path-slug: apiv1taxcalculate-get
      parameters:
      - in: query
        name: amount
        description: Amount
      - in: query
        name: billing_country_code
        description: Billing two letter ISO country code
      - in: query
        name: buyer_credit_card_prefix
        description: First 6 digits of buyers credit card prefix
      - in: query
        name: buyer_tax_number
        description: Buyers tax number - EU VAT number for example
      - in: query
        name: currency_code
        description: Currency code for transaction - e
      - in: query
        name: force_country_code
        description: Two-letter ISO country code, e
      - in: query
        name: invoice_address_city
        description: Invoice address/postal_code
      - in: query
        name: invoice_address_postal_code
        description: Invoice address/postal_code
      - in: query
        name: invoice_address_region
        description: Invoice address/region
      - in: query
        name: order_date
        description: Order date in yyyy-MM-dd format, in merchants timezone
      - in: query
        name: product_type
        description: Product type, according to dictionary /dictionaries/product_types
      - in: query
        name: quantity
        description: Quantity Defaults to 1
      - in: query
        name: tax_deducted
        description: If the transaction is in a country supported by Taxamo, but the
          tax is not calculated due to merchant settings or EU B2B transaction for
          example
      - in: query
        name: total_amount
        description: Total amount
      - in: query
        name: unit_price
        description: Unit price
      responses:
        200:
          description: OK
      tags:
      - Simple
      - Tax
    post:
      summary: Calculate Tax
      description: Calculate tax.
      operationId: calculateTax
      x-api-path-slug: apiv1taxcalculate-post
      parameters:
      - in: body
        name: input
        description: Input
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Calculate
      - Tax
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