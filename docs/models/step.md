# Step

## Example Usage

```typescript
import { Step } from "@continuous-labs/sdk/models";

let value: Step = {
  advanceId: "<id>",
  kind: "api",
  label: "<value>",
  step: 695829,
  timeAfter: new Date("2025-03-20T01:28:28.025Z"),
  timeBefore: new Date("2024-07-31T03:22:01.106Z"),
};
```

## Fields

| Field                                                                                                                | Type                                                                                                                 | Required                                                                                                             | Description                                                                                                          |
| -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| `advanceId`                                                                                                          | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | Advance that produced this step, if any.                                                                             |
| `kind`                                                                                                               | [models.StepKind](../models/step-kind.md)                                                                            | :heavy_check_mark:                                                                                                   | api for an API write or advance for a clock advance.                                                                 |
| `label`                                                                                                              | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | HTTP method and path of the request that produced this step, without the query string, for example POST /v1/widgets. |
| `step`                                                                                                               | *number*                                                                                                             | :heavy_check_mark:                                                                                                   | Step number. Use it as at_step when you fork.                                                                        |
| `timeAfter`                                                                                                          | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                        | :heavy_check_mark:                                                                                                   | Clock after the step.                                                                                                |
| `timeBefore`                                                                                                         | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                        | :heavy_check_mark:                                                                                                   | Clock before the step.                                                                                               |