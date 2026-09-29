# SpecificationWarningCode

Stable warning code. build.limitation marks behavior the Simulator does not serve like the real system.

## Example Usage

```typescript
import { SpecificationWarningCode } from "@continuous-labs/sdk/models";

let value: SpecificationWarningCode = "spec.response_untyped";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"spec.enum_duplicate" | "spec.path_parameter_optional" | "spec.default_invalid" | "spec.response_untyped" | "spec.schema_limit" | "build.limitation" | Unrecognized<string>
```