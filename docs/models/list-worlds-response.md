# ListWorldsResponse

## Example Usage

```typescript
import { ListWorldsResponse } from "@continuous-labs/sdk/models";

let value: ListWorldsResponse = {
  nextCursor: "<value>",
  worlds: [
    {
      activeAdvanceId: null,
      createdAt: new Date("2026-01-15T12:00:00Z"),
      currentTime: new Date("2024-01-01T00:00:00Z"),
      error: null,
      id: "wld_01J8Z5X4K7M2N9P0Q1R2S3T4V7",
      instructions: "Use stable example data for each Simulator.",
      simulations: [],
      simulators: [
        "smr_01J8Z5X4K7M2N9P0Q1R2S3T4V5",
      ],
      startTime: new Date("2024-01-01T00:00:00Z"),
      status: "building",
    },
  ],
};
```

## Fields

| Field                                | Type                                 | Required                             | Description                          |
| ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ |
| `nextCursor`                         | *string*                             | :heavy_check_mark:                   | Cursor for the next page, or null.   |
| `worlds`                             | [models.World](../models/world.md)[] | :heavy_check_mark:                   | Worlds in this page.                 |