# Cloud Good Clean API Demo

## Purpose
This repo demonstrates the expected "Clean API" behavior for:

/vcpcloud/api/padApi/getCloudGoodList

## Requirements
- Only core product list
- Fixed pricing
- No VMOS events or campaign logic
- Stable response for backend (B2B) integration

## Problem (Current API)
The current response includes unwanted fields:

- eventPrice
- eventType
- campaignTag

These fields come from VMOS events and should NOT be included.

## Expected Response (Clean API)
```json
{
  "productId": "xxx",
  "price": 10,
  "currency": "USD",
  "duration": "1 month"
}
