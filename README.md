
# Price Watcher

* REST APIs for grabbing prices

# REST APIs Overview

| Method | Version | API Path | Permission | Description
|:-----|:------|:------|:----------|:---------------|
| GET | v1.0 | /1/price/gold | Public | Live Gold Price

## GET /1/price/gold

* Grab live gold price from [usagold.com](http://www.usagold.com/mobile/)

### Query String Parameters

No query string

### Response

| Field | Type |  Description| 
|:-----|:------|:----------|
| success | integer | Backbone status
| errors  | array | Backbone status
| errfor  | array | Backbone status
| item.type   | string | Price type
| item.data   | array | Price data
| item.data.price | string | Live price
| item.data.move | string | Price move
| item.data.timestamp | string | Timestamp

### Example

Request:
```
http://priceover.net/1/price/gold
```
Response:
```
{
  "success": true,
  "errors": [],
  "errfor": {},
  "item": {
    "type": "goldprice",
    "data": [
      {
        "price": "1313",
        "move": "-6.68",
        "timestamp": "2014-07-18T07:50:47.011Z"
      }
    ]
  }
}
```