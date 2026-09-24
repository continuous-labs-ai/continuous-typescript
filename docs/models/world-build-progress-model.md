# WorldBuildProgressModel

The model the builder and reviewer run on, or null for a build created before provider selection. A build recorded before model selection reports its provider's default.

## Example Usage

```typescript
import { WorldBuildProgressModel } from "@continuous-labs/sdk/models";

let value: WorldBuildProgressModel = "gpt-6-astra";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"gpt-6-astra" | "gpt-6-sol" | "claude-opus-5-5" | "claude-fable-5-1" | Unrecognized<string>
```