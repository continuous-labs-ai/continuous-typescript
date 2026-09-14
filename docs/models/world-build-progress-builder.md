# WorldBuildProgressBuilder

Selected model provider, or null for a build created before provider selection.

## Example Usage

```typescript
import { WorldBuildProgressBuilder } from "@continuous-labs/sdk/models";

let value: WorldBuildProgressBuilder = "openai";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"openai" | "claude" | Unrecognized<string>
```