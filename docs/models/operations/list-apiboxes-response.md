# ListApiboxesResponse

## Example Usage

```typescript
import { ListApiboxesResponse } from "@continuous-labs/sdk/models/operations";

let value: ListApiboxesResponse = {
  result: {
    apiboxes: [
      {
        createdAt: new Date("2024-03-17T19:39:51.908Z"),
        deletedAt: new Date("2026-05-16T15:08:53.108Z"),
        endpoint: "https://fearless-fax.net",
        error: {
          code: "mcpbox_apibox_unissued",
          detail: "<value>",
        },
        id: "<id>",
        includeSampleData: false,
        lastActiveAt: new Date("2024-11-18T03:55:14.254Z"),
        metadata: "<value>",
        name: "<value>",
        snapshotId: "<id>",
        status: "running",
        statusChangedAt: new Date("2024-03-03T15:15:35.235Z"),
      },
    ],
    nextCursor: "<value>",
  },
};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `result`                                                               | [models.ListAPIBoxesResponse](../../models/list-api-boxes-response.md) | :heavy_check_mark:                                                     | N/A                                                                    |