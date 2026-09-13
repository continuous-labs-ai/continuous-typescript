# ListAdvanceEventsOutputBody

## Example Usage

```typescript
import { ListAdvanceEventsOutputBody } from "@continuous-labs/sdk/models";

let value: ListAdvanceEventsOutputBody = {
  events: [
    {
      at: new Date("2024-08-27T23:33:25.418Z"),
      eventId: "<id>",
      sequence: 709886,
      type: "<value>",
    },
  ],
  nextCursor: "<value>",
};
```

## Fields

| Field                                           | Type                                            | Required                                        | Description                                     |
| ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- |
| `events`                                        | [models.ClockEvent](../models/clock-event.md)[] | :heavy_check_mark:                              | Committed events in execution order.            |
| `nextCursor`                                    | *string*                                        | :heavy_check_mark:                              | Cursor for the next page, or null.              |