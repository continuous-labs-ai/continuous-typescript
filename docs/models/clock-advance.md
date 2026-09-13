# ClockAdvance

## Example Usage

```typescript
import { ClockAdvance } from "@continuous-labs/sdk/models";

let value: ClockAdvance = {
  error: {
    code: "<value>",
    detail: "<value>",
  },
  eventCount: 214396,
  from: new Date("2024-03-05T09:39:26.311Z"),
  id: "<id>",
  members: [
    {
      error: {
        code: "<value>",
        detail: "<value>",
      },
      eventCount: 125513,
      simulationId: "<id>",
      status: "failed",
      step: 182548,
    },
  ],
  status: "failed",
  step: 395283,
  to: new Date("2024-04-02T01:22:26.699Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `error`                                                                                       | [models.ResourceError](../models/resource-error.md)                                           | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `eventCount`                                                                                  | *number*                                                                                      | :heavy_check_mark:                                                                            | Number of committed event executions.                                                         |
| `from`                                                                                        | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Clock before the requested advance.                                                           |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Stable clock advance operation ID.                                                            |
| `members`                                                                                     | [models.ClockAdvanceMember](../models/clock-advance-member.md)[]                              | :heavy_check_mark:                                                                            | Progress for each participating Simulation.                                                   |
| `status`                                                                                      | [models.ClockAdvanceStatus](../models/clock-advance-status.md)                                | :heavy_check_mark:                                                                            | Durable operation state. Poll while pending or running.                                       |
| `step`                                                                                        | *number*                                                                                      | :heavy_check_mark:                                                                            | Committed local step, or null for no change or a World operation.                             |
| `to`                                                                                          | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Requested absolute target time.                                                               |