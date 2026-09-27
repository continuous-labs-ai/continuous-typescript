# AdvanceTimeRequest

## Example Usage

```typescript
import { AdvanceTimeRequest } from "@continuous-labs/sdk/models";

let value: AdvanceTimeRequest = {
  to: new Date("2024-11-02T13:08:00.478Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `to`                                                                                          | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Absolute target time in RFC 3339, with at most millisecond precision.                         |