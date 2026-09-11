# WorldRecordCount

## Example Usage

```typescript
import { WorldRecordCount } from "@continuous-labs/sdk/models";

let value: WorldRecordCount = {
  count: 631083,
  entity: "<value>",
  memberIndex: 939436,
  simulatorId: "<id>",
};
```

## Fields

| Field                                                      | Type                                                       | Required                                                   | Description                                                |
| ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- |
| `count`                                                    | *number*                                                   | :heavy_check_mark:                                         | Number of stored starting records of this type.            |
| `entity`                                                   | *string*                                                   | :heavy_check_mark:                                         | Record type reported by the Simulator.                     |
| `memberIndex`                                              | *number*                                                   | :heavy_check_mark:                                         | Position in the selected Simulator list, starting at zero. |
| `simulatorId`                                              | *string*                                                   | :heavy_check_mark:                                         | Stable ID of the Simulator for this member.                |