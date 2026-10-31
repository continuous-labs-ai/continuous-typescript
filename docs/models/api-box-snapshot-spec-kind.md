# APIBoxSnapshotSpecKind

The specification the Snapshot was built from, or null until the build has read it.

## Example Usage

```typescript
import { APIBoxSnapshotSpecKind } from "@continuous-labs/sdk/models";

let value: APIBoxSnapshotSpecKind = "openapi";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"openapi" | "wsdl" | "graphql" | Unrecognized<string>
```