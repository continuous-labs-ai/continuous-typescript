# CreateMcpboxSnapshotRequestBody

## Example Usage

```typescript
import { CreateMcpboxSnapshotRequestBody } from "@continuous-labs/sdk/models/operations";

let value: CreateMcpboxSnapshotRequestBody = {
  request: {
    apiboxSnapshotId: "<id>",
  },
};
```

## Fields

| Field                                                                                                                                                                                                            | Type                                                                                                                                                                                                             | Required                                                                                                                                                                                                         | Description                                                                                                                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `document`                                                                                                                                                                                                       | [operations.CreateMcpboxSnapshotDocument](../../models/operations/create-mcpbox-snapshot-document.md)[]                                                                                                          | :heavy_minus_sign:                                                                                                                                                                                               | Vendor documentation the builder and reviewer read before they start, as repeated file parts: UTF-8 text (.md, .txt, .html, .json, .yaml, .xml, .csv) or PDF (.pdf). The documents share the request body limit. |
| `request`                                                                                                                                                                                                        | [models.BuildMCPBoxSnapshotRequest](../../models/build-mcp-box-snapshot-request.md)                                                                                                                              | :heavy_check_mark:                                                                                                                                                                                               | N/A                                                                                                                                                                                                              |