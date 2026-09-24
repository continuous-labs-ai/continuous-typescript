# BuildSimulatorRequestBuilder

Legacy provider selection. Alone it selects the provider's default model (openai is gpt-6-astra, claude is claude-fable-5-1); with model it must name the model's provider.

## Example Usage

```typescript
import { BuildSimulatorRequestBuilder } from "@continuous-labs/sdk/models";

let value: BuildSimulatorRequestBuilder = "claude";
```

## Values

```typescript
"openai" | "claude"
```