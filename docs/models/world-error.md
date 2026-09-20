# WorldError

## Example Usage

```typescript
import { WorldError } from "@continuous-labs/sdk/models";

let value: WorldError = {
  code: "world_start_failed",
  detail: "<value>",
  reason: null,
};
```

## Fields

| Field                                                                                                                | Type                                                                                                                 | Required                                                                                                             | Description                                                                                                          |
| -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| `code`                                                                                                               | [models.WorldErrorCode](../models/world-error-code.md)                                                               | :heavy_check_mark:                                                                                                   | Stable World error code.                                                                                             |
| `detail`                                                                                                             | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | Safe human-readable error detail.                                                                                    |
| `reason`                                                                                                             | [models.WorldErrorReason](../models/world-error-reason.md)                                                           | :heavy_check_mark:                                                                                                   | Bounded failure reason for selecting recovery guidance, or null when unavailable. Older servers can omit this field. |