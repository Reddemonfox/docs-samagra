```json
{
    "$id": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/healthcare/schema/0.5.0/person.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes a person",
    "type": "object",
    "properties": {
        "id" : {
            "type" : "string"
          },
          "uhid" : {
            "type" : "string"
          },
          "consentid" : {
            "type" : "string"
          },
          "isActive" : {
            "type" : "boolean"
          },
          "address" : {
            "$ref" : "https://schema.beckn.org/core/schema/0.7.1/location.json"
          },
          "last_gps_location" : {
            "$ref" : "https://schema.beckn.org/core/schema/0.7.1/location.json"
          }
    }
}
```