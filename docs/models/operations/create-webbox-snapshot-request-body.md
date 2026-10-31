# CreateWebboxSnapshotRequestBody

## Example Usage

```typescript
import { CreateWebboxSnapshotRequestBody } from "@continuous-labs/sdk/models/operations";

let value: CreateWebboxSnapshotRequestBody = {
  request: {
    credentialIds: [],
  },
};
```

## Fields

| Field                                                                                                                                                                                                            | Type                                                                                                                                                                                                             | Required                                                                                                                                                                                                         | Description                                                                                                                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `document`                                                                                                                                                                                                       | [operations.CreateWebboxSnapshotDocument](../../models/operations/create-webbox-snapshot-document.md)[]                                                                                                          | :heavy_minus_sign:                                                                                                                                                                                               | Vendor documentation the builder and reviewer read before they start, as repeated file parts: UTF-8 text (.md, .txt, .html, .json, .yaml, .xml, .csv) or PDF (.pdf). The documents share the request body limit. |
| `request`                                                                                                                                                                                                        | [models.BuildWebBoxSnapshotRequest](../../models/build-web-box-snapshot-request.md)                                                                                                                              | :heavy_check_mark:                                                                                                                                                                                               | N/A                                                                                                                                                                                                              |