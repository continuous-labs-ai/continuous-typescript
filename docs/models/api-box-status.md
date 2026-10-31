# APIBoxStatus

starting while its runtime boots; running while it serves requests; stopping while it saves its state; stopped when it holds no runtime. A start resumes the saved state.

## Example Usage

```typescript
import { APIBoxStatus } from "@continuous-labs/sdk/models";

let value: APIBoxStatus = "starting";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"starting" | "running" | "stopping" | "stopped" | Unrecognized<string>
```