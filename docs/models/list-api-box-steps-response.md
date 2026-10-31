# ListAPIBoxStepsResponse

## Example Usage

```typescript
import { ListAPIBoxStepsResponse } from "@continuous-labs/sdk/models";

let value: ListAPIBoxStepsResponse = {
  nextCursor: "<value>",
  steps: [
    {
      label: "<value>",
      step: 128729,
      time: new Date("2024-04-20T11:53:09.010Z"),
    },
  ],
};
```

## Fields

| Field                                           | Type                                            | Required                                        | Description                                     |
| ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- |
| `nextCursor`                                    | *string*                                        | :heavy_check_mark:                              | Cursor for the next page, or null.              |
| `steps`                                         | [models.ApiboxStep](../models/apibox-step.md)[] | :heavy_check_mark:                              | Steps in this page.                             |