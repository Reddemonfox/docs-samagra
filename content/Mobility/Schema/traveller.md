```json
{
    "$id": "http://schema.beckn.org/mobility/schema/0.7.1/traveller.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes a traveller",
    "type": "object",
    "properties": {
        "descriptor" : {
            "$ref" : "http://schema.beckn.org/core/schema/0.7.1/person.json"
        },
        "rating" : {
            "$ref" : "http://schema.beckn.org/core/schema/0.7.1/rating.json"
        },
        "origin" : {
            "$ref" : "http://schema.beckn.org/mobility/schema/0.7.1/stop.json"
        },
        "destination" : {
            "$ref" : "http://schema.beckn.org/mobility/schema/0.7.1/stop.json"
        }
    }
}
```