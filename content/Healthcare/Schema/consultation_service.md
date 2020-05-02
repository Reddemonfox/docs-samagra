```json
{
    "$id": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/healthcare/schema/0.5.0/consultation_service.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the consultation service",
    "type": "object",
    "properties": {
        "id" : {
            "type" : "string"
          },
          "state" : {
            "type" : "string",
            "enum" : [ "OFFERED", "CONFIRMED", "REVOKED", "COMPLETED" ]
          },
          "expires_at" : {
            "$ref" : "https://schema.beckn.org/core/schema/0.7.1/time.json"
          },
          "item" : {
            "$ref" : "http://schema.beckn.org/core/schema/0.7.1/item.json"
          },
          "speciality" : {
            "type" : "string"
          },
          "clinicalnotes_url" : {
            "type" : "string"
          },
          "protocol" : {
            "$ref" : "#/components/schemas/consultationprotocol"
          },
          "consultations" : {
            "type" : "array",
            "items" : {
              "$ref" : "#/components/schemas/consultation"
            }
          },
          "person" : {
            "$ref" : "#/components/schemas/person/properties/id"
          },
          "provider" : {
            "$ref" : "http://schema.beckn.org/core/schema/0.7.1/provider.json#/properties/id"
          }
    }
}
```