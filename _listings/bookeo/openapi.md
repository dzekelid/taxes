swagger: "2.0"
x-collection-name: Bookeo
x-complete: 1
info:
  title: Bookeo
  version: 1.0.0
host: api.bookeo.com
basePath: /v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /settings/taxes:
    get:
      summary: Retrieve all taxes used by this business
      description: Retrieve all taxes used by this business.
      operationId: getSettingsTaxes
      x-api-path-slug: settingstaxes-get
      responses:
        200:
          description: OK
      tags:
      - Settings
      - Taxes