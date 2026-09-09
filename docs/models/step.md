# Step

## Example Usage

```typescript
import { Step } from "@continuous-labs/sdk/models";

let value: Step = {
  label: "<value>",
  step: 475372,
};
```

## Fields

| Field                                                                             | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `label`                                                                           | *string*                                                                          | :heavy_check_mark:                                                                | Request label. It usually contains the HTTP method and path.                      |
| `step`                                                                            | *number*                                                                          | :heavy_check_mark:                                                                | Completed request number. Use this value as at_step when you fork the Simulation. |