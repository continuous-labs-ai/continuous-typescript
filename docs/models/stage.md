# Stage

Current phase of starting-data preparation.

## Example Usage

```typescript
import { Stage } from "@continuous-labs/sdk/models";

let value: Stage = "planning";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"planning" | "generating" | "validating" | "complete" | Unrecognized<string>
```