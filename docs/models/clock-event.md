# ClockEvent

## Example Usage

```typescript
import { ClockEvent } from "@continuous-labs/sdk/models";

let value: ClockEvent = {
  at: new Date("2025-10-30T11:32:54.483Z"),
  eventId: "<id>",
  sequence: 173898,
  type: "<value>",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `at`                                                                                          | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Simulated time observed by this event handler.                                                |
| `eventId`                                                                                     | *string*                                                                                      | :heavy_check_mark:                                                                            | Scheduled event ID.                                                                           |
| `sequence`                                                                                    | *number*                                                                                      | :heavy_check_mark:                                                                            | Persisted insertion order for events due at the same time.                                    |
| `type`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | Declared event type.                                                                          |