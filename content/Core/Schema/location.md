```json
{
  "$id": "http://schema.beckn.org/core/schema/0.7.1/location.json",
  "$schema": "http://json-schema.org/draft-07/schema#",
  "version" : "0.7.1",
  "description": "Describes the location of an object or a service",
  "type": "object",
  "properties": {
    "type": {
      "type": "string",
      "enum": ["gps", "address", "station_code", "area_code", "city", "country", "polygon", "3dspace"]
    },
    "gps": {
      "type": "object",
      "properties" : {
          "lat" : {
              "type" : "string"
          },
          "lon" : {
              "type" : "string"
          }
      },
      "required" : ["lat", "lon"]
    },
    "address": {
      "type": "object",
      "properties" : {
          "door" : {
              "type" : "string"
          },
          "building" : {
              "type" : "string"
          },
          "street" : {
              "type" : "string"
          },
          "area" : {
              "type" : "string"
          },
          "city" : {
              "type" : "string"
          },
          "country" : {
              "type" : "string"
          },
          "area_code" : {
              "type" : "string"
          }
      }
    },
    "station_code": {
      "type": "string"
    },
    "area_code": {
      "type": "string"
    },
    "city": {
      "type": "object",
      "properties" : {
          "name" : {"type" : "string"},
          "code" : {"type" : "string"}
      }
    },
    "country": {
      "type": "object",
      "properties" : {
          "name" : {"type" : "string"},
          "code" : {"type" : "string"}
      }
    },
    "polygon" : {
        "type" : "string"
    },
    "3dspace" : {
        "type" : "string"
    }
  },
  "required": [ "type" ]
}
```