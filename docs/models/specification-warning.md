# SpecificationWarning

## Example Usage

```typescript
import { SpecificationWarning } from "@continuous-labs/sdk/models";

let value: SpecificationWarning = {
  code: "spec.schema_limit",
  location: "<value>",
  message: "<value>",
  operations: [
    "<value 1>",
  ],
};
```

## Fields

| Field                                                                      | Type                                                                       | Required                                                                   | Description                                                                |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `code`                                                                     | [models.SpecificationWarningCode](../models/specification-warning-code.md) | :heavy_check_mark:                                                         | Stable warning code.                                                       |
| `location`                                                                 | *string*                                                                   | :heavy_check_mark:                                                         | Readable endpoint or field affected by this warning.                       |
| `message`                                                                  | *string*                                                                   | :heavy_check_mark:                                                         | What the specification declares and how the build handles it.              |
| `operations`                                                               | *string*[]                                                                 | :heavy_check_mark:                                                         | Always empty.                                                              |