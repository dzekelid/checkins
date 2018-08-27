{
  "info": {
    "name": "Foursquare Get Checkins Recent",
    "_postman_id": "ad4f03c2-c76f-4bdd-a222-356c748e200e",
    "description": "/checkins/add",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Campaigns",
      "item": [
        {
          "id": "31e277f3-cb7e-4041-9a73-3aa491440dd7",
          "name": "campaignscampaign-id",
          "request": {
            "url": "http://api.foursquare.com/v2/campaigns/add?campaignId=%7B%7D&endAt=%7B%7D&groupId=%7B%7D&specialId=%7B%7D&startAt=%7B%7D&v=%7B%7D&venueId=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "/campaigns/{CAMPAIGN_ID}"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "69ad7ccb-fd23-422c-935a-4a6ce72208bf"
            }
          ]
        },
        {
          "id": "4c2d6387-e20b-47f8-8f04-d1337b45e66e",
          "name": "campaignsadd",
          "request": {
            "url": "http://api.foursquare.com/v2/campaigns/list?groupId=%7B%7D&specialId=%7B%7D&status=%7B%7D&v=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "/campaigns/add"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f6335b19-937d-421e-be7f-e333339ecbd4"
            }
          ]
        },
        {
          "id": "7bfcddd2-353a-47fb-b0a7-37bfdc9bb886",
          "name": "specialsspecial-idretire",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.foursquare.com",
              "path": [
                "v2",
                "campaigns/:CAMPAIGN_ID"
              ],
              "query": [
                {
                  "key": "v",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "CAMPAIGN_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "/specials/{SPECIAL_ID}/retire"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c7380ef3-af9f-421b-ba49-3c0c1e14a9ca"
            }
          ]
        },
        {
          "id": "c50bfc54-ba6a-4cad-a75a-32917acef198",
          "name": "campaignscampaign-idtimeseries",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.foursquare.com",
              "path": [
                "v2",
                "campaigns/:CAMPAIGN_ID/delete"
              ],
              "query": [
                {
                  "key": "v",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "CAMPAIGN_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "/campaigns/{CAMPAIGN_ID}/timeseries"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "544dab27-f96a-4050-9236-0ae03951bb34"
            }
          ]
        },
        {
          "id": "88428fab-fab3-4c18-80af-a9d82f2b011c",
          "name": "campaignscampaign-iddelete",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.foursquare.com",
              "path": [
                "v2",
                "campaigns/:CAMPAIGN_ID/end"
              ],
              "query": [
                {
                  "key": "v",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "CAMPAIGN_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "/campaigns/{CAMPAIGN_ID}/delete"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "55814590-d905-4000-9fa5-1bcdf9b28a7a"
            }
          ]
        },
        {
          "id": "8e94b4c0-5436-438c-aa55-6e7f0fc531bb",
          "name": "campaignscampaign-idend",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.foursquare.com",
              "path": [
                "v2",
                "campaigns/:CAMPAIGN_ID/start"
              ],
              "query": [
                {
                  "key": "startAt",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "v",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "CAMPAIGN_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "/campaigns/{CAMPAIGN_ID}/end"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f53454b9-e7e2-48a3-882c-511283e07b52"
            }
          ]
        },
        {
          "id": "da4c08ca-fc31-4cf7-9180-a353d735ae7e",
          "name": "campaignslist",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.foursquare.com",
              "path": [
                "v2",
                "campaigns/:CAMPAIGN_ID/timeseries"
              ],
              "query": [
                {
                  "key": "endAt",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "startAt",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "v",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "CAMPAIGN_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "/campaigns/list"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "90ef7962-247c-45df-a3ab-0ff8a475c7f7"
            }
          ]
        }
      ]
    },
    {
      "name": "Checkins",
      "item": [
        {
          "id": "7bead537-6351-4f06-95f9-d7fbf710ded2",
          "name": "checkinscheckin-id",
          "request": {
            "url": "http://api.foursquare.com/v2/checkins/add?alt=%7B%7D&altAcc=%7B%7D&broadcast=%7B%7D&eventId=%7B%7D&ll=%7B%7D&llAcc=%7B%7D&shout=%7B%7D&v=%7B%7D&venue=%7B%7D&venueId=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "/checkins/{CHECKIN_ID}"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1784e3a1-b7fa-4476-b6b2-2fd8effaf251"
            }
          ]
        },
        {
          "id": "f67eb490-2cce-4fbf-9395-83f40c601998",
          "name": "checkinsadd",
          "request": {
            "url": "http://api.foursquare.com/v2/checkins/recent?afterTimestamp=%7B%7D&limit=%7B%7D&ll=%7B%7D&v=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "/checkins/add"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ed689337-f4ae-4497-aaf3-e07a5f2c210f"
            }
          ]
        }
      ]
    }
  ]
}