---
swagger: "2.0"
x-collection-name: Square
x-complete: 0
info:
  title: Square Connect API Modifies the details of an existing fee (tax).
  description: Modifies the details of an existing fee (tax).
  termsOfService: https://connect.squareup.com/tos
  contact:
    name: Square Developer Platform
    url: https://squareup.com/developers
    email: developers@squareup.com
  version: "2.0"
host: connect.squareup.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/{location_id}/fees:
    get:
      summary: Lists all of a location's fees (taxes).
      description: Lists all of a location's fees (taxes).
      operationId: ListFees
      x-api-path-slug: v1location-idfees-get
      parameters:
      - in: path
        name: location_id
        description: The ID of the location to list fees for
      responses:
        200:
          description: OK
      tags:
      - Lists
      - ""
      - Of
      - Locations
      - Fees
      - (taxes)
    post:
      summary: Creates a fee (tax).
      description: Creates a fee (tax).
      operationId: CreateFee
      x-api-path-slug: v1location-idfees-post
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: location_id
        description: The ID of the location to create a fee for
      responses:
        200:
          description: OK
      tags:
      - Creates
      - Fee
      - (tax)
  /v1/{location_id}/fees/{fee_id}:
    delete:
      summary: Deletes an existing fee (tax).
      description: Deletes an existing fee (tax).
      operationId: DeleteFee
      x-api-path-slug: v1location-idfeesfee-id-delete
      parameters:
      - in: path
        name: fee_id
        description: The ID of the fee to delete
      - in: path
        name: location_id
        description: The ID of the fees associated location
      responses:
        200:
          description: OK
      tags:
      - S
      - Existing
      - Fee
      - (tax)
    put:
      summary: Modifies the details of an existing fee (tax).
      description: Modifies the details of an existing fee (tax).
      operationId: UpdateFee
      x-api-path-slug: v1location-idfeesfee-id-put
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: fee_id
        description: The ID of the fee to edit
      - in: path
        name: location_id
        description: The ID of the fees associated location
      responses:
        200:
          description: OK
      tags:
      - Modifies
      - Details
      - Of
      - Existing
      - Fee
      - (tax)
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