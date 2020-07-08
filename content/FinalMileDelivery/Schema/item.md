Describes an item in a Package

**Namespace** : fmd

**Type** : FmdItem


## JSON Schema
```
{
    "$id": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/final-mile-delivery/schema/0.7.0/fmd_item.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.0",
    "description": "Describes an item in an FMD package",
    "allOf" : [
        {
            "$ref" : "https://raw.githubusercontent.com/beckn/protocol-specifications/master/core/schema/0.8.0/item.json"
        },
        {
            "properties": {
                "fragile" : {
                    "type" : "boolean"
                }
            }
        }
    ]
}
```