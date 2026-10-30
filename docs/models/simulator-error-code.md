# SimulatorErrorCode

Stable Simulator build error code. live_credential_rejected is a build that waited at QA for its rejected live credentials and was not resumed within 7 days.

## Example Usage

```typescript
import { SimulatorErrorCode } from "@continuous-labs/sdk/models";

let value: SimulatorErrorCode = "live_credential_rejected";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"build_failed" | "build_canceled" | "specification_validation_failed" | "live_credential_rejected" | Unrecognized<string>
```