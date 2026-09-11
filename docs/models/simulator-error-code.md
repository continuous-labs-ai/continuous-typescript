# SimulatorErrorCode

Stable Simulator build error code.

## Example Usage

```typescript
import { SimulatorErrorCode } from "@continuous-labs/sdk/models";

let value: SimulatorErrorCode = "build_cancelled";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"build_failed" | "build_cancelled" | Unrecognized<string>
```