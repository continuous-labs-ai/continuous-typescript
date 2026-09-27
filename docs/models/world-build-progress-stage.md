# WorldBuildProgressStage

planning while the build prepares; generating while the builder writes starting data; validating while the data is checked through the Simulators' APIs; reviewing while the separate reviewer checks it; complete when verified starting data is saved.

## Example Usage

```typescript
import { WorldBuildProgressStage } from "@continuous-labs/sdk/models";

let value: WorldBuildProgressStage = "generating";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"planning" | "generating" | "validating" | "reviewing" | "complete" | Unrecognized<string>
```