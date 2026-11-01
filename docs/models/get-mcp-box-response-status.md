# GetMCPBoxResponseStatus

starting while its runtime boots; running while it serves MCP; stopping while it releases its runtime; stopped when it holds no runtime.

## Example Usage

```typescript
import { GetMCPBoxResponseStatus } from "@continuous-labs/sdk/models";

let value: GetMCPBoxResponseStatus = "stopped";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"starting" | "running" | "stopping" | "stopped" | Unrecognized<string>
```