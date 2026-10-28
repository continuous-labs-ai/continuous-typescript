# SimulatorSpecKind

The specification the Simulator was built from, or null until a build has read it. recorded is a Web App Simulator's: the app's origin.

## Example Usage

```typescript
import { SimulatorSpecKind } from "@continuous-labs/sdk/models";

let value: SimulatorSpecKind = "wsdl";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"openapi" | "wsdl" | "graphql" | "recorded" | Unrecognized<string>
```