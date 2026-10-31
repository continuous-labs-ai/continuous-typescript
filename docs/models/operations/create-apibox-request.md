# CreateApiboxRequest

## Example Usage

```typescript
import { CreateApiboxRequest } from "@continuous-labs/sdk/models/operations";

let value: CreateApiboxRequest = {
  body: {
    metadata: {
      "customer_id": "cust_123",
    },
    name: "billing-sandbox",
    snapshotId: "abs_01J8Z5X4K70000000000000002",
  },
};
```

## Fields

| Field                                                                                                                                                                                           | Type                                                                                                                                                                                            | Required                                                                                                                                                                                        | Description                                                                                                                                                                                     | Example                                                                                                                                                                                         |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `idempotencyKey`                                                                                                                                                                                | *string*                                                                                                                                                                                        | :heavy_minus_sign:                                                                                                                                                                              | Optional key for retrying this create safely. A retry with the same key and request returns the same API Box and token. The same key with a different request returns 409 idempotency_conflict. |                                                                                                                                                                                                 |
| `body`                                                                                                                                                                                          | [models.CreateAPIBoxRequest](../../models/create-api-box-request.md)                                                                                                                            | :heavy_check_mark:                                                                                                                                                                              | N/A                                                                                                                                                                                             | {<br/>"metadata": {<br/>"customer_id": "cust_123"<br/>},<br/>"name": "billing-sandbox",<br/>"snapshot_id": "abs_01J8Z5X4K70000000000000002"<br/>}                                               |