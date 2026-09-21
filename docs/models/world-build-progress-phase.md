# WorldBuildProgressPhase

Agent phase: build for generation, review for the separate reviewer, finalize for author repair after review. Null when not recorded.

## Example Usage

```typescript
import { WorldBuildProgressPhase } from "@continuous-labs/sdk/models";

let value: WorldBuildProgressPhase = "finalize";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"build" | "review" | "finalize" | Unrecognized<string>
```