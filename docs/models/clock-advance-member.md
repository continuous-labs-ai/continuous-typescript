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

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `error`                                                                                  | [models.ResourceError](../models/resource-error.md)                                      | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `eventCount`                                                                             | *number*                                                                                 | :heavy_check_mark:                                                                       | Number of committed event executions.                                                    |
| `simulationId`                                                                           | *string*                                                                                 | :heavy_check_mark:                                                                       | Member Simulation ID.                                                                    |
| `status`                                                                                 | [models.ClockAdvanceMemberStatus](../models/clock-advance-member-status.md)              | :heavy_check_mark:                                                                       | Whether this member is pending, committed, failed, or skipped because it is not running. |
| `step`                                                                                   | *number*                                                                                 | :heavy_check_mark:                                                                       | Committed local step, or null for no change or a failed advance.                         |