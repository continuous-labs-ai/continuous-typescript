# ApiboxStep

## Example Usage

```typescript
import { ApiboxStep } from "@continuous-labs/sdk/models";

let value: ApiboxStep = {
  label: "<value>",
  step: 7551,
  time: null,
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `label`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | The request that made the step.                                                               |
| `step`                                                                                        | *number*                                                                                      | :heavy_check_mark:                                                                            | Step number, from 1 in order.                                                                 |
| `time`                                                                                        | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | When the request ran, or null when the runtime did not record it.                             |