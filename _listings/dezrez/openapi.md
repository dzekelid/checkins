swagger: "2.0"
x-collection-name: Dezrez
x-complete: 1
info:
  title: Dezrez.Rezi.Client.Api
  version: 1.0.0
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/property/{id}/keys/checkin:
    put:
      summary: Checkin a collection of keys for a property
      description: Checkin a collection of keys for a property.
      operationId: Property_CheckinKeysByidBycheckinDetails
      x-api-path-slug: apipropertyidkeyscheckin-put
      parameters:
      - in: body
        name: checkinDetails
        description: The details of the keys to checkin
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: The property id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Checkin
      - Collection
      - Of
      - Keysa
      - Property