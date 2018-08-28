---
swagger: "2.0"
x-collection-name: AWS Storage Gateway Service
x-complete: 0
info:
  title: AWS Storage Gateway Service API Create Tape With Barcode
  version: 1.0.0
  description: Creates a virtual tape by using your own barcode.
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
  /?Action=DeleteTapeArchive:
    get:
      summary: Delete Tape Archive
      description: Deletes the specified virtual tape from the virtual tape shelf
        (VTS).
      operationId: deleteTapeArchive
      x-api-path-slug: actiondeletetapearchive-get
      parameters:
      - in: query
        name: TapeARN
        description: The Amazon Resource Name (ARN) of the virtual tape to delete
          from the virtual tape         shelf (VTS)
        type: string
      responses:
        200:
          description: OK
      tags:
      - Tapes
      - Archives
  /?Action=DescribeTapes:
    get:
      summary: Describe Tapes
      description: Returns a description of the specified Amazon Resource Name (ARN)
        of virtual tapes.
      operationId: describeTapes
      x-api-path-slug: actiondescribetapes-get
      parameters:
      - in: query
        name: GatewayARN
        description: The Amazon Resource Name (ARN) of the gateway
        type: string
      - in: query
        name: Limit
        description: Specifies that the number of virtual tapes described be limited
          to the specified         number
        type: string
      - in: query
        name: Marker
        description: A marker value, obtained in a previous call to DescribeTapes
        type: string
      - in: query
        name: TapeARNs
        description: Specifies one or more unique Amazon Resource Names (ARNs) that
          represent the virtual         tapes you want to describe
        type: string
      responses:
        200:
          description: OK
      tags:
      - Tapes
  /?Action=ListTapes:
    get:
      summary: List Tapes
      description: |-
        Lists virtual tapes in your virtual tape library (VTL) and your virtual tape shelf
                 (VTS).
      operationId: listTapes
      x-api-path-slug: actionlisttapes-get
      parameters:
      - in: query
        name: Limit
        description: An optional number limit for the tapes in the list returned by
          this call
        type: string
      - in: query
        name: Marker
        description: A string that indicates the position at which to begin the returned
          list of         tapes
        type: string
      - in: query
        name: TapeARNs
        description: The Amazon Resource Name (ARN) of each of the tapes you want
          to list
        type: string
      responses:
        200:
          description: OK
      tags:
      - Tapes
  /?Action=RetrieveTapeArchive:
    get:
      summary: Retrieve Tape Archive
      description: |-
        Retrieves an archived virtual tape from the virtual tape shelf (VTS) to a
                 gateway-VTL.
      operationId: retrieveTapeArchive
      x-api-path-slug: actionretrievetapearchive-get
      parameters:
      - in: query
        name: GatewayARN
        description: The Amazon Resource Name (ARN) of the gateway you want to retrieve
          the virtual tape         to
        type: string
      - in: query
        name: TapeARN
        description: The Amazon Resource Name (ARN) of the virtual tape you want to
          retrieve from the         virtual tape shelf (VTS)
        type: string
      responses:
        200:
          description: OK
      tags:
      - Tapes
      - Archives
  /?Action=DescribeTapeRecoveryPoints:
    get:
      summary: Describe Tape Recovery Points
      description: |-
        Returns a list of virtual tape recovery points that are available for the specified
                 gateway-VTL.
      operationId: describeTapeRecoveryPoints
      x-api-path-slug: actiondescribetaperecoverypoints-get
      parameters:
      - in: query
        name: GatewayARN
        description: The Amazon Resource Name (ARN) of the gateway
        type: string
      - in: query
        name: Limit
        description: Specifies that the number of virtual tape recovery points that
          are described be         limited to the specified number
        type: string
      - in: query
        name: Marker
        description: An opaque string that indicates the position at which to begin
          describing the virtual         tape recovery points
        type: string
      responses:
        200:
          description: OK
      tags:
      - Tape Recovery Points
  /?Action=CreateTapeWithBarcode:
    get:
      summary: Create Tape With Barcode
      description: Creates a virtual tape by using your own barcode.
      operationId: createTapeWithBarcode
      x-api-path-slug: actioncreatetapewithbarcode-get
      parameters:
      - in: query
        name: GatewayARN
        description: The unique Amazon Resource Name (ARN) that represents the gateway
          to associate the         virtual tape with
        type: string
      - in: query
        name: TapeBarcode
        description: The barcode that you want to assign to the tape
        type: string
      - in: query
        name: TapeSizeInBytes
        description: The size, in bytes, of the virtual tape that you want to create
        type: string
      responses:
        200:
          description: OK
      tags:
      - Tape With Barcode
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