# BuildProgressModel

The model the builder and reviewer run on, or combined, which currently runs as claude-opus-5-5.

## Example Usage

```typescript
import { BuildProgressModel } from "@continuous-labs/sdk/models";

let value: BuildProgressModel = "gpt-6-sol";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"gpt-6-astra" | "gpt-6.1-sol" | "claude-opus-5-5" | "claude-fable-5-2" | "gpt-6-sol" | "claude-fable-5-1" | "combined" | Unrecognized<string>
```