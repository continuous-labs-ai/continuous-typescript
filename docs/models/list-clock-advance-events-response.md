# ListClockAdvanceEventsResponse

## Example Usage

```typescript
import { ListClockAdvanceEventsResponse } from "@continuous-labs/sdk/models";

let value: ListClockAdvanceEventsResponse = {
  events: [],
  nextCursor: "<value>",
};
```

## Fields

| Field                                           | Type                                            | Required                                        | Description                                     |
| ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- |
| `events`                                        | [models.ClockEvent](../models/clock-event.md)[] | :heavy_check_mark:                              | Committed events in execution order.            |
| `nextCursor`                                    | *string*                                        | :heavy_check_mark:                              | Cursor for the next page, or null.              |