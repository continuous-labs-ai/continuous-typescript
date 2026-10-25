# ListSimulationAdvanceEventsResponse

## Example Usage

```typescript
import { ListSimulationAdvanceEventsResponse } from "@continuous-labs/sdk/models/operations";

let value: ListSimulationAdvanceEventsResponse = {
  result: {
    events: [
      {
        at: new Date("2026-11-25T06:09:23.973Z"),
        eventId: "<id>",
        sequence: 217035,
        type: "<value>",
      },
    ],
    nextCursor: "<value>",
  },
};
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `result`                                                                                    | [models.ListClockAdvanceEventsResponse](../../models/list-clock-advance-events-response.md) | :heavy_check_mark:                                                                          | N/A                                                                                         |