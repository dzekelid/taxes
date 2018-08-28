---
swagger: "2.0"
x-collection-name: Google Content API for Shopping
x-complete: 0
info:
  title: Google Content API for Shopping API Update Account Tax
  description: 'Updates the tax settings of the account. This method can only be called
    for accounts to which the managing account has access: either the managing account
    itself or sub-accounts if the managing account is a multi-client account.'
  contact:
    name: Google
    url: https://google.com
  version: v2
host: www.googleapis.com
basePath: /content/v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /accounttax/batch:
    post:
      summary: Account Taxes
      description: Retrieves and updates tax settings of multiple accounts in a single
        request.
      operationId: content.accounttax.custombatch
      x-api-path-slug: accounttaxbatch-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: dryRun
        description: Flag to run the request in dry-run mode
      responses:
        200:
          description: OK
      tags:
      - Account
      - Taxes
  /{merchantId}/accounttax:
    get:
      summary: Get Account Taxes
      description: Lists the tax settings of the sub-accounts in your Merchant Center
        account. This method can only be called for multi-client accounts.
      operationId: content.accounttax.list
      x-api-path-slug: merchantidaccounttax-get
      parameters:
      - in: query
        name: maxResults
        description: The maximum number of tax settings to return in the response,
          used for paging
      - in: path
        name: merchantId
        description: The ID of the managing account
      - in: query
        name: pageToken
        description: The token returned by the previous request
      responses:
        200:
          description: OK
      tags:
      - Account
      - Taxes
  /{merchantId}/accounttax/{accountId}:
    get:
      summary: Get Account Tax
      description: 'Retrieves the tax settings of the account. This method can only
        be called for accounts to which the managing account has access: either the
        managing account itself or sub-accounts if the managing account is a multi-client
        account.'
      operationId: content.accounttax.get
      x-api-path-slug: merchantidaccounttaxaccountid-get
      parameters:
      - in: path
        name: accountId
        description: The ID of the account for which to get/update account tax settings
      - in: path
        name: merchantId
        description: The ID of the managing account
      responses:
        200:
          description: OK
      tags:
      - Account
      - Tax
    patch:
      summary: Update Account Tax
      description: 'Updates the tax settings of the account. This method can only
        be called for accounts to which the managing account has access: either the
        managing account itself or sub-accounts if the managing account is a multi-client
        account. This method supports patch semantics.'
      operationId: content.accounttax.patch
      x-api-path-slug: merchantidaccounttaxaccountid-patch
      parameters:
      - in: path
        name: accountId
        description: The ID of the account for which to get/update account tax settings
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: dryRun
        description: Flag to run the request in dry-run mode
      - in: path
        name: merchantId
        description: The ID of the managing account
      responses:
        200:
          description: OK
      tags:
      - Account
      - Tax
    put:
      summary: Update Account Tax
      description: 'Updates the tax settings of the account. This method can only
        be called for accounts to which the managing account has access: either the
        managing account itself or sub-accounts if the managing account is a multi-client
        account.'
      operationId: content.accounttax.update
      x-api-path-slug: merchantidaccounttaxaccountid-put
      parameters:
      - in: path
        name: accountId
        description: The ID of the account for which to get/update account tax settings
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: dryRun
        description: Flag to run the request in dry-run mode
      - in: path
        name: merchantId
        description: The ID of the managing account
      responses:
        200:
          description: OK
      tags:
      - Account
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