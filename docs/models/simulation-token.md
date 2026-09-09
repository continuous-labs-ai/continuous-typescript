# SimulationToken

## Example Usage

```typescript
import { SimulationToken } from "@continuous-labs/sdk/models";

let value: SimulationToken = {
  expiresAt: new Date("2026-01-15T13:00:00Z"),
  token: "<redacted>",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `expiresAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Token expiration time.                                                                        |
| `token`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | New data-plane token.                                                                         |