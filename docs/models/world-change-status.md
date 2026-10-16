# WorldChangeStatus

Durable change state. Poll while pending, building, or applying.

## Example Usage

```typescript
import { WorldChangeStatus } from "@continuous-labs/sdk/models";

let value: WorldChangeStatus = "completed";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"pending" | "building" | "applying" | "completed" | "failed" | Unrecognized<string>
```