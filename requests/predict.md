# `/InferenceService/Predict`

## Scenario 1

1. Method: `/InferenceService/Predict`
2. Body:

```json
{
  "customerId": "C-1024",
  "features": {
    "avgOrderValue": 250000,
    "monthlyOrders": 7
  }
}
```

3. Response:

```json
{
  "customer_id": "C-1024",
  "score": 0.59,
  "label": "standard",
  "model_version": "integrated-http2-v1"
}
```

## Scenario 2

1. Method: `/InferenceService/Predict`
2. Body:

```json
{
  "customerId": "C-1025",
  "features": {
    "avgOrderValue": 125000000,
    "monthlyOrders": 100
  }
}
```

3. Response:

```json
{
  "customer_id": "C-1025",
  "score": 1,
  "label": "high_value",
  "model_version": "integrated-http2-v1"
}
```
