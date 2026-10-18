# SimulatorPublication

## Example Usage

```typescript
import { SimulatorPublication } from "@continuous-labs/sdk/models";

let value: SimulatorPublication = {
  environmentId: "<id>",
  error: "<value>",
  publishedAt: null,
  status: "published",
};
```

## Fields

| Field                                                                                                                                                                 | Type                                                                                                                                                                  | Required                                                                                                                                                              | Description                                                                                                                                                           |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `environmentId`                                                                                                                                                       | *string*                                                                                                                                                              | :heavy_check_mark:                                                                                                                                                    | The workspace's default customer runtime environment.                                                                                                                 |
| `error`                                                                                                                                                               | *string*                                                                                                                                                              | :heavy_check_mark:                                                                                                                                                    | Why the last attempt failed, naming the role and repository it used, or null.                                                                                         |
| `publishedAt`                                                                                                                                                         | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                                                         | :heavy_check_mark:                                                                                                                                                    | When the image was published, or null.                                                                                                                                |
| `status`                                                                                                                                                              | [models.SimulatorPublicationStatus](../models/simulator-publication-status.md)                                                                                        | :heavy_check_mark:                                                                                                                                                    | published once the Simulator's image is in the environment's own registry; failed when the last attempt failed. Creating a Simulation in the environment tries again. |