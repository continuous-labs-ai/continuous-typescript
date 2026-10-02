# ClockAdvanceMember

## Example Usage

```typescript
import { ClockAdvanceMember } from "@continuous-labs/sdk/models";

let value: ClockAdvanceMember = {
  error: {
    code: "<value>",
    detail: "<value>",
  },
  eventCount: 793176,
  simulationId: "<id>",
  status: "pending",
  step: 54531,
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `error`                                                                                       | [models.ResourceError](../models/resource-error.md)                                           | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `eventCount`                                                                                  | *number*                                                                                      | :heavy_check_mark:                                                                            | Number of committed event executions.                                                         |
| `reached`                                                                                     | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | Clock time a failed advance reached with the batches it kept committed.                       |
| `simulationId`                                                                                | *string*                                                                                      | :heavy_check_mark:                                                                            | Member Simulation ID.                                                                         |
| `status`                                                                                      | [models.ClockAdvanceMemberStatus](../models/clock-advance-member-status.md)                   | :heavy_check_mark:                                                                            | Whether this member is pending, committed, failed, or skipped because it is not running.      |
| `step`                                                                                        | *number*                                                                                      | :heavy_check_mark:                                                                            | Last committed local step, or null when the advance committed none.                           |