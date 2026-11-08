# AgentState

What the build's agent was doing when the build last checked on it, every few minutes: working while it thinks or runs a command, idle when its turn ended without a tool call, waiting_for_limit while a subscription model waits for its usage limit to reset. Null when the build is not running, while it waits for the requester, or for a build recorded before agents reported it.

## Example Usage

```typescript
import { AgentState } from "@continuous-labs/sdk/models";

let value: AgentState = "working";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"working" | "idle" | "waiting_for_limit" | Unrecognized<string>
```