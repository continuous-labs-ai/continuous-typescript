# BoxStep

## Example Usage

```typescript
import { BoxStep } from "@continuous-labs/sdk/models";

let value: BoxStep = {
  label: "<value>",
  step: 676131,
  time: new Date("2024-03-01T07:40:05.260Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `label`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | The request that made the step, or "Handle async events" for events the app scheduled.        |
| `step`                                                                                        | *number*                                                                                      | :heavy_check_mark:                                                                            | Step number, from 1 in order.                                                                 |
| `time`                                                                                        | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | When the request ran, or null when the runtime did not record it.                             |