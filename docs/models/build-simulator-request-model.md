# BuildSimulatorRequestModel

Model that builds and reviews the Simulator. Defaults to gpt-6-astra. Its provider is derived from the model.

## Example Usage

```typescript
import { BuildSimulatorRequestModel } from "@continuous-labs/sdk/models";

let value: BuildSimulatorRequestModel = "claude-fable-5-1";
```

## Values

```typescript
"gpt-6-astra" | "gpt-6-sol" | "claude-opus-5-5" | "claude-fable-5-1"
```