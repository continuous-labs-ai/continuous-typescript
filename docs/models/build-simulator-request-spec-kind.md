# BuildSimulatorRequestSpecKind

Source specification format. Omission detects the format; GraphQL SDL needs graphql, and a GraphQL introspection result is stored as SDL.

## Example Usage

```typescript
import { BuildSimulatorRequestSpecKind } from "@continuous-labs/sdk/models";

let value: BuildSimulatorRequestSpecKind = "openapi";
```

## Values

```typescript
"openapi" | "wsdl" | "graphql"
```