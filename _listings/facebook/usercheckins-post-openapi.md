---
swagger: "2.0"
x-collection-name: Facebook
x-complete: 0
info:
  title: Facebook Post User Checkins
  description: Checks the user into a place
  version: 1.0.0
host: graph.facebook.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{page}/checkins:
    get:
      summary: Get Page Checkins
      description: Checkins made to this Place Page by the current user, and friends
        of the current user
      operationId: getPageCheckins
      x-api-path-slug: pagecheckins-get
      parameters:
      - in: path
        name: page
        description: Represents the ID of the page object
      responses:
        200:
          description: OK
      tags:
      - Page
      - Checkins
  /{user}/checkins:
    get:
      summary: Get User Checkins
      description: The places that the user has checked-into
      operationId: getUserCheckins
      x-api-path-slug: usercheckins-get
      parameters:
      - in: path
        name: user
        description: Represents the ID of the user object
      responses:
        200:
          description: OK
      tags:
      - User
      - Checkins
    post:
      summary: Post User Checkins
      description: Checks the user into a place
      operationId: postUserCheckins
      x-api-path-slug: usercheckins-post
      parameters:
      - in: query
        name: coordinates
        description: 'The users location, as a string containing latitude and longitude:
          {latitude:'
      - in: query
        name: link
        description: Checkin link
      - in: query
        name: message
        description: Checkin description
      - in: query
        name: picture
        description: Checkin picture
      - in: query
        name: place
        description: Checkin Place ID; for example 110506962309835 for Facebook HQ
      - in: query
        name: tags
        description: Comma-separated list of tagged friends user IDs
      - in: path
        name: user
        description: Represents the ID of the user object
      responses:
        200:
          description: OK
      tags:
      - User
      - Checkins
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