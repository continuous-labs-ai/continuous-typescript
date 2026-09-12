# WorldBuildStage

Current phase of starting-data preparation.

## Example Usage

```typescript
import { WorldBuildStage } from "@continuous-labs/sdk/models";

let value: WorldBuildStage = "complete";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"planning" | "generating" | "validating" | "complete" | Unrecognized<string>
```