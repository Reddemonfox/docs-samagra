---
title: "On Init"
metaTitle: "Beckn for Developers"
metaDescription: "Documentation for developers of the Beckn ecosystem"
---

On Init
===================

>   Send order object with payment details updated

Overview
--------

>   The BPP will send the draft order with the payment terms to the BAP.

Request
-------

### URL

>   /on_init

### Method

>  *POST*

### Request Body Schema

|**Field**|**Type**|
|---------|--------|
|context*|[ContextForOn_init](/Mobility/Schema%20Reference/contextforon_init)|
|message| [MessageForOn_init](/Mobility/Schema%20Reference/messageforon_init) |
|error| [Error](/Mobility/Schema%20Reference/error) |

### Request Body Example

```
{
    "context": {
        "domain": "mobility",
        "country": "IND",
        "city": "std:080",
        "action": "init",
        "core_version": "0.9.1",
        "bap_id": "https://mock_bap.com/",
        "bap_uri": "https://mock_bap.com/beckn/",
        "bpp_id": "https://mock_bpp.com/",
        "bpp_uri": "https://mock_bpp.com/beckn/",
        "transaction_id": "1209849124",
        "message_id": "12341242344",
        "timestamp": "2021-03-23T10:00:40.065Z"
    },
    "message": {
        "order": {
            "items":[
                {
                    "id": "sedan_spot",
                    "quantity": {
                        "count": 1
                    }
                }
            ],
            "billing": {
                "name": "John Doe",
                "address": {
                    "door": "21A",
                    "name": "ABC Appartments",
                    "locality": "HSR Layout",
                    "city": "Bengaluru",
                    "state": "Karnataka",
                    "country": "India",
                    "area_code": "560102"
                },
                "email": "user@example.com",
                "phone": "+919876543210"
            },
            "fulfillment": {
                "tracking": true,
                "start": {
                    "location": {
                        "id": "user-location",
                        "descriptor": {
                            "name": "Current user location"
                        },
                        "gps": "12.9349377,77.6055586"
                    },
                    "instructions": {
                        "name": "pick up instructions",
                        "short_desc": "Ask doorman to ring 21A"
                    },
                    "time": {
                        "label": "ETA",
                        "duration": "P12M"
                    },
                    "contact": {
                        "phone": "+919999999999",
                        "email": "test@example.com"
                    }
                },
                "end": {
                    "location": {
                        "gps": "12.914028, 77.638698"
                    }
                }
            },
            "quote": {
                "price": {
                    "currency": "INR",
                    "value": "180"
                },
                "breakup": [
                    {
                        "title": "Sedan Spot Booking",
                        "price": {
                            "currency": "INR",
                            "value": "170"
                        }
                    },
                    {
                        "title": "Service Charge",
                        "price": {
                            "currency": "INR",
                            "value": "10"
                        }
                    }
                ]
            },
            "payment": {
                "uri": "https://api.bpp.com/pay?amt=$180&mode=upi&vpa=bpp@upi",
                "tl_method": "http/get",
                "params": {
                    "amount": "180",
                    "mode": "upi",
                    "vpa": "bpp@upi"
                },
                "type": "ON-FULFILMENT",
                "status": "NOT-PAID"
            }
        }
    }
}
```

>   The order object with the quote and the payment terms are returned. Here the payment will be done on completion of the trip.

Response
--------

### Response Body Schema

|**Field**|**Type**|
|---------|--------|
|message*|{ [Ack](/Mobility/Schema%20Reference/ack) }|
|error| [Error](/Mobility/Schema%20Reference/error) |

### Response Body Example

```
{
  "message": {
    "ack": {
      "status": "ACK"
    }
  }
}
```

> Acknowldegement response

### Response Codes

| **Code**       | **Description** |
|----------------|-----------------|
| 200 | Acknowledgement of message received   |