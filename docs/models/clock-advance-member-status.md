# ClockAdvanceMemberStatus

Whether this member is pending, committed, or rolled back after a deterministic failure.

## Example Usage

```typescript
import { ClockAdvanceMemberStatus } from "@continuous-labs/sdk/models";

let value: ClockAdvanceMemberStatus = "completed";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"pending" | "completed" | "failed" | Unrecognized<string>
```