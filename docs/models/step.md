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

| Field                                                                                                                | Type                                                                                                                 | Required                                                                                                             | Description                                                                                                          |
| -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| `label`                                                                                                              | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | HTTP method and path of the request that produced this step, without the query string, for example POST /v1/widgets. |
| `step`                                                                                                               | *number*                                                                                                             | :heavy_check_mark:                                                                                                   | Step number. Use it as at_step when you fork.                                                                        |