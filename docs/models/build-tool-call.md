# BuildToolCall

## Example Usage

```typescript
import { BuildToolCall } from "@continuous-labs/sdk/models";

let value: BuildToolCall = {
  at: new Date("2025-05-21T19:51:59.913Z"),
  tool: "<value>",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `at`                                                                                          | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Time the call ran.                                                                            |
| `tool`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | Name of the tool. Arguments and output are private.                                           |