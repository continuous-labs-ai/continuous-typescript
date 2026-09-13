# ClockAdvanceStatus

Durable operation state. Poll while pending or running.

## Example Usage

```typescript
import { ClockAdvanceStatus } from "@continuous-labs/sdk/models";

let value: ClockAdvanceStatus = "running";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"pending" | "running" | "completed" | "failed" | Unrecognized<string>
```