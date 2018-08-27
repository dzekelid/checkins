swagger: "2.0"
x-collection-name: Foursquare
x-complete: 1
info:
  title: Foursquare
  version: 1.0.0
host: api.foursquare.com
basePath: /v2/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /checkins/add:
    post:
      summary: Post Checkins Add
      description: /checkins/{CHECKIN_ID}
      operationId: checkinscheckin-id
      x-api-path-slug: checkinsadd-post
      parameters:
      - in: query
        name: alt
        description: Altitude of the users location, in meters
      - in: query
        name: altAcc
        description: Vertical accuracy of the users location, in meters
      - in: query
        name: broadcast
        description: Who to broadcast this check-in to
      - in: query
        name: eventId
        description: The event the user is checking in to
      - in: query
        name: ll
        description: Latitude and longitude of the users location
      - in: query
        name: llAcc
        description: Accuracy of the users latitude and longitude, in meters
      - in: query
        name: shout
        description: A message about your check-in
      - in: query
        name: v
        description: All requests now accept a v=YYYYMMDD param, which indicates that
          the client is up to date as of the specified date
      - in: query
        name: venue
        description: If are not shouting, but you dont have a venue ID or would rather
          prefer a venueless checkin, pass the venue name as a string using this parameter
      - in: query
        name: venueId
        description: The venue where the user is checking in
      responses:
        200:
          description: OK
      tags:
      - Checkins
  /checkins/recent:
    get:
      summary: Get Checkins Recent
      description: /checkins/add
      operationId: checkinsadd
      x-api-path-slug: checkinsrecent-get
      parameters:
      - in: query
        name: afterTimestamp
        description: Seconds after which to look for checkins, e
      - in: query
        name: limit
        description: Number of results to return, up to 100
      - in: query
        name: ll
        description: Latitude and longitude of the users location, so response can
          include distance
      - in: query
        name: v
        description: All requests now accept a v=YYYYMMDD param, which indicates that
          the client is up to date as of the specified date
      responses:
        200:
          description: OK
      tags:
      - Checkins
      - Recent
  /checkins/{CHECKIN_ID}:
    get:
      summary: Get Checkins Checkin
      description: /venuegroups/{GROUP_ID}/removevenue
      operationId: venuegroupsgroup-idremovevenue
      x-api-path-slug: checkinscheckin-id-get
      parameters:
      - in: query
        name: CHECKIN_ID
        description: The ID of the checkin to retrieve additional information for
      - in: path
        name: CHECKIN_ID
      - in: query
        name: signature
        description: When checkins are sent to public feeds such as Twitter, foursquare
          appends a signature (s=XXXXXX) allowing users to bypass the friends-only
          access check on checkins
      - in: query
        name: v
        description: All requests now accept a v=YYYYMMDD param, which indicates that
          the client is up to date as of the specified date
      responses:
        200:
          description: OK
      tags:
      - Checkins
      - Checkin
  /checkins/{CHECKIN_ID}/addcomment:
    post:
      summary: Post Checkins Checkin Addcomment
      description: /checkins/recent
      operationId: checkinsrecent
      x-api-path-slug: checkinscheckin-idaddcomment-post
      parameters:
      - in: query
        name: CHECKIN_ID
        description: The ID of the checkin to add a comment to
      - in: path
        name: CHECKIN_ID
      - in: query
        name: text
        description: The text of the comment, up to 200 characters
      - in: query
        name: v
        description: All requests now accept a v=YYYYMMDD param, which indicates that
          the client is up to date as of the specified date
      responses:
        200:
          description: OK
      tags:
      - Checkins
      - Checkin
      - Comment
  /checkins/{CHECKIN_ID}/deletecomment:
    post:
      summary: Post Checkins Checkin Deletecomment
      description: /checkins/{CHECKIN_ID}/addcomment
      operationId: checkinscheckin-idaddcomment
      x-api-path-slug: checkinscheckin-iddeletecomment-post
      parameters:
      - in: query
        name: CHECKIN_ID
        description: The ID of the checkin to remove a comment from
      - in: path
        name: CHECKIN_ID
      - in: query
        name: commentId
        description: The id of the comment to remove
      - in: query
        name: v
        description: All requests now accept a v=YYYYMMDD param, which indicates that
          the client is up to date as of the specified date
      responses:
        200:
          description: OK
      tags:
      - Checkins
      - Checkin
      - Comment
  /users/{USER_ID}/checkins:
    get:
      summary: Get Users Checkins
      description: /users/{USER_ID}/badges
      operationId: usersuser-idbadges
      x-api-path-slug: usersuser-idcheckins-get
      parameters:
      - in: query
        name: afterTimestamp
        description: Retrieve the first results to follow these seconds since epoch
      - in: query
        name: beforeTimestamp
        description: Retrieve the first results prior to these seconds since epoch
      - in: query
        name: limit
        description: Number of results to return, up to 250
      - in: query
        name: offset
        description: The number of results to skip
      - in: query
        name: USER_ID
        description: Identity of the user to get details for
      - in: path
        name: USER_ID
      - in: query
        name: v
        description: All requests now accept a v=YYYYMMDD param, which indicates that
          the client is up to date as of the specified date
      responses:
        200:
          description: OK
      tags:
      - Users
      - Checkins