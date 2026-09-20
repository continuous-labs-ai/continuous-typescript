# SimulatorError

## Example Usage

```typescript
import { SimulatorError } from "@continuous-labs/sdk/models";

let value: SimulatorError = {
  agentMessage: "<value>",
  code: "build_failed",
  detail: "<value>",
  reason: "population_unsupported",
  validation: null,
};
```

## Fields

| Field                                                                                                                | Type                                                                                                                 | Required                                                                                                             | Description                                                                                                          |
| -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| `agentMessage`                                                                                                       | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | Plain-text explanation from the build agent, when it could not continue. At most 4096 UTF-8 bytes.                   |
| `code`                                                                                                               | [models.SimulatorErrorCode](../models/simulator-error-code.md)                                                       | :heavy_check_mark:                                                                                                   | Stable Simulator build error code.                                                                                   |
| `detail`                                                                                                             | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | Safe human-readable error detail.                                                                                    |
| `reason`                                                                                                             | [models.SimulatorErrorReason](../models/simulator-error-reason.md)                                                   | :heavy_check_mark:                                                                                                   | Bounded failure reason for selecting recovery guidance, or null when unavailable. Older servers can omit this field. |
| `validation`                                                                                                         | [models.SpecificationValidation](../models/specification-validation.md)                                              | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |