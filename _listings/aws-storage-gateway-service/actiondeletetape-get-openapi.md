---
swagger: "2.0"
x-collection-name: AWS Storage Gateway Service
x-complete: 0
info:
  title: AWS Storage Gateway Service API Delete Tape
  version: 1.0.0
  description: Deletes the specified virtual tape.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=CreateTapes:
    get:
      summary: Create Tapes
      description: Creates one or more virtual tapes.
      operationId: createTapes
      x-api-path-slug: actioncreatetapes-get
      parameters:
      - in: query
        name: ClientToken
        description: A unique identifier that you use to retry a request
        type: string
      - in: query
        name: GatewayARN
        description: The unique Amazon Resource Name (ARN) that represents the gateway
          to associate the         virtual tapes with
        type: string
      - in: query
        name: NumTapesToCreate
        description: The number of virtual tapes that you want to create
        type: string
      - in: query
        name: TapeBarcodePrefix
        description: A prefix that you append to the barcode of the virtual tape you
          are creating
        type: string
      - in: query
        name: TapeSizeInBytes
        description: The size, in bytes, of the virtual tapes that you want to create
        type: string
      responses:
        200:
          description: OK
      tags:
      - Tapes
  /?Action=DeleteTape:
    get:
      summary: Delete Tape
      description: Deletes the specified virtual tape.
      operationId: deleteTape
      x-api-path-slug: actiondeletetape-get
      parameters:
      - in: query
        name: GatewayARN
        description: The unique Amazon Resource Name (ARN) of the gateway that the
          virtual tape to delete         is associated with
        type: string
      - in: query
        name: TapeARN
        description: The Amazon Resource Name (ARN) of the virtual tape to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Tapes
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