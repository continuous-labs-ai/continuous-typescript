# SimulatorSource

workspace for a Simulator your workspace built; catalog for a read-only Simulator that Continuous publishes.

## Example Usage

```typescript
import { SimulatorSource } from "@continuous-labs/sdk/models";

let value: SimulatorSource = "catalog";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"workspace" | "catalog" | Unrecognized<string>
```