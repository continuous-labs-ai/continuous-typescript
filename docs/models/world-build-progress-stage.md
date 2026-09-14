# WorldBuildProgressStage

Current phase of starting-data preparation.

## Example Usage

```typescript
import { WorldBuildProgressStage } from "@continuous-labs/sdk/models";

let value: WorldBuildProgressStage = "generating";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"planning" | "generating" | "validating" | "complete" | Unrecognized<string>
```