# WorldBuildBuilder

Selected model provider. Absent for builds created before provider selection.

## Example Usage

```typescript
import { WorldBuildBuilder } from "@continuous-labs/sdk/models";

let value: WorldBuildBuilder = "claude";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"openai" | "claude" | Unrecognized<string>
```