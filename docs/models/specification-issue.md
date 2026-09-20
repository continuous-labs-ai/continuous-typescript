# SpecificationIssue

## Example Usage

```typescript
import { SpecificationIssue } from "@continuous-labs/sdk/models";

let value: SpecificationIssue = {
  code: "<value>",
  kind: "unsupported",
  message: "<value>",
  operation: "<value>",
  path: "/opt/sbin",
  suggestion: "<value>",
};
```

## Fields

| Field                                                                                      | Type                                                                                       | Required                                                                                   | Description                                                                                |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `code`                                                                                     | *string*                                                                                   | :heavy_check_mark:                                                                         | Stable validation rule code.                                                               |
| `kind`                                                                                     | [models.SpecificationIssueKind](../models/specification-issue-kind.md)                     | :heavy_check_mark:                                                                         | Whether the input is invalid, unsupported, incomplete, or has no specific diagnosis.       |
| `message`                                                                                  | *string*                                                                                   | :heavy_check_mark:                                                                         | What needs attention at this location.                                                     |
| `operation`                                                                                | *string*                                                                                   | :heavy_check_mark:                                                                         | Affected operation ID or method and path, when available. Empty for document-level issues. |
| `path`                                                                                     | *string*                                                                                   | :heavy_check_mark:                                                                         | Location in the submitted specification, as a JSON pointer or XML path.                    |
| `suggestion`                                                                               | *string*                                                                                   | :heavy_check_mark:                                                                         | How to correct or address the problem.                                                     |