# SaveBoxSnapshotRequest

## Example Usage

```typescript
import { SaveBoxSnapshotRequest } from "@continuous-labs/sdk/models";

let value: SaveBoxSnapshotRequest = {};
```

## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `metadata`                                                  | *any*                                                       | :heavy_minus_sign:                                          | Customer JSON metadata, up to 16 KiB and 64 nesting levels. |
| `name`                                                      | *string*                                                    | :heavy_minus_sign:                                          | Name for the Snapshot. Omission generates a name.           |