# Package

Describes the package to be transported

**Namespace** : fmd

**Type** : FmdPackage 


## JSON Schema
```
{
    "$id": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/final-mile-delivery/schema/0.7.0/fmd_package.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.0",
    "description": "Describes the package object",
    "type": "object",
    "properties": {
        "id" : {
            "type" : "string"
        },
        "parent_package_id" : {
            "$ref" : "https://raw.githubusercontent.com/beckn/protocol-specifications/master/final-mile-delivery/schema/0.7.0/fmd_package.json#/properties/id"
        },
        "descriptor" : {
            "$ref": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/core/schema/0.8.0/descriptor.json"
        },
        "category" : {
            "type" : "object",
            "properties": {
                "id" : {
                    "$ref": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/core/schema/0.8.0/category.json#/properties/id"
                }
            }
        },
        "contents" : {
            "type" : "array",
            "items" : {
                "$ref": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/final-mile-delivery/schema/0.7.0/fmd_item.json"
            }
        },
        "price" : {
            "$ref" : "https://raw.githubusercontent.com/beckn/protocol-specifications/master/core/schema/0.8.0/price.json"
        },
        "weight": {
            "$ref": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/core/schema/0.8.0/scalar.json"
        },
        "dimensions": {
            "$ref": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/core/schema/0.8.0/dimensions.json"
        }
    }
}    
```