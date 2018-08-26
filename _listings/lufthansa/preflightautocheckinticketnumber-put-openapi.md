---
swagger: "2.0"
x-collection-name: Lufthansa
x-complete: 0
info:
  title: LH Partner Auto Check-In
  version: "1.0"
  description: Trigger an automatic check-in given a ticket number. This service is
    only accessible for LH privileged partners
host: api.lufthansa.com
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /preflight/autocheckin/{ticketnumber}:
    put:
      summary: Auto Check-In
      description: Trigger an automatic check-in given a ticket number. This service
        is only accessible for LH privileged partners
      operationId: preflight.autocheckin.ticketnumber.put
      x-api-path-slug: preflightautocheckinticketnumber-put
      parameters:
      - in: header
        name: Accept
        description: 'http header: application/json or application/xml (Acceptable
          values are: application/json, application/xml)'
      - in: query
        name: emailAddress
        description: Email address
      - in: path
        name: ticketnumber
        description: Ticket number
      responses:
        200:
          description: OK
      tags:
      - Auto
      - Check-In
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