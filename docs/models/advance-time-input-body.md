# AdvanceTimeInputBody

## Example Usage

```typescript
import { AdvanceTimeInputBody } from "@continuous-labs/sdk/models";

let value: AdvanceTimeInputBody = {
  to: new Date("2024-04-08T03:50:55.967Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `to`                                                                                          | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Absolute target time in RFC 3339, with at most millisecond precision.                         |