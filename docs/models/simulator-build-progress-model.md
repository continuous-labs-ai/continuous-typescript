# SimulatorBuildProgressModel

The model the builder and reviewer run on. A build recorded before model selection reports its provider's default.

## Example Usage

```typescript
import { SimulatorBuildProgressModel } from "@continuous-labs/sdk/models";

let value: SimulatorBuildProgressModel = "gpt-6-astra";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"gpt-6-astra" | "gpt-6-sol" | "claude-opus-5-5" | "claude-fable-5-1" | Unrecognized<string>
```