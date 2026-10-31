# CreateMCPBoxRequest

## Example Usage

```typescript
import { CreateMCPBoxRequest } from "@continuous-labs/sdk/models";

let value: CreateMCPBoxRequest = {
  apiboxId: "abx_01J8Z5X4K70000000000000001",
  name: "billing-tools",
  snapshotId: "mbs_01J8Z5X4K70000000000000007",
};
```

## Fields

| Field                                                                                                  | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `apiboxId`                                                                                             | *string*                                                                                               | :heavy_check_mark:                                                                                     | An API Box of the workspace, started from the API Box Snapshot the MCP Box Snapshot was built against. |
| `metadata`                                                                                             | *any*                                                                                                  | :heavy_minus_sign:                                                                                     | Customer JSON metadata, up to 16 KiB and 64 nesting levels.                                            |
| `name`                                                                                                 | *string*                                                                                               | :heavy_minus_sign:                                                                                     | Name for the MCP Box. Omission generates a name.                                                       |
| `snapshotId`                                                                                           | *string*                                                                                               | :heavy_check_mark:                                                                                     | An MCP Box Snapshot of the workspace.                                                                  |