---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Get Tax rates
  version: 1.0.0
  description: Get tax rates.
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/accountingsystem/taxstatus:
    get:
      summary: Get Tax Status of Accounting System
      description: Get tax status of accounting system.
      operationId: AccountingSystem_GetTaxStatus
      x-api-path-slug: apiaccountingsystemtaxstatus-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Tax
      - Status
      - Of
      - Accounting
      - System
  /api/tax/agentheld:
    get:
      summary: Get all tax held by agent
      description: Get all tax held by agent.
      operationId: Tax_GetAgentTaxHeldLedger
      x-api-path-slug: apitaxagentheld-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Tax
      - Held
      - By
      - Agent
  /api/tax/pay/hmrc:
    post:
      summary: Pay tax out of tax held account
      description: Pay tax out of tax held account.
      operationId: Tax_PayTaxHmrcBypayTaxDataContract
      x-api-path-slug: apitaxpayhmrc-post
      parameters:
      - in: body
        name: payTaxDataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Pay
      - Tax
      - Out
      - Of
      - Tax
      - Held
      - Account
  /api/tax/{id}/setasdefault:
    post:
      summary: Set default tax rate for the accounting system
      description: Set default tax rate for the accounting system.
      operationId: Tax_SetDefaultTaxRateByid
      x-api-path-slug: apitaxidsetasdefault-post
      parameters:
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Set
      - Default
      - Tax
      - Ratethe
      - Accounting
      - System
  /api/tax/create:
    post:
      summary: Create a new tax rate for the system
      description: Create a new tax rate for the system.
      operationId: Tax_CreateTaxRateBytaxRateDataContract
      x-api-path-slug: apitaxcreate-post
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: body
        name: taxRateDataContract
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - New
      - Tax
      - Ratethe
      - System
  /api/Tax:
    get:
      summary: Get Tax rates
      description: Get tax rates.
      operationId: Tax_Get
      x-api-path-slug: apitax-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Tax
      - Rates
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