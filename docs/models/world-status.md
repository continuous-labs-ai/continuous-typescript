# WorldStatus

Current World lifecycle status.

## Example Usage

```typescript
import { WorldStatus } from "@continuous-labs/sdk/models";

let value: WorldStatus = "building";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"building" | "ready" | "running" | "stopped" | "failed" | "canceled" | Unrecognized<string>
```