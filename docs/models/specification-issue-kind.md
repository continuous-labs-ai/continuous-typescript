# SpecificationIssueKind

Whether the input is invalid, unsupported, incomplete, exceeds a build limit, or has no specific diagnosis.

## Example Usage

```typescript
import { SpecificationIssueKind } from "@continuous-labs/sdk/models";

let value: SpecificationIssueKind = "invalid";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"invalid" | "unsupported" | "incomplete" | "limit" | "unknown" | Unrecognized<string>
```