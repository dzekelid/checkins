{
  "info": {
    "name": "LH Partner Auto Check-In",
    "_postman_id": "4ffdc040-3660-4a51-bc87-76b373696f81",
    "description": "Trigger an automatic check-in given a ticket number. This service is only accessible for LH privileged partners",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Baggage",
      "item": [
        {
          "id": "f8f728f9-01e6-48c4-8688-252db80899c0",
          "name": "baggage.baggagetripandcontact.searchID.get",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.lufthansa.com",
              "path": [
                "v1",
                "baggage/baggagetripandcontact/:searchID"
              ],
              "variable": [
                {
                  "id": "searchID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "http header: application/json or application/xml (Acceptable values are: application/json, application/xml)",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve passenger trip, contact and baggage details. This service is only accessible for LH privileged partners"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ba01445f-eb5a-4266-a841-fcd5176481e6"
            }
          ]
        }
      ]
    },
    {
      "name": "All",
      "item": [
        {
          "id": "683a9d52-ff86-4189-81af-985a1e704cef",
          "name": "offers.fares.allfares.get",
          "request": {
            "url": "http://api.lufthansa.com/v1/offers/fares/allfares?cabin-class=%7B%7D&catalogues=%7B%7D&destination=%7B%7D&fare-family=%7B%7D&origin=%7B%7D&return-date=%7B%7D&trackingid=%7B%7D&travel-date=%7B%7D&travelers=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "Mandatory http header:  application/xml or application/json",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves all available fares for a specific Origin & Destination pair on a given date. Available fares are: One-way and Return for 4U. Return only for OS"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e5f4d26d-0fb7-4597-b1eb-dc99e14a647e"
            }
          ]
        }
      ]
    },
    {
      "name": "Best",
      "item": [
        {
          "id": "eb459495-f210-46db-9cdf-18a06eb5276c",
          "name": "offers.fares.bestfares.get",
          "request": {
            "url": "http://api.lufthansa.com/v1/offers/fares/bestfares?cabin-class=%7B%7D&catalogues=%7B%7D&country=%7B%7D&destination=%7B%7D&fare-family=%7B%7D&origin=%7B%7D&range=%7B%7D&trackingid=%7B%7D&travel-date=%7B%7D&trip-duration=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "http header: application/json or application/xml (Acceptable values are: application/json, application/xml)",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve best fares for the requested journey across multiple days or multiple months."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "de8001d7-f5a7-401d-9fa4-40b68d318aee"
            }
          ]
        }
      ]
    },
    {
      "name": "Deep",
      "item": [
        {
          "id": "3123999a-f015-4137-a9fb-96d3d65381b0",
          "name": "offers.fares.deeplink.get",
          "request": {
            "url": "http://api.lufthansa.com/v1/offers/fares/deeplink?cabin-class=%7B%7D&catalogues=%7B%7D&country=%7B%7D&destination=%7B%7D&destination-name=%7B%7D&encryption-key=%7B%7D&fare=%7B%7D&fare-currency=%7B%7D&lang=%7B%7D&net-fare=%7B%7D&origin=%7B%7D&origin-name=%7B%7D&outbound-segments=%7B%7D&partnerid=%7B%7D&return-date=%7B%7D&return-segments=%7B%7D&trackingid=%7B%7D&travel-date=%7B%7D&travelers=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "http header: application/json or application/xml (Acceptable values are: application/json, application/xml)",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns valid deep links for the provided input parameters"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6f20f74e-68b9-4be9-806f-193d0fb88b05"
            }
          ]
        }
      ]
    },
    {
      "name": "LH",
      "item": [
        {
          "id": "d979848a-ca71-4b75-81a1-788dc81fc71c",
          "name": "offers.fares.deeplink.ffp.get",
          "request": {
            "url": "http://api.lufthansa.com/v1/offers/fares/deeplink/ffp?cabin-class=%7B%7D&catalogues=%7B%7D&country=%7B%7D&destination=%7B%7D&encryption-key=%7B%7D&lang=%7B%7D&origin=%7B%7D&partnerid=%7B%7D&return-date=%7B%7D&trackingid=%7B%7D&travel-date=%7B%7D&travelers=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "http header: application/json or application/xml (Acceptable values are: application/json, application/xml)",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns valid LH deep links (FFP - links to flight selection screen on LH.COM)"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8e4b4bed-ea1e-405f-9086-89aaf7f4da44"
            }
          ]
        },
        {
          "id": "a9fc7a23-a275-44a9-88b1-43f54a76b107",
          "name": "offers.fares.deeplink.itco.get",
          "request": {
            "url": "http://api.lufthansa.com/v1/offers/fares/deeplink/itco?cabin-class=%7B%7D&catalogues=%7B%7D&country=%7B%7D&destination=%7B%7D&encryption-key=%7B%7D&fare=%7B%7D&fare-currency=%7B%7D&lang=%7B%7D&net-fare=%7B%7D&origin=%7B%7D&outbound-segments=%7B%7D&partnerid=%7B%7D&return-date=%7B%7D&return-segments=%7B%7D&trackingid=%7B%7D&travel-date=%7B%7D&travelers=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "http header: application/json or application/xml (Acceptable values are: application/json, application/xml)",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns valid LH deep links (ITCO - links to shopping cart on LH.COM)"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dad627e1-aaad-4650-9bcf-220911294b45"
            }
          ]
        }
      ]
    },
    {
      "name": "Fares",
      "item": [
        {
          "id": "c88070d8-2c18-447f-92af-3bd109e17347",
          "name": "Fares",
          "request": {
            "url": "http://api.lufthansa.com/v1/offers/fares/fares?carriers=%7B%7D&catalogues=%7B%7D&fare-types=%7B%7D&segments=%7B%7D&travelers=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "http header: application/json or application/xml (Acceptable values are: application/json, application/xml)",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve all available fares per fare family for a specific Origin & Destination on a given date"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5b95a8e1-dc6d-47ef-a349-a406adfbdff0"
            }
          ]
        },
        {
          "id": "d94efa2d-0321-4694-8277-28e908477f69",
          "name": "offers.fares.subscriptions.get",
          "request": {
            "url": "http://api.lufthansa.com/v1/offers/fares/subscriptions?cabin-class=%7B%7D&country=%7B%7D&destination=%7B%7D&email=%7B%7D&lang=%7B%7D&origin=%7B%7D&trackingid=%7B%7D&trip-duration=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "http header: application/json or application/xml (Acceptable values are: application/json, application/xml)",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Create a subscription for best price O&D. Receive regular updates on lowest fares"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "54ff8729-d12d-4cdd-9a6d-7c9f36e29e11"
            }
          ]
        }
      ]
    },
    {
      "name": "Lowest",
      "item": [
        {
          "id": "a304feed-7d8b-4878-ada5-bc3aea725604",
          "name": "offers.fares.lowestfares.get",
          "request": {
            "url": "http://api.lufthansa.com/v1/offers/fares/lowestfares?cabin-class=%7B%7D&catalogues=%7B%7D&country=%7B%7D&destination=%7B%7D&fare-family=%7B%7D&origin=%7B%7D&return-date=%7B%7D&travel-date=%7B%7D&travelers=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "http header: application/json or application/xml (Acceptable values are: application/json, application/xml)",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve lowest fare for a specific Origin & Destination pair on a given date. Available fares are: One-way and Return for 4U. Return only for OS & LH"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d2378481-9386-43b5-9c47-8aed58cc5d67"
            }
          ]
        }
      ]
    },
    {
      "name": "OND",
      "item": [
        {
          "id": "0c1b6f72-a5d4-464d-837e-8ebd38eade74",
          "name": "offers.ond.route.origin.destination.get",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.lufthansa.com",
              "path": [
                "v1",
                "offers/ond/route/:origin/:destination"
              ],
              "query": [
                {
                  "key": "catalogues",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "offset",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "destination",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "origin",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "Mandatory http header:  application/xml or application/json",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns LH route origin & destination information"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f9615d84-d803-4698-a4b6-00662e7a7f11"
            }
          ]
        },
        {
          "id": "71a01142-9a99-4ed5-9dba-8ab12d485f3a",
          "name": "offers.ond.status.get",
          "request": {
            "url": "http://api.lufthansa.com/v1/offers/ond/status?catalogues=%7B%7D&new-routes=%7B%7D&old-routes=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "Mandatory http header:  application/xml or application/json",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns LH network route status information. Search for recently added or retired routes"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ec9b4614-67e5-49d1-88f5-3b36931dac40"
            }
          ]
        }
      ]
    },
    {
      "name": "Top",
      "item": [
        {
          "id": "db68cd73-dc11-4f5e-9940-41b31a336515",
          "name": "offers.ond.top.get",
          "request": {
            "url": "http://api.lufthansa.com/v1/offers/ond/top?catalogues=%7B%7D&origin=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "Mandatory http header:  application/xml or application/json",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns LH Top routes per country or across all countries"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8cf9e9d8-8e2a-49f0-a30f-90424c5ea774"
            }
          ]
        }
      ]
    },
    {
      "name": "Orders",
      "item": [
        {
          "id": "e2b57b49-0b59-450b-8f06-3285d6bfc22c",
          "name": "Orders",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.lufthansa.com",
              "path": [
                "v1",
                "orders/orders/:orderID/:name"
              ],
              "variable": [
                {
                  "id": "name",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "orderID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "http header: application/json or application/xml (Acceptable values are: application/json, application/xml)",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve order by ID and optionally name. This service is only accessible for LH privileged partners"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "aa88a81d-fa8a-4e71-b390-433a885c064a"
            }
          ]
        }
      ]
    },
    {
      "name": "Auto",
      "item": [
        {
          "id": "fdc7a674-ae9c-46bc-9ac9-1b95efe2fc29",
          "name": "preflight.autocheckin.ticketnumber.put",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.lufthansa.com",
              "path": [
                "v1",
                "preflight/autocheckin/:ticketnumber"
              ],
              "query": [
                {
                  "key": "emailAddress",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "ticketnumber",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "http header: application/json or application/xml (Acceptable values are: application/json, application/xml)",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Trigger an automatic check-in given a ticket number. This service is only accessible for LH privileged partners"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a81bdd0c-46b5-4c1d-8a39-74befea3c907"
            }
          ]
        }
      ]
    }
  ]
}