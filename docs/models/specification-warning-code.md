# SpecificationWarningCode

Stable warning code. build.limitation marks behavior the Simulator does not serve like the real system. build.unrepaired marks such behavior that review did not mark a limit of the pinned contract or the scaffold, or that the build declared after review.

## Example Usage

```typescript
import { SpecificationWarningCode } from "@continuous-labs/sdk/models";

let value: SpecificationWarningCode = "spec.version_ambiguous";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"spec.enum_duplicate" | "spec.path_parameter_optional" | "spec.default_invalid" | "spec.response_untyped" | "spec.schema_limit" | "spec.operation_unservable" | "spec.version_ambiguous" | "spec.example_null" | "build.limitation" | "build.unrepaired" | Unrecognized<string>
```