# McpboxSnapshots

## Overview

Build MCP Box Snapshots of an MCP server's tools against a ready API Box Snapshot. MCP Boxes serve a ready Snapshot.

### Available Operations

* [list](#list) - List MCP Box Snapshots
* [create](#create) - Create MCP Box Snapshot
* [delete](#delete) - Delete MCP Box Snapshot
* [get](#get) - Get MCP Box Snapshot
* [update](#update) - Update MCP Box Snapshot
* [cancel](#cancel) - Cancel MCP Box Snapshot build
* [clone](#clone) - Clone MCP Box Snapshot
* [resume](#resume) - Resume MCP Box Snapshot build

## list

Returns the workspace's MCP Box Snapshots and the catalog's, newest first. Results can be filtered by status and source, and by the MCP Box a Snapshot was saved from.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="list-mcpbox-snapshots" method="get" path="/v1/mcpbox-snapshots" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.mcpboxSnapshots.list({});

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
import { mcpboxSnapshotsList } from "@continuous-labs/sdk/funcs/mcpbox-snapshots-list.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await mcpboxSnapshotsList(continuous, {});
  if (res.ok) {
    const { value: result } = res;
    for await (const page of result) {
    console.log(page);
  }
  } else {
    console.log("mcpboxSnapshotsList failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListMcpboxSnapshotsRequest](../../models/operations/list-mcpbox-snapshots-request.md)                                                                              | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ListMcpboxSnapshotsResponse](../../models/operations/list-mcpbox-snapshots-response.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.APIError               | 400, 401, 422                 | application/problem+json      |
| errors.APIError               | 500, 503                      | application/problem+json      |
| errors.ContinuousDefaultError | 4XX, 5XX                      | \*/\*                         |

## create

Starts an asynchronous build and returns the MCP Box Snapshot with status pending. Get the Snapshot until its status is ready, failed or canceled; MCP Boxes serve a ready one. The build makes an MCP server that answers from the API Box Snapshot it names, run in real time: with a credential, it copies the live MCP server at the credential's base_url; without one, the server its instructions or research name. Builds of every kind share one queue and the daily quota. Send multipart/form-data with a JSON part named request and optional file parts named document with vendor documentation. To build on a ready MCP Box Snapshot, set parent_id.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="create-mcpbox-snapshot" method="post" path="/v1/mcpbox-snapshots" example="bad_request_body" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.mcpboxSnapshots.create({
    body: {
      request: {},
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
import { mcpboxSnapshotsCreate } from "@continuous-labs/sdk/funcs/mcpbox-snapshots-create.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await mcpboxSnapshotsCreate(continuous, {
    body: {
      request: {},
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("mcpboxSnapshotsCreate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CreateMcpboxSnapshotRequest](../../models/operations/create-mcpbox-snapshot-request.md)                                                                            | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.CreateMcpboxSnapshotResponse](../../models/operations/create-mcpbox-snapshot-response.md)\>**

### Errors

| Error Type                        | Status Code                       | Content Type                      |
| --------------------------------- | --------------------------------- | --------------------------------- |
| errors.APIError                   | 400, 401, 404, 408, 409, 413, 415 | application/problem+json          |
| errors.APIError                   | 429                               | application/problem+json          |
| errors.APIError                   | 500                               | application/problem+json          |
| errors.APIError                   | 503                               | application/problem+json          |
| errors.ContinuousDefaultError     | 4XX, 5XX                          | \*/\*                             |

## delete

Deletes an MCP Box Snapshot. A build that is still pending or building is canceled first. The API Box Snapshot it was built against stays. A Snapshot that MCP Boxes serve returns 409 mcpbox_snapshot_in_use; delete those MCP Boxes first. While a build that names it as parent_id is pending or building, it returns 409 mcpbox_snapshot_parent_in_use; retry after the build finishes.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="delete-mcpbox-snapshot" method="delete" path="/v1/mcpbox-snapshots/{id}" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  await continuous.mcpboxSnapshots.delete({
    id: "<id>",
  });


}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { ContinuousCore } from "@continuous-labs/sdk/core.js";
import { mcpboxSnapshotsDelete } from "@continuous-labs/sdk/funcs/mcpbox-snapshots-delete.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await mcpboxSnapshotsDelete(continuous, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    
  } else {
    console.log("mcpboxSnapshotsDelete failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.DeleteMcpboxSnapshotRequest](../../models/operations/delete-mcpbox-snapshot-request.md)                                                                            | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<void\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.APIError               | 401, 403, 404, 409            | application/problem+json      |
| errors.APIError               | 500, 503                      | application/problem+json      |
| errors.ContinuousDefaultError | 4XX, 5XX                      | \*/\*                         |

## get

Returns an MCP Box Snapshot of the workspace or the catalog, and its build status.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get-mcpbox-snapshot" method="get" path="/v1/mcpbox-snapshots/{id}" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.mcpboxSnapshots.get({
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
import { mcpboxSnapshotsGet } from "@continuous-labs/sdk/funcs/mcpbox-snapshots-get.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await mcpboxSnapshotsGet(continuous, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("mcpboxSnapshotsGet failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetMcpboxSnapshotRequest](../../models/operations/get-mcpbox-snapshot-request.md)                                                                                  | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.MCPBoxSnapshot](../../models/mcp-box-snapshot.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.APIError               | 401, 404                      | application/problem+json      |
| errors.APIError               | 500, 503                      | application/problem+json      |
| errors.ContinuousDefaultError | 4XX, 5XX                      | \*/\*                         |

## update

Renames an MCP Box Snapshot or replaces its metadata. Omitted fields keep their current values. Its tools do not change. Catalog Snapshots cannot be updated.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="update-mcpbox-snapshot" method="patch" path="/v1/mcpbox-snapshots/{id}" example="bad_request_body" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.mcpboxSnapshots.update({
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
import { mcpboxSnapshotsUpdate } from "@continuous-labs/sdk/funcs/mcpbox-snapshots-update.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await mcpboxSnapshotsUpdate(continuous, {
    id: "<id>",
    body: {},
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("mcpboxSnapshotsUpdate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.UpdateMcpboxSnapshotRequest](../../models/operations/update-mcpbox-snapshot-request.md)                                                                            | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.MCPBoxSnapshot](../../models/mcp-box-snapshot.md)\>**

### Errors

| Error Type                             | Status Code                            | Content Type                           |
| -------------------------------------- | -------------------------------------- | -------------------------------------- |
| errors.APIError                        | 400, 401, 403, 404, 408, 413, 415, 422 | application/problem+json               |
| errors.APIError                        | 500, 503                               | application/problem+json               |
| errors.ContinuousDefaultError          | 4XX, 5XX                               | \*/\*                                  |

## cancel

Requests cancellation of a pending or active build and returns the Snapshot without waiting for the build to stop. Get the Snapshot until its status leaves pending or building. The build can finish before cancellation takes effect. A Snapshot whose build has settled is returned unchanged.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="cancel-mcpbox-snapshot" method="post" path="/v1/mcpbox-snapshots/{id}/cancel" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.mcpboxSnapshots.cancel({
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
import { mcpboxSnapshotsCancel } from "@continuous-labs/sdk/funcs/mcpbox-snapshots-cancel.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await mcpboxSnapshotsCancel(continuous, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("mcpboxSnapshotsCancel failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CancelMcpboxSnapshotRequest](../../models/operations/cancel-mcpbox-snapshot-request.md)                                                                            | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.MCPBoxSnapshot](../../models/mcp-box-snapshot.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.APIError               | 401, 403, 404                 | application/problem+json      |
| errors.APIError               | 500, 503                      | application/problem+json      |
| errors.ContinuousDefaultError | 4XX, 5XX                      | \*/\*                         |

## clone

Creates a ready copy of a ready MCP Box Snapshot in another workspace, without a build. The clone has a new ID and the source's artifact, documents and saved state; the source is unchanged. The clone records no credentials, since they belong to the source workspace, and no parent or source Snapshot. An API Box Snapshot of the source workspace that the MCP Box Snapshot was built against is cloned with it, and the clone is built against the copy; a catalog one is kept. The source is the caller's workspace. An API key may clone into any other workspace of its organization.

### Example Usage: bad_request_body

<!-- UsageSnippet language="typescript" operationID="clone-mcpbox-snapshot" method="post" path="/v1/mcpbox-snapshots/{id}/clone" example="bad_request_body" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.mcpboxSnapshots.clone({
    id: "<id>",
    body: {
      targetWorkspaceId: "<id>",
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
import { mcpboxSnapshotsClone } from "@continuous-labs/sdk/funcs/mcpbox-snapshots-clone.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await mcpboxSnapshotsClone(continuous, {
    id: "<id>",
    body: {
      targetWorkspaceId: "<id>",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("mcpboxSnapshotsClone failed:", res.error);
  }
}

run();
```
### Example Usage: bad_request_clone_target

<!-- UsageSnippet language="typescript" operationID="clone-mcpbox-snapshot" method="post" path="/v1/mcpbox-snapshots/{id}/clone" example="bad_request_clone_target" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.mcpboxSnapshots.clone({
    id: "<id>",
    body: {
      targetWorkspaceId: "<id>",
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
import { mcpboxSnapshotsClone } from "@continuous-labs/sdk/funcs/mcpbox-snapshots-clone.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await mcpboxSnapshotsClone(continuous, {
    id: "<id>",
    body: {
      targetWorkspaceId: "<id>",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("mcpboxSnapshotsClone failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CloneMcpboxSnapshotRequest](../../models/operations/clone-mcpbox-snapshot-request.md)                                                                              | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.MCPBoxSnapshot](../../models/mcp-box-snapshot.md)\>**

### Errors

| Error Type                                  | Status Code                                 | Content Type                                |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| errors.APIError                             | 400, 401, 403, 404, 408, 409, 413, 415, 422 | application/problem+json                    |
| errors.APIError                             | 500, 503                                    | application/problem+json                    |
| errors.ContinuousDefaultError               | 4XX, 5XX                                    | \*/\*                                       |

## resume

Resumes a build that waits, as build.waiting reports: at QA because its live credential was rejected or the live source rate limited its calls, or for more time after it used its time limit. For a credential wait, refresh the credential it names with PATCH /v1/credentials/{id} first: QA then runs again with its current value, and the build goes on to finalize. For a rate-limit wait, resume once the rate limit resets: QA then runs again. For a wait for more time, send add_seconds: the build continues where it stopped, with that much time from the resume. Returns the Snapshot, still building. A wait does not count toward the build's time limit: a build resumed from a QA wait has the time it had left when it began waiting. A build that is not waiting returns 409 mcpbox_snapshot_not_waiting.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="resume-mcpbox-snapshot" method="post" path="/v1/mcpbox-snapshots/{id}/resume" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.mcpboxSnapshots.resume({
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
import { mcpboxSnapshotsResume } from "@continuous-labs/sdk/funcs/mcpbox-snapshots-resume.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await mcpboxSnapshotsResume(continuous, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("mcpboxSnapshotsResume failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ResumeMcpboxSnapshotRequest](../../models/operations/resume-mcpbox-snapshot-request.md)                                                                            | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.MCPBoxSnapshot](../../models/mcp-box-snapshot.md)\>**

### Errors

| Error Type                             | Status Code                            | Content Type                           |
| -------------------------------------- | -------------------------------------- | -------------------------------------- |
| errors.APIError                        | 400, 401, 403, 404, 408, 409, 413, 415 | application/problem+json               |
| errors.APIError                        | 500, 503                               | application/problem+json               |
| errors.ContinuousDefaultError          | 4XX, 5XX                               | \*/\*                                  |