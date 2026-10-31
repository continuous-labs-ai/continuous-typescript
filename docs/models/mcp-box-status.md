# MCPBoxStatus

starting while its runtime boots; running while it serves MCP; stopping while it releases its runtime; stopped when it holds no runtime.

## Example Usage

```typescript
import { MCPBoxStatus } from "@continuous-labs/sdk/models";

let value: MCPBoxStatus = "stopped";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"starting" | "running" | "stopping" | "stopped" | Unrecognized<string>
```