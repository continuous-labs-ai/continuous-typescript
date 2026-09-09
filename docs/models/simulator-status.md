# SimulatorStatus

Current build status.

## Example Usage

```typescript
import { SimulatorStatus } from "@continuous-labs/sdk/models";

let value: SimulatorStatus = "canceled";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"building" | "ready" | "failed" | "canceled" | Unrecognized<string>
```