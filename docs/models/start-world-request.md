# StartWorldRequest

## Example Usage

```typescript
import { StartWorldRequest } from "@continuous-labs/sdk/models";

let value: StartWorldRequest = {};
```

## Fields

| Field                                                                                                                                                                       | Type                                                                                                                                                                        | Required                                                                                                                                                                    | Description                                                                                                                                                                 |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `startTime`                                                                                                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                                                               | :heavy_minus_sign:                                                                                                                                                          | Initial simulated time for the first Start, in RFC 3339 format. Omission uses 2024-01-01T00:00:00Z. Saved business dates remain unchanged. Later starts preserve the clock. |