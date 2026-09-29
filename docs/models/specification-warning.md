# SpecificationWarning

## Example Usage

```typescript
import { SpecificationWarning } from "@continuous-labs/sdk/models";

let value: SpecificationWarning = {
  code: "spec.response_untyped",
  location: "<value>",
  message: "<value>",
  operations: [
    "<value 1>",
  ],
};
```

## Fields

| Field                                                                                                   | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                  | [models.SpecificationWarningCode](../models/specification-warning-code.md)                              | :heavy_check_mark:                                                                                      | Stable warning code. build.limitation marks behavior the Simulator does not serve like the real system. |
| `location`                                                                                              | *string*                                                                                                | :heavy_check_mark:                                                                                      | Readable endpoint or field affected by this warning, or the affected operations for a limitation.       |
| `message`                                                                                               | *string*                                                                                                | :heavy_check_mark:                                                                                      | What the specification declares and how the build handles it, or what the limitation is.                |
| `operations`                                                                                            | *string*[]                                                                                              | :heavy_check_mark:                                                                                      | Operation IDs a limitation affects, or empty when the warning names none.                               |