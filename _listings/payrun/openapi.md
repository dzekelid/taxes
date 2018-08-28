swagger: "2.0"
x-collection-name: PayRun
x-complete: 1
info:
  title: Pay Run.IO
  description: open-scableable-transparent-payroll-api-
  version: 17.18.6.206
host: api.test.payrun.io
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Templates/paylinetax:
    get:
      summary: Gets the pay line tax template
      description: Return the pay line tax data object template
      operationId: GetPayLineTaxTemplate
      x-api-path-slug: templatespaylinetax-get
      parameters:
      - in: header
        name: Api-Version
        description: The version of the api to target
      - in: header
        name: Authorization
        description: The OAuth 1 authorization header
      responses:
        200:
          description: OK
      tags:
      - Pay
      - Line
      - Tax
      - Template
  /Templates/taxpayinstruction:
    get:
      summary: Gets the tax pay instruction template
      description: Return the tax pay instruction data object template
      operationId: GetTaxPayInstructionTemplate
      x-api-path-slug: templatestaxpayinstruction-get
      parameters:
      - in: header
        name: Api-Version
        description: The version of the api to target
      - in: header
        name: Authorization
        description: The OAuth 1 authorization header
      responses:
        200:
          description: OK
      tags:
      - Tax
      - Pay
      - Instruction
      - Template
  /Templates/taxytdpayinstruction:
    get:
      summary: Gets the tax YTD pay instruction template
      description: Return the tax YTD pay instruction data object template
      operationId: GetTaxYtdPayInstructionTemplate
      x-api-path-slug: templatestaxytdpayinstruction-get
      parameters:
      - in: header
        name: Api-Version
        description: The version of the api to target
      - in: header
        name: Authorization
        description: The OAuth 1 authorization header
      responses:
        200:
          description: OK
      tags:
      - Tax
      - YTD
      - Pay
      - Instruction
      - Template
  /Schemas/TaxPayInstruction.xsd:
    get:
      summary: Get the TaxPayInstruction schema
      description: Returns the TaxPayInstruction schema object
      operationId: GetTaxPayInstructionSchema
      x-api-path-slug: schemastaxpayinstruction-xsd-get
      parameters:
      - in: header
        name: Api-Version
        description: The version of the api to target
      - in: header
        name: Authorization
        description: The OAuth 1 authorization header
      responses:
        200:
          description: OK
      tags:
      - TaxPayInstruction
      - Schema