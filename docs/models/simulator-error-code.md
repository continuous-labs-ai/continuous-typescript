# SimulatorErrorCode

Stable Simulator build error code.

## Example Usage

```typescript
import { SimulatorErrorCode } from "@continuous-labs/sdk/models";

let value: SimulatorErrorCode = "specification_validation_failed";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"build_failed" | "build_cancelled" | "specification_validation_failed" | Unrecognized<string>
```