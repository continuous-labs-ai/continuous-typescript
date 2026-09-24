# BuildWorldRequestModel

Model that builds and reviews starting data. Defaults to gpt-6-astra. Its provider is derived from the model.

## Example Usage

```typescript
import { BuildWorldRequestModel } from "@continuous-labs/sdk/models";

let value: BuildWorldRequestModel = "claude-opus-5-5";
```

## Values

```typescript
"gpt-6-astra" | "gpt-6-sol" | "claude-opus-5-5" | "claude-fable-5-1"
```