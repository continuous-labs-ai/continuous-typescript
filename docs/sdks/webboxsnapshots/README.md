# WebboxSnapshots

## Overview

Build Web Box Snapshots from a vendor's live web app, or use the catalog's. Web Boxes start from a ready Snapshot.

### Available Operations

* [list](#list) - List Web Box Snapshots
* [create](#create) - Create Web Box Snapshot
* [delete](#delete) - Delete Web Box Snapshot
* [get](#get) - Get Web Box Snapshot
* [update](#update) - Update Web Box Snapshot
* [cancel](#cancel) - Cancel Web Box Snapshot build
* [clone](#clone) - Clone Web Box Snapshot
* [resume](#resume) - Resume Web Box Snapshot build

## list

Returns the workspace's Web Box Snapshots and the catalog's, newest first. Results can be filtered by source and status, and by the Web Box a Snapshot was saved from.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="list-webbox-snapshots" method="get" path="/v1/webbox-snapshots" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.webboxSnapshots.list({});

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
import { webboxSnapshotsList } from "@continuous-labs/sdk/funcs/webbox-snapshots-list.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await webboxSnapshotsList(continuous, {});
  if (res.ok) {
    const { value: result } = res;
    for await (const page of result) {
    console.log(page);
  }
  } else {
    console.log("webboxSnapshotsList failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListWebboxSnapshotsRequest](../../models/operations/list-webbox-snapshots-request.md)                                                                              | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ListWebboxSnapshotsResponse](../../models/operations/list-webbox-snapshots-response.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.APIError               | 400, 401, 422                 | application/problem+json      |
| errors.APIError               | 500, 503                      | application/problem+json      |
| errors.ContinuousDefaultError | 4XX, 5XX                      | \*/\*                         |

## create

Starts an asynchronous build and returns the Web Box Snapshot with status pending. Get the Snapshot until its status is ready, failed or canceled; Web Boxes start from a ready one. The build runs in real time: the builder and QA use the vendor's live web app through its login credential, and the built app has no simulated clock. Builds of every kind share one queue and the daily quota. Send multipart/form-data with a JSON part named request and optional file parts named document with vendor documentation. To build on a ready Snapshot, set parent_id.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="create-webbox-snapshot" method="post" path="/v1/webbox-snapshots" example="bad_request_body" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.webboxSnapshots.create({
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
import { webboxSnapshotsCreate } from "@continuous-labs/sdk/funcs/webbox-snapshots-create.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await webboxSnapshotsCreate(continuous, {
    body: {
      request: {},
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("webboxSnapshotsCreate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CreateWebboxSnapshotRequest](../../models/operations/create-webbox-snapshot-request.md)                                                                            | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.CreateWebboxSnapshotResponse](../../models/operations/create-webbox-snapshot-response.md)\>**

### Errors

| Error Type                        | Status Code                       | Content Type                      |
| --------------------------------- | --------------------------------- | --------------------------------- |
| errors.APIError                   | 400, 401, 404, 408, 409, 413, 415 | application/problem+json          |
| errors.APIError                   | 429                               | application/problem+json          |
| errors.APIError                   | 500                               | application/problem+json          |
| errors.APIError                   | 503                               | application/problem+json          |
| errors.ContinuousDefaultError     | 4XX, 5XX                          | \*/\*                             |

## delete

Deletes a Web Box Snapshot. A build that is still pending or building is canceled first. A Snapshot that Web Boxes started from returns 409 webbox_snapshot_in_use; delete those Web Boxes first. While a build that names it as parent_id is pending or building, it returns 409 webbox_snapshot_parent_in_use; retry after the build finishes. Catalog Snapshots cannot be deleted.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="delete-webbox-snapshot" method="delete" path="/v1/webbox-snapshots/{id}" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  await continuous.webboxSnapshots.delete({
    id: "<id>",
  });


}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { ContinuousCore } from "@continuous-labs/sdk/core.js";
import { webboxSnapshotsDelete } from "@continuous-labs/sdk/funcs/webbox-snapshots-delete.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await webboxSnapshotsDelete(continuous, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    
  } else {
    console.log("webboxSnapshotsDelete failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.DeleteWebboxSnapshotRequest](../../models/operations/delete-webbox-snapshot-request.md)                                                                            | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
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

Returns a Web Box Snapshot of the workspace or the catalog, and its build status.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get-webbox-snapshot" method="get" path="/v1/webbox-snapshots/{id}" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.webboxSnapshots.get({
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
import { webboxSnapshotsGet } from "@continuous-labs/sdk/funcs/webbox-snapshots-get.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await webboxSnapshotsGet(continuous, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("webboxSnapshotsGet failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetWebboxSnapshotRequest](../../models/operations/get-webbox-snapshot-request.md)                                                                                  | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.WebBoxSnapshot](../../models/web-box-snapshot.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.APIError               | 401, 404                      | application/problem+json      |
| errors.APIError               | 500, 503                      | application/problem+json      |
| errors.ContinuousDefaultError | 4XX, 5XX                      | \*/\*                         |

## update

Renames a Web Box Snapshot or replaces its metadata. Omitted fields keep their current values. The built app does not change. Catalog Snapshots cannot be updated.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="update-webbox-snapshot" method="patch" path="/v1/webbox-snapshots/{id}" example="bad_request_body" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.webboxSnapshots.update({
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
import { webboxSnapshotsUpdate } from "@continuous-labs/sdk/funcs/webbox-snapshots-update.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await webboxSnapshotsUpdate(continuous, {
    id: "<id>",
    body: {},
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("webboxSnapshotsUpdate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.UpdateWebboxSnapshotRequest](../../models/operations/update-webbox-snapshot-request.md)                                                                            | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.WebBoxSnapshot](../../models/web-box-snapshot.md)\>**

### Errors

| Error Type                             | Status Code                            | Content Type                           |
| -------------------------------------- | -------------------------------------- | -------------------------------------- |
| errors.APIError                        | 400, 401, 403, 404, 408, 413, 415, 422 | application/problem+json               |
| errors.APIError                        | 500, 503                               | application/problem+json               |
| errors.ContinuousDefaultError          | 4XX, 5XX                               | \*/\*                                  |

## cancel

Requests cancellation of a pending or active build and returns the Snapshot without waiting for the build to stop. Get the Snapshot until its status leaves pending or building. The build can finish before cancellation takes effect. A Snapshot whose build has settled is returned unchanged.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="cancel-webbox-snapshot" method="post" path="/v1/webbox-snapshots/{id}/cancel" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.webboxSnapshots.cancel({
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
import { webboxSnapshotsCancel } from "@continuous-labs/sdk/funcs/webbox-snapshots-cancel.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await webboxSnapshotsCancel(continuous, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("webboxSnapshotsCancel failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CancelWebboxSnapshotRequest](../../models/operations/cancel-webbox-snapshot-request.md)                                                                            | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.WebBoxSnapshot](../../models/web-box-snapshot.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.APIError               | 401, 403, 404                 | application/problem+json      |
| errors.APIError               | 500, 503                      | application/problem+json      |
| errors.ContinuousDefaultError | 4XX, 5XX                      | \*/\*                         |

## clone

Creates a ready copy of a ready Web Box Snapshot in another workspace, without a build. The clone has a new ID and the source's artifact, documents and saved state; the source is unchanged. The clone records no credentials, since they belong to the source workspace, and no parent or source Snapshot. The source is the caller's workspace. An API key may clone into any other workspace of its organization.

### Example Usage: bad_request_body

<!-- UsageSnippet language="typescript" operationID="clone-webbox-snapshot" method="post" path="/v1/webbox-snapshots/{id}/clone" example="bad_request_body" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.webboxSnapshots.clone({
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
import { webboxSnapshotsClone } from "@continuous-labs/sdk/funcs/webbox-snapshots-clone.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await webboxSnapshotsClone(continuous, {
    id: "<id>",
    body: {
      targetWorkspaceId: "<id>",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("webboxSnapshotsClone failed:", res.error);
  }
}

run();
```
### Example Usage: bad_request_clone_target

<!-- UsageSnippet language="typescript" operationID="clone-webbox-snapshot" method="post" path="/v1/webbox-snapshots/{id}/clone" example="bad_request_clone_target" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.webboxSnapshots.clone({
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
import { webboxSnapshotsClone } from "@continuous-labs/sdk/funcs/webbox-snapshots-clone.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await webboxSnapshotsClone(continuous, {
    id: "<id>",
    body: {
      targetWorkspaceId: "<id>",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("webboxSnapshotsClone failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CloneWebboxSnapshotRequest](../../models/operations/clone-webbox-snapshot-request.md)                                                                              | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.WebBoxSnapshot](../../models/web-box-snapshot.md)\>**

### Errors

| Error Type                                  | Status Code                                 | Content Type                                |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| errors.APIError                             | 400, 401, 403, 404, 408, 409, 413, 415, 422 | application/problem+json                    |
| errors.APIError                             | 500, 503                                    | application/problem+json                    |
| errors.ContinuousDefaultError               | 4XX, 5XX                                    | \*/\*                                       |

## resume

Resumes a build that waits, as build.waiting reports: at QA because its live credentials were rejected or the live systems rate limited its calls, or for more time after it used its time limit. For a credential wait, refresh each credential it names with PATCH /v1/credentials/{id} first: QA then runs again with their current values, and the build goes on to finalize. For a rate-limit wait, resume once the rate limit resets: QA then runs again. For a wait for more time, send add_seconds: the build continues where it stopped, with that much time from the resume. Returns the Snapshot, still building. A wait does not count toward the build's time limit: a build resumed from a QA wait has the time it had left when it began waiting. A build that is not waiting returns 409 webbox_snapshot_not_waiting.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="resume-webbox-snapshot" method="post" path="/v1/webbox-snapshots/{id}/resume" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.webboxSnapshots.resume({
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
import { webboxSnapshotsResume } from "@continuous-labs/sdk/funcs/webbox-snapshots-resume.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await webboxSnapshotsResume(continuous, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("webboxSnapshotsResume failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ResumeWebboxSnapshotRequest](../../models/operations/resume-webbox-snapshot-request.md)                                                                            | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.WebBoxSnapshot](../../models/web-box-snapshot.md)\>**

### Errors

| Error Type                             | Status Code                            | Content Type                           |
| -------------------------------------- | -------------------------------------- | -------------------------------------- |
| errors.APIError                        | 400, 401, 403, 404, 408, 409, 413, 415 | application/problem+json               |
| errors.APIError                        | 500, 503                               | application/problem+json               |
| errors.ContinuousDefaultError          | 4XX, 5XX                               | \*/\*                                  |