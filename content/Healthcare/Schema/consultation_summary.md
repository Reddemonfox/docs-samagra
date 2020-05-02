```json
{
    "$id": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/healthcare/schema/0.5.0/consultation_summary.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the summary of a consultation",
    "type": "object",
    "properties": {
        "consultation" : {
            "$ref" : "#/components/schemas/consultationservice/properties/id"
          },
          "summary" : {
            "type" : "object",
            "properties" : {
              "duration" : {
                "type" : "number"
              },
              "prescription_url" : {
                "type" : "string"
              },
              "prescription" : {
                "$ref" : "#/components/schemas/prescription"
              }
            }
          }
         
    }
}
