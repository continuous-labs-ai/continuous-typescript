# SpecificationWarningCode

Stable warning code.

## Example Usage

```typescript
import { SpecificationWarningCode } from "@continuous-labs/sdk/models";

let value: SpecificationWarningCode = "spec.operation_unservable";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"spec.enum_duplicate" | "spec.path_parameter_optional" | "spec.default_invalid" | "spec.response_untyped" | "spec.schema_limit" | "spec.operation_unservable" | "spec.version_ambiguous" | "spec.example_null" | Unrecognized<string>
```