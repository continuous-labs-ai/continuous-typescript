# ClockAdvanceMemberStatus

Whether this member is pending, committed, failed, or skipped because it is not running.

## Example Usage

```typescript
import { ClockAdvanceMemberStatus } from "@continuous-labs/sdk/models";

let value: ClockAdvanceMemberStatus = "completed";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"pending" | "completed" | "failed" | "skipped" | Unrecognized<string>
```