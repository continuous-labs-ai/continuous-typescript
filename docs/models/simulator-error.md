# SimulatorError

## Example Usage

```typescript
import { SimulatorError } from "@continuous-labs/sdk/models";

let value: SimulatorError = {
  agentMessage: "<value>",
  code: "build_failed",
  detail: "<value>",
  reason: "service_unavailable",
  validation: null,
};
```

## Fields

| Field                                                                                                                                                         | Type                                                                                                                                                          | Required                                                                                                                                                      | Description                                                                                                                                                   |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `agentMessage`                                                                                                                                                | *string*                                                                                                                                                      | :heavy_check_mark:                                                                                                                                            | Plain-text explanation from the build agent when it could not continue, or the problems the check of the build's index found. At most 4096 UTF-8 bytes.       |
| `code`                                                                                                                                                        | [models.SimulatorErrorCode](../models/simulator-error-code.md)                                                                                                | :heavy_check_mark:                                                                                                                                            | Stable Simulator build error code. live_credential_rejected is a build that waited at QA for its rejected live credentials and was not resumed within 7 days. |
| `detail`                                                                                                                                                      | *string*                                                                                                                                                      | :heavy_check_mark:                                                                                                                                            | Safe human-readable error detail.                                                                                                                             |
| `reason`                                                                                                                                                      | [models.Reason](../models/reason.md)                                                                                                                          | :heavy_check_mark:                                                                                                                                            | Bounded failure reason for selecting recovery guidance, or null when unavailable.                                                                             |
| `validation`                                                                                                                                                  | [models.SpecificationValidation](../models/specification-validation.md)                                                                                       | :heavy_check_mark:                                                                                                                                            | N/A                                                                                                                                                           |