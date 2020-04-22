```json
{
    "$id": "http://schema.beckn.org/mobility/schema/0.7.1/vehicle.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the properties of a vehicle used in a mobility service",
    "type": "object",
    "properties": {
        "category" : {
            "type" : "string",
            "enum" : ["CAR", "MOTORCYCLE", "BICYCLE", "TRUCK", "OTHER"]
        },
        "capacity" : {
            "type" : "integer"
        },
        "make" : {
            "type" : "string"
        },
        "model" : {
            "type" : "string"
        },
        "size" : {
            "type" : "string"
        },
        "variant" : {
            "type" : "string"
        },
        "color" : {
            "type" : "string"
        },
        "energy_type" : {
            "type" : "string",
            "enum" : ["PETROL", "DIESEL", "LPG", "CNG", "EV", "OTHER"]
        },
        "registration" : {
            "type" : "object",
                "properties" : {
                    "category" : {
                        "type" : "string",
                        "enum" : ["PERSONAL", "COMMERCIAL", "OTHER"]
                    },
                    "number" : {
                        "type" : "string"
                    }
                }

        }
        
    }        
}
```