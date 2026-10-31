# MCPBoxSnapshotStatus

pending while waiting for capacity; building while the build runs; ready when MCP Boxes can serve it; failed when the build failed; canceled when a cancel request took effect.

## Example Usage

```typescript
import { MCPBoxSnapshotStatus } from "@continuous-labs/sdk/models";

let value: MCPBoxSnapshotStatus = "pending";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"pending" | "building" | "ready" | "failed" | "canceled" | Unrecognized<string>
```