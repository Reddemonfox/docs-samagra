```json
{
    "$id": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/healthcare/schema/0.5.0/clinical_notes.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes clinical notes",
    "type": "object",
    "properties": {
        "chiefcomplaints" : {
            "$ref" : "#/components/schemas/taxonomyitem"
          },
          "medicalhistory" : {
            "$ref" : "#/components/schemas/taxonomyitem"
          },
          "allergies" : {
            "$ref" : "#/components/schemas/taxonomyitem"
          },
          "previousconditions" : {
            "$ref" : "#/components/schemas/taxonomyitem"
          },
          "otherinfo" : {
            "$ref" : "#/components/schemas/objectmap"
          }
    }
}
```