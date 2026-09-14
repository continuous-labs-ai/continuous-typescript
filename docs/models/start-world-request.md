# StartWorldRequest

## Example Usage

```typescript
import { StartWorldRequest } from "@continuous-labs/sdk/models";

let value: StartWorldRequest = {};
```

## Fields

| Field                                                                                                                                                                     | Type                                                                                                                                                                      | Required                                                                                                                                                                  | Description                                                                                                                                                               |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `startTime`                                                                                                                                                               | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                                                             | :heavy_minus_sign:                                                                                                                                                        | Simulated time for the first Start, in RFC 3339 format. Omission keeps the clock chosen at build. Saved business dates remain unchanged. Later starts preserve the clock. |