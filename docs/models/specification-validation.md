# SpecificationValidation

## Example Usage

```typescript
import { SpecificationValidation } from "@continuous-labs/sdk/models";

let value: SpecificationValidation = {
  issues: [
    {
      code: "<value>",
      kind: "unsupported",
      location: "<value>",
      message: "<value>",
      operation: "<value>",
      suggestion: "<value>",
    },
  ],
};
```

## Fields

| Field                                                           | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `issues`                                                        | [models.SpecificationIssue](../models/specification-issue.md)[] | :heavy_check_mark:                                              | Specification validation problems. At most 20 are returned.     |