# Limitation

## Example Usage

```typescript
import { Limitation } from "@continuous-labs/sdk/models";

let value: Limitation = {
  location: "<value>",
  message: "<value>",
  operations: [
    "<value 1>",
    "<value 2>",
  ],
  reviewed: false,
};
```

## Fields

| Field                                                                                                                                                                                         | Type                                                                                                                                                                                          | Required                                                                                                                                                                                      | Description                                                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `location`                                                                                                                                                                                    | *string*                                                                                                                                                                                      | :heavy_check_mark:                                                                                                                                                                            | The operations the limitation affects, readably, or Simulator when it names none.                                                                                                             |
| `message`                                                                                                                                                                                     | *string*                                                                                                                                                                                      | :heavy_check_mark:                                                                                                                                                                            | What the Simulator does differently from the real system.                                                                                                                                     |
| `operations`                                                                                                                                                                                  | *string*[]                                                                                                                                                                                    | :heavy_check_mark:                                                                                                                                                                            | Operation IDs the limitation affects, or empty when it names none.                                                                                                                            |
| `reviewed`                                                                                                                                                                                    | *boolean*                                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                                            | Whether review confirmed that the pinned contract or the scaffold cannot express the correct behavior. False for a limitation the build recorded after review or that review did not confirm. |