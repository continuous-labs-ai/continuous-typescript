# ListBoxStepsResponse

## Example Usage

```typescript
import { ListBoxStepsResponse } from "@continuous-labs/sdk/models";

let value: ListBoxStepsResponse = {
  nextCursor: "<value>",
  steps: [
    {
      label: "<value>",
      step: 310215,
      time: new Date("2025-10-20T07:13:50.096Z"),
    },
  ],
};
```

## Fields

| Field                                     | Type                                      | Required                                  | Description                               |
| ----------------------------------------- | ----------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| `nextCursor`                              | *string*                                  | :heavy_check_mark:                        | Cursor for the next page, or null.        |
| `steps`                                   | [models.BoxStep](../models/box-step.md)[] | :heavy_check_mark:                        | Steps in this page.                       |