# SimulatorSpecKind

The specification the Simulator was built from, or null until a build has read it.

## Example Usage

```typescript
import { SimulatorSpecKind } from "@continuous-labs/sdk/models";

let value: SimulatorSpecKind = "wsdl";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"openapi" | "wsdl" | "graphql" | Unrecognized<string>
```