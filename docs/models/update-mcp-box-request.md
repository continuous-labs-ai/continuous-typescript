# UpdateMCPBoxRequest

## Example Usage

```typescript
import { UpdateMCPBoxRequest } from "@continuous-labs/sdk/models";

let value: UpdateMCPBoxRequest = {};
```

## Fields

| Field                                                                                        | Type                                                                                         | Required                                                                                     | Description                                                                                  |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `metadata`                                                                                   | *any*                                                                                        | :heavy_minus_sign:                                                                           | Replacement customer JSON metadata, up to 16 KiB and 64 nesting levels, or null to clear it. |
| `name`                                                                                       | *string*                                                                                     | :heavy_minus_sign:                                                                           | New API Box name.                                                                            |