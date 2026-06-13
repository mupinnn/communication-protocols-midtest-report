# `/InferenceService/BatchPredict`

1. Method: `/InferenceService/BatchPredict`
2. Body:

```json
{
  "items": [
    {
      "customerId": "C-1001",
      "features": {
        "avgOrderValue": 150000,
        "monthlyOrders": 3
      }
    },
    {
      "customerId": "C-1002",
      "features": {
        "avgOrderValue": 420000,
        "monthlyOrders": 9
      }
    }
  ]
}
```

3. Response:

```json
{
  "predictions": [
    {
      "customer_id": "C-1001",
      "score": 0.3,
      "label": "standard",
      "model_version": "integrated-http2-v1"
    },
    {
      "customer_id": "C-1002",
      "score": 0.867,
      "label": "high_value",
      "model_version": "integrated-http2-v1"
    }
  ]
}
```
