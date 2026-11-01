# GetAPIBoxResponseStatus

starting while its runtime boots; running while it serves requests; stopping while it saves its state; stopped when it holds no runtime. A start resumes the saved state.

## Example Usage

```typescript
import { GetAPIBoxResponseStatus } from "@continuous-labs/sdk/models";

let value: GetAPIBoxResponseStatus = "stopped";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"starting" | "running" | "stopping" | "stopped" | Unrecognized<string>
```