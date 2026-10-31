# CreateWebboxRequest

## Example Usage

```typescript
import { CreateWebboxRequest } from "@continuous-labs/sdk/models/operations";

let value: CreateWebboxRequest = {
  body: {
    name: "crm-sandbox",
    snapshotId: "wbs_01J8Z5X4K70000000000000005",
  },
};
```

## Fields

| Field                                                                                                                                                                                 | Type                                                                                                                                                                                  | Required                                                                                                                                                                              | Description                                                                                                                                                                           | Example                                                                                                                                                                               |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `idempotencyKey`                                                                                                                                                                      | *string*                                                                                                                                                                              | :heavy_minus_sign:                                                                                                                                                                    | Optional key for retrying this create safely. A retry with the same key and request returns the same Web Box. The same key with a different request returns 409 idempotency_conflict. |                                                                                                                                                                                       |
| `body`                                                                                                                                                                                | [models.CreateWebBoxRequest](../../models/create-web-box-request.md)                                                                                                                  | :heavy_check_mark:                                                                                                                                                                    | N/A                                                                                                                                                                                   | {<br/>"name": "crm-sandbox",<br/>"snapshot_id": "wbs_01J8Z5X4K70000000000000005"<br/>}                                                                                                |