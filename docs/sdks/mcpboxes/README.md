# Mcpboxes

## Overview

Start MCP Boxes from MCP Box Snapshots. Each MCP Box serves its Snapshot's tools over MCP in front of an API Box. Stop, start and delete them.

### Available Operations

* [list](#list) - List MCP Boxes
* [create](#create) - Create MCP Box
* [delete](#delete) - Delete MCP Box
* [get](#get) - Get MCP Box
* [update](#update) - Update MCP Box
* [saveSnapshot](#savesnapshot) - Save MCP Box as Snapshot
* [start](#start) - Start MCP Box
* [stop](#stop) - Stop MCP Box

## list

Returns the workspace's MCP Boxes, newest first. Results can be filtered by status and Snapshot.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="list-mcpboxes" method="get" path="/v1/mcpbox" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.mcpboxes.list({});

  for await (const page of result) {
    console.log(page);
  }
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { ContinuousCore } from "@continuous-labs/sdk/core.js";
import { mcpboxesList } from "@continuous-labs/sdk/funcs/mcpboxes-list.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await mcpboxesList(continuous, {});
  if (res.ok) {
    const { value: result } = res;
    for await (const page of result) {
    console.log(page);
  }
  } else {
    console.log("mcpboxesList failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListMcpboxesRequest](../../models/operations/list-mcpboxes-request.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ListMcpboxesResponse](../../models/operations/list-mcpboxes-response.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.APIError               | 400, 401, 422                 | application/problem+json      |
| errors.APIError               | 500, 503                      | application/problem+json      |
| errors.ContinuousDefaultError | 4XX, 5XX                      | \*/\*                         |

## create

Creates an MCP Box that serves an MCP Box Snapshot's tools over MCP in front of an API Box, and starts it. The API Box must be in the workspace and started from the API Box Snapshot the MCP Box Snapshot was built against. It returns at once with status starting and the MCP Box's token; get the MCP Box until it is running. Send MCP requests to its endpoint followed by /mcp, with the token in X-Continuous-Token. The MCP Box keeps no state: its tools read and change the API Box, and a tool call while the API Box is stopped returns the API Box's refusal as a tool error.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="create-mcpbox" method="post" path="/v1/mcpbox" example="bad_request_body" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.mcpboxes.create({
    body: {
      apiboxId: "abx_01J8Z5X4K70000000000000001",
      name: "billing-tools",
      snapshotId: "mbs_01J8Z5X4K70000000000000007",
    },
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { ContinuousCore } from "@continuous-labs/sdk/core.js";
import { mcpboxesCreate } from "@continuous-labs/sdk/funcs/mcpboxes-create.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await mcpboxesCreate(continuous, {
    body: {
      apiboxId: "abx_01J8Z5X4K70000000000000001",
      name: "billing-tools",
      snapshotId: "mbs_01J8Z5X4K70000000000000007",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("mcpboxesCreate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CreateMcpboxRequest](../../models/operations/create-mcpbox-request.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.CreateMCPBoxResponse](../../models/create-mcp-box-response.md)\>**

### Errors

| Error Type                                  | Status Code                                 | Content Type                                |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| errors.APIError                             | 400, 401, 404, 408, 409, 413, 415, 422, 429 | application/problem+json                    |
| errors.APIError                             | 500, 503                                    | application/problem+json                    |
| errors.ContinuousDefaultError               | 4XX, 5XX                                    | \*/\*                                       |

## delete

Deletes an MCP Box, running or stopped. Its API Box stays. Its runtime is released after the response.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="delete-mcpbox" method="delete" path="/v1/mcpbox/{id}" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  await continuous.mcpboxes.delete({
    id: "<id>",
  });


}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { ContinuousCore } from "@continuous-labs/sdk/core.js";
import { mcpboxesDelete } from "@continuous-labs/sdk/funcs/mcpboxes-delete.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await mcpboxesDelete(continuous, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    
  } else {
    console.log("mcpboxesDelete failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.DeleteMcpboxRequest](../../models/operations/delete-mcpbox-request.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<void\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.APIError               | 401, 404                      | application/problem+json      |
| errors.APIError               | 500, 503                      | application/problem+json      |
| errors.ContinuousDefaultError | 4XX, 5XX                      | \*/\*                         |

## get

Returns an MCP Box, its status and its connection: its endpoint and token, whether it is running or stopped. Requests reach it only while it is running.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get-mcpbox" method="get" path="/v1/mcpbox/{id}" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.mcpboxes.get({
    id: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { ContinuousCore } from "@continuous-labs/sdk/core.js";
import { mcpboxesGet } from "@continuous-labs/sdk/funcs/mcpboxes-get.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await mcpboxesGet(continuous, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("mcpboxesGet failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetMcpboxRequest](../../models/operations/get-mcpbox-request.md)                                                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.GetMCPBoxResponse](../../models/get-mcp-box-response.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.APIError               | 401, 404                      | application/problem+json      |
| errors.APIError               | 500, 503                      | application/problem+json      |
| errors.ContinuousDefaultError | 4XX, 5XX                      | \*/\*                         |

## update

Renames an MCP Box or replaces its metadata. Omitted fields keep their current values.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="update-mcpbox" method="patch" path="/v1/mcpbox/{id}" example="bad_request_body" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.mcpboxes.update({
    id: "<id>",
    body: {},
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { ContinuousCore } from "@continuous-labs/sdk/core.js";
import { mcpboxesUpdate } from "@continuous-labs/sdk/funcs/mcpboxes-update.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await mcpboxesUpdate(continuous, {
    id: "<id>",
    body: {},
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("mcpboxesUpdate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.UpdateMcpboxRequest](../../models/operations/update-mcpbox-request.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.MCPBox](../../models/mcp-box.md)\>**

### Errors

| Error Type                        | Status Code                       | Content Type                      |
| --------------------------------- | --------------------------------- | --------------------------------- |
| errors.APIError                   | 400, 401, 404, 408, 413, 415, 422 | application/problem+json          |
| errors.APIError                   | 500, 503                          | application/problem+json          |
| errors.ContinuousDefaultError     | 4XX, 5XX                          | \*/\*                             |

## saveSnapshot

Saves an MCP Box and the API Box it fronts as a new MCP Box Snapshot and a new API Box Snapshot, both ready when the response returns, or neither. The API Box must be running; a paused one is woken, and it keeps running. The MCP Box Snapshot serves the MCP Box's tools and is built against the API Box Snapshot, which holds the API Box's service and current state. Create an API Box from apibox_snapshot_id, then an MCP Box from the MCP Box Snapshot in front of it. Both Snapshots outlive the Boxes. An MCP Box whose API Box was deleted returns 409 mcpbox_apibox_gone; a starting API Box returns 409 apibox_starting; a stopping or stopped one returns 409 apibox_stopped; one whose runtime cannot save its state returns 409 mcpbox_rebuild_required.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="save-mcpbox-snapshot" method="post" path="/v1/mcpbox/{id}/snapshot" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.mcpboxes.saveSnapshot({
    id: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { ContinuousCore } from "@continuous-labs/sdk/core.js";
import { mcpboxesSaveSnapshot } from "@continuous-labs/sdk/funcs/mcpboxes-save-snapshot.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await mcpboxesSaveSnapshot(continuous, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("mcpboxesSaveSnapshot failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.SaveMcpboxSnapshotRequest](../../models/operations/save-mcpbox-snapshot-request.md)                                                                                | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.MCPBoxSnapshot](../../models/mcp-box-snapshot.md)\>**

### Errors

| Error Type                             | Status Code                            | Content Type                           |
| -------------------------------------- | -------------------------------------- | -------------------------------------- |
| errors.APIError                        | 400, 401, 404, 408, 409, 413, 415, 422 | application/problem+json               |
| errors.APIError                        | 500, 503                               | application/problem+json               |
| errors.ContinuousDefaultError          | 4XX, 5XX                               | \*/\*                                  |

## start

Starts a stopped MCP Box in front of its API Box, and returns at once with status starting; get the MCP Box until it is running. Its token stays the same; its get returns it. A running, starting or stopping MCP Box returns 409 mcpbox_not_stopped, and one whose API Box was deleted 409 mcpbox_apibox_gone.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="start-mcpbox" method="post" path="/v1/mcpbox/{id}/start" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.mcpboxes.start({
    id: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { ContinuousCore } from "@continuous-labs/sdk/core.js";
import { mcpboxesStart } from "@continuous-labs/sdk/funcs/mcpboxes-start.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await mcpboxesStart(continuous, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("mcpboxesStart failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.StartMcpboxRequest](../../models/operations/start-mcpbox-request.md)                                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.MCPBox](../../models/mcp-box.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.APIError               | 401, 404, 409, 429            | application/problem+json      |
| errors.APIError               | 500, 503                      | application/problem+json      |
| errors.ContinuousDefaultError | 4XX, 5XX                      | \*/\*                         |

## stop

Stops a running MCP Box and releases its runtime; its API Box keeps running, and its token stays for the next start. It returns at once with status stopping; get the MCP Box until it is stopped. A stopped MCP Box is returned unchanged; a starting one returns 409 mcpbox_starting.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="stop-mcpbox" method="post" path="/v1/mcpbox/{id}/stop" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.mcpboxes.stop({
    id: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { ContinuousCore } from "@continuous-labs/sdk/core.js";
import { mcpboxesStop } from "@continuous-labs/sdk/funcs/mcpboxes-stop.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await mcpboxesStop(continuous, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("mcpboxesStop failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.StopMcpboxRequest](../../models/operations/stop-mcpbox-request.md)                                                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.MCPBox](../../models/mcp-box.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.APIError               | 401, 404, 409                 | application/problem+json      |
| errors.APIError               | 500, 503                      | application/problem+json      |
| errors.ContinuousDefaultError | 4XX, 5XX                      | \*/\*                         |