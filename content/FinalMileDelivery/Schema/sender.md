```json
{
    "$id": "https://schema.beckn.org/fmd/schema/0.7.1/sender.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the sender of a package",
    "type": "object",
    "properties": {
        "descriptor" : {
            "$ref" : "https://schema.beckn.org/core/schema/0.7.1/person.json"
        },
        "rating" : {
            "$ref" : "https://schema.beckn.org/core/schema/0.7.1/rating.json"
        },
        "location" : {
            "$ref" : "https://schema.beckn.org/core/schema/0.7.1/location.json"
        }    
    }
}
```