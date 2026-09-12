# SimulatorBuildProgressStage

derive while the effective spec, build skeleton, and sandbox are prepared; build while the coding loop runs; assemble while an accepted artifact publishes.

## Example Usage

```typescript
import { SimulatorBuildProgressStage } from "@continuous-labs/sdk/models";

let value: SimulatorBuildProgressStage = "build";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"derive" | "build" | "assemble" | Unrecognized<string>
```