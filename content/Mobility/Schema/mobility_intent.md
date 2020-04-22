```json
{
    "$id": "http://schema.beckn.org/mobility/schema/0.7.1/mobility_intent.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version" : "0.7.1",
    "description": "Describes the mobility search request object",
    "type": "object",
    "properties": {
        "domain": {
            "$ref" : "http://schema.beckn.org/core/schema/0.7.1/domain.json"
        },
        "origin": {
            "$ref": "http://schema.beckn.org/core/schema/0.7.1/location.json"
        },
        "destination": {
            "$ref": "http://schema.beckn.org/core/schema/0.7.1/location.json"
        },
        "time" : {
            "type" : "string",
            "format" : "date-time"
        },
        "stops" : {
            "type" : "array",
            "items" : {
                "$ref" : "http://schema.beckn.org/mobility/schema/0.7.1/stop.json"
            }
        },
        "vehicle" : {
            "$ref" : "http://schema.beckn.org/mobility/schema/0.7.1/vehicle.json"
        },
        "providers" : {
            "type" : "array",
            "items" : {
                "$ref" : "http://schema.beckn.org/core/schema/0.7.1/provider.json"
            }
        },
        "payload": {
            "type": "object",
                "properties": {
                "travellers": {
                    "type": "object",
                    "properties" : {
                        "count" : {
                            "type" : "integer",
                            "minimum" : 1
                        }
                    }
                },
                "luggage": {
                    "type": "object",
                    "properties": {
                        "count": {
                            "type": "integer",
                            "minimum": 0
                        },
                        "weight_range": {
                            "$ref" : "http://schema.beckn.org/core/schema/0.7.1/scalar_range.json"
                        },
                        "dimensions": {
                            "type": "object",
                            "minimum": 0,
                            "properties": {
                                "length": {
                                    "$ref" : "http://schema.beckn.org/core/schema/0.7.1/scalar.json"
                                },
                                "breadth": {
                                    "$ref" : "http://schema.beckn.org/core/schema/0.7.1/scalar.json"
                                },
                                "height": {
                                    "$ref" : "http://schema.beckn.org/core/schema/0.7.1/scalar.json"
                                }
                            }
                        }
                    }
                }
            }
        },
        "transfer_attrs": {
            "type": "object",
            "properties": {
                "max_count": {
                    "type": "integer",
                    "default": 0
                },
                "max_distance": {
                    "$ref" : "http://schema.beckn.org/core/schema/0.7.1/scalar.json"
                }
            }
        },
        "fare_range": {
            "$ref" : "http://schema.beckn.org/core/schema/0.7.1/scalar_range.json"
        },
        "tags": {
            "type": "array",
            "items" : {
                "$ref" : "http://schema.beckn.org/core/schema/0.7.1/tag.json"
            }
        }
    }
}
```