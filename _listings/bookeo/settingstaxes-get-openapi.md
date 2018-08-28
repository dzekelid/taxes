---
swagger: "2.0"
x-collection-name: Bookeo
x-complete: 0
info:
  title: Bookeo Retrieve all taxes used by this business
  version: 1.0.0
  description: Retrieve all taxes used by this business.
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