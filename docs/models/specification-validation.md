# SpecificationValidation

## Example Usage

```typescript
import { SpecificationValidation } from "@continuous-labs/sdk/models";

let value: SpecificationValidation = {
  issues: [
    {
      code: "<value>",
      kind: "unsupported",
      message: "<value>",
      operation: "<value>",
      path: "/private",
      suggestion: "<value>",
    },
  ],
};
```

## Fields

| Field                                                           | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `issues`                                                        | [models.SpecificationIssue](../models/specification-issue.md)[] | :heavy_check_mark:                                              | Specification validation problems. At most 20 are returned.     |