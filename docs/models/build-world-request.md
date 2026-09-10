# BuildWorldRequest

## Example Usage

```typescript
import { BuildWorldRequest } from "@continuous-labs/sdk/models";

let value: BuildWorldRequest = {
  instructions: "Use stable example data for each Simulator.",
  simulators: [
    "smr_01J8Z5X4K7M2N9P0Q1R2S3T4V5",
  ],
};
```

## Fields

| Field                                                                                                                | Type                                                                                                                 | Required                                                                                                             | Description                                                                                                          |
| -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| `instructions`                                                                                                       | *string*                                                                                                             | :heavy_minus_sign:                                                                                                   | Instructions for the builder. At most 16,384 characters and 65,536 UTF-8 bytes; must not be blank or contain U+0000. |
| `simulators`                                                                                                         | *string*[]                                                                                                           | :heavy_check_mark:                                                                                                   | Simulator IDs for the World.                                                                                         |