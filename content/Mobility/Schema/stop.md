```json
{
    "$id": "http://schema.beckn.org/mobility/schema/0.7.1/stop.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the stop object",
    "type": "object",
    "properties": {
        "location" : {
            "$ref" : "http://schema.beckn.org/core/schema/0.7.1/location.json"
        },
        "arrival_time" : {
            "type" : "string",
            "format" : "date-time"
        },
        "departure_time" : {
            "type" : "string",
            "format" : "date-time"
        }
    }
}
```        