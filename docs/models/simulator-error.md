# SimulatorError

## Example Usage

```typescript
import { SimulatorError } from "@continuous-labs/sdk/models";

let value: SimulatorError = {
  code: "build_cancelled",
  detail: "<value>",
};
```

## Fields

| Field                                                          | Type                                                           | Required                                                       | Description                                                    |
| -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- |
| `code`                                                         | [models.SimulatorErrorCode](../models/simulator-error-code.md) | :heavy_check_mark:                                             | Stable Simulator build error code.                             |
| `detail`                                                       | *string*                                                       | :heavy_check_mark:                                             | Safe human-readable error detail.                              |