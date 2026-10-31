# WebBoxStatus

starting while its runtime boots; running while it serves its app; stopping while it saves its state; stopped when it holds no runtime. A start resumes the saved state.

## Example Usage

```typescript
import { WebBoxStatus } from "@continuous-labs/sdk/models";

let value: WebBoxStatus = "stopped";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"starting" | "running" | "stopping" | "stopped" | Unrecognized<string>
```