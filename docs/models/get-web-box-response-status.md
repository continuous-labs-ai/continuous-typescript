# GetWebBoxResponseStatus

starting while its runtime boots; running while it serves its app; stopping while it saves its state; stopped when it holds no runtime. A start resumes the saved state.

## Example Usage

```typescript
import { GetWebBoxResponseStatus } from "@continuous-labs/sdk/models";

let value: GetWebBoxResponseStatus = "stopping";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"starting" | "running" | "stopping" | "stopped" | Unrecognized<string>
```