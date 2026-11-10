# BuildProgressModel

The model the builder and reviewer run on, or combined, which currently runs as claude-opus-5-5. A build recorded before model selection reports its provider's default.

## Example Usage

```typescript
import { BuildProgressModel } from "@continuous-labs/sdk/models";

let value: BuildProgressModel = "claude-fable-5-1";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"gpt-6-astra" | "gpt-6.1-sol" | "claude-opus-5-5" | "claude-fable-5-1" | "gpt-6-sol" | "combined" | Unrecognized<string>
```