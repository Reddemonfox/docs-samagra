```json
{
    "$id": "https://raw.githubusercontent.com/beckn/protocol-specifications/master/healthcare/schema/0.5.0/prescription.json",
    "$schema": "http://json-schema.org/draft-07/schema#",
    "version": "0.5.0",
    "description": "Describes a doctor's prescription",
    "type": "object",
    "properties": {
        "clinicalnotes": {
            "$ref": "#/components/schemas/clinicalnotes"
        },
        "diagnosis": {
            "type": "array",
            "items": {
                "type": "object",
                "properties": {
                    "diagnosis": {
                        "$ref": "#/components/schemas/taxonomyitem"
                    }
                }
            }
        },
        "medicines": {
            "type": "array",
            "items": {
                "type": "object",
                "properties": {
                    "medication": {
                        "$ref": "#/components/schemas/taxonomyitem"
                    },
                    "for": {
                        "type": "array",
                        "items": {
                            "type": "string"
                        }
                    },
                    "regimen": {
                        "type": "array",
                        "items": {
                            "type": "object",
                            "properties": {
                                "regimen": {
                                    "type": "string"
                                },
                                "start": {
                                    "$ref": "https://schema.beckn.org/core/schema/0.7.1/time.json"
                                },
                                "duration": {
                                    "type": "number"
                                }
                            }
                        }
                    }
                }
            }
        },
        "diagnostictests": {
            "type": "array",
            "items": {
                "type": "object",
                "properties": {
                    "test": {
                        "$ref": "#/components/schemas/taxonomyitem"
                    },
                    "additional_info": {
                        "type": "string"
                    }
                }
            }
        },
        "general_advice": {
            "$ref": "#/components/schemas/objectmap"
        },
        "followup": {
            "$ref": "https://schema.beckn.org/core/schema/0.7.1/time.json"
        },
        "referral": {
            "type": "object",
            "properties": {
                "referto_speciality": {
                    "type": "string"
                },
                "notes": {
                    "type": "string"
                }
            }
        },
        "doctor": {
            "$ref": "#/components/schemas/doctor"
        }
    }
}
```