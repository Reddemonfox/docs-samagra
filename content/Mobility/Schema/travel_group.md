```json
{
    "$id": "http://schema.beckn.org/mobility/schema/0.7.1/travel_group.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes a travel group object",
    "type": "object",
    "properties": {
        "primary_traveller" : {
            "$ref" : "http://schema.beckn.org/core/schema/0.7.1/person.json"
        },
        "group_size" : {
            "type" : "integer"
        }    
    }
}
```