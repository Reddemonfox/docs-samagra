```json
{
    "$id": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/healthcare/schema/0.5.0/consultation_service.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes an instantiated consultation service",
    "type": "object",
    "properties": {
        "type" : {
            "$ref" : "#/components/schemas/consultationtype"
          },
          "state" : {
            "type" : "string",
            "enum" : [ "NEW", "SCHEDULED", "IN_PROGRESS", "COMPLETED", "CLOSED" ]
          },
          "who" : {
            "$ref" : "#/components/schemas/doctor"
          },
          "assign_at" : {
            "$ref" : "https://schema.beckn.org/core/schema/0.7.1/time.json"
          },
          "at" : {
            "$ref" : "https://schema.beckn.org/core/schema/0.7.1/time.json"
          },
          "duration" : {
            "type" : "number"
          },
          "url" : {
            "type" : "string"
          },
          "channels" : {
            "type" : "array",
            "items" : {
              "$ref" : "#/components/schemas/channel"
            }
          },
          "preferred_channel" : {
            "$ref" : "#/components/schemas/channel"
          },
          "clinical_notes" : {
            "$ref" : "#/components/schemas/clinicalnotes"
          },
          "summary" : {
            "$ref" : "#/components/schemas/consultationsummary"
          }
    }
}
```json