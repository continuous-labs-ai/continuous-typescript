# WorldDataSummary

## Example Usage

```typescript
import { WorldDataSummary } from "@continuous-labs/sdk/models";

let value: WorldDataSummary = {
  assumptions: [
    "<value 1>",
    "<value 2>",
    "<value 3>",
  ],
  conditions: [
    "<value 1>",
    "<value 2>",
  ],
  records: [
    {
      count: 494879,
      entity: "<value>",
      memberIndex: 788904,
      simulatorId: "<id>",
    },
  ],
  relationships: [
    "<value 1>",
  ],
};
```

## Fields

| Field                                                                           | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `assumptions`                                                                   | *string*[]                                                                      | :heavy_check_mark:                                                              | Defaults and inferred choices used to prepare the starting data.                |
| `conditions`                                                                    | *string*[]                                                                      | :heavy_check_mark:                                                              | Record conditions and counts computed from a complete census of served records. |
| `records`                                                                       | [models.WorldRecordCount](../models/world-record-count.md)[]                    | :heavy_check_mark:                                                              | Observed starting record counts for each member and record type.                |
| `relationships`                                                                 | *string*[]                                                                      | :heavy_check_mark:                                                              | Shared relationships checked against the data and served API values.            |