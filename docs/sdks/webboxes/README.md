# Webboxes

## Overview

Start Web Boxes from Web Box Snapshots. Each Web Box serves its Snapshot's web app at a host of its own, with its own state, in real time. Stop, start and delete them.

### Available Operations

* [list](#list) - List Web Boxes
* [create](#create) - Create Web Box
* [delete](#delete) - Delete Web Box
* [get](#get) - Get Web Box
* [update](#update) - Update Web Box
* [saveSnapshot](#savesnapshot) - Save Web Box as Snapshot
* [start](#start) - Start Web Box
* [listSteps](#liststeps) - List Web Box steps
* [stop](#stop) - Stop Web Box

## list

Returns the workspace's Web Boxes, newest first. Results can be filtered by status and Snapshot.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="list-webboxes" method="get" path="/v1/webbox" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.webboxes.list({});

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
import { webboxesList } from "@continuous-labs/sdk/funcs/webboxes-list.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await webboxesList(continuous, {});
  if (res.ok) {
    const { value: result } = res;
    for await (const page of result) {
    console.log(page);
  }
  } else {
    console.log("webboxesList failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListWebboxesRequest](../../models/operations/list-webboxes-request.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ListWebboxesResponse](../../models/operations/list-webboxes-response.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.APIError               | 400, 401, 422                 | application/problem+json      |
| errors.APIError               | 500, 503                      | application/problem+json      |
| errors.ContinuousDefaultError | 4XX, 5XX                      | \*/\*                         |

## create

Creates a Web Box from a ready Web Box Snapshot and starts it. It returns at once with status starting; get the Web Box until it is running. Open its url in a browser: the app is served at a host of its own, open to anyone with the URL. Each Web Box has its own state, and runs in real time.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="create-webbox" method="post" path="/v1/webbox" example="bad_request_body" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.webboxes.create({
    body: {
      name: "crm-sandbox",
      snapshotId: "wbs_01J8Z5X4K70000000000000005",
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
import { webboxesCreate } from "@continuous-labs/sdk/funcs/webboxes-create.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await webboxesCreate(continuous, {
    body: {
      name: "crm-sandbox",
      snapshotId: "wbs_01J8Z5X4K70000000000000005",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("webboxesCreate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CreateWebboxRequest](../../models/operations/create-webbox-request.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.CreateWebBoxResponse](../../models/create-web-box-response.md)\>**

### Errors

| Error Type                                  | Status Code                                 | Content Type                                |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| errors.APIError                             | 400, 401, 404, 408, 409, 413, 415, 422, 429 | application/problem+json                    |
| errors.APIError                             | 500, 503                                    | application/problem+json                    |
| errors.ContinuousDefaultError               | 4XX, 5XX                                    | \*/\*                                       |

## delete

Deletes a Web Box, running or stopped, with its state. Its runtime is released after the response.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="delete-webbox" method="delete" path="/v1/webbox/{id}" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  await continuous.webboxes.delete({
    id: "<id>",
  });


}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { ContinuousCore } from "@continuous-labs/sdk/core.js";
import { webboxesDelete } from "@continuous-labs/sdk/funcs/webboxes-delete.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await webboxesDelete(continuous, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    
  } else {
    console.log("webboxesDelete failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.DeleteWebboxRequest](../../models/operations/delete-webbox-request.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
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

Returns a Web Box, its status and its connection: the URL that opens its app, whether it is running or stopped. The app answers only while the Web Box is running.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get-webbox" method="get" path="/v1/webbox/{id}" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.webboxes.get({
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
import { webboxesGet } from "@continuous-labs/sdk/funcs/webboxes-get.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await webboxesGet(continuous, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("webboxesGet failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetWebboxRequest](../../models/operations/get-webbox-request.md)                                                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.GetWebBoxResponse](../../models/get-web-box-response.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.APIError               | 401, 404                      | application/problem+json      |
| errors.APIError               | 500, 503                      | application/problem+json      |
| errors.ContinuousDefaultError | 4XX, 5XX                      | \*/\*                         |

## update

Renames a Web Box or replaces its metadata. Omitted fields keep their current values.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="update-webbox" method="patch" path="/v1/webbox/{id}" example="bad_request_body" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.webboxes.update({
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
import { webboxesUpdate } from "@continuous-labs/sdk/funcs/webboxes-update.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await webboxesUpdate(continuous, {
    id: "<id>",
    body: {},
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("webboxesUpdate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.UpdateWebboxRequest](../../models/operations/update-webbox-request.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.WebBox](../../models/web-box.md)\>**

### Errors

| Error Type                        | Status Code                       | Content Type                      |
| --------------------------------- | --------------------------------- | --------------------------------- |
| errors.APIError                   | 400, 401, 404, 408, 413, 415, 422 | application/problem+json          |
| errors.APIError                   | 500, 503                          | application/problem+json          |
| errors.ContinuousDefaultError     | 4XX, 5XX                          | \*/\*                             |

## saveSnapshot

Saves a running Web Box's app and current state as a Web Box Snapshot, ready when the response returns. The Web Box keeps running, and a paused one is woken. Web Boxes created from the Snapshot start with the saved state instead of a new workspace, so they refuse include_sample_data. The Snapshot outlives the Web Box. A starting Web Box returns 409 webbox_starting; a stopping or stopped one returns 409 webbox_stopped; one whose runtime cannot save its state returns 409 webbox_rebuild_required.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="save-webbox-snapshot" method="post" path="/v1/webbox/{id}/snapshot" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.webboxes.saveSnapshot({
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
import { webboxesSaveSnapshot } from "@continuous-labs/sdk/funcs/webboxes-save-snapshot.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await webboxesSaveSnapshot(continuous, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("webboxesSaveSnapshot failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.SaveWebboxSnapshotRequest](../../models/operations/save-webbox-snapshot-request.md)                                                                                | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.WebBoxSnapshot](../../models/web-box-snapshot.md)\>**

### Errors

| Error Type                             | Status Code                            | Content Type                           |
| -------------------------------------- | -------------------------------------- | -------------------------------------- |
| errors.APIError                        | 400, 401, 404, 408, 409, 413, 415, 422 | application/problem+json               |
| errors.APIError                        | 500, 503                               | application/problem+json               |
| errors.ContinuousDefaultError          | 4XX, 5XX                               | \*/\*                                  |

## start

Starts a stopped Web Box from the state its stop saved, and returns at once with status starting. A running, starting or stopping Web Box returns 409 webbox_not_stopped.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="start-webbox" method="post" path="/v1/webbox/{id}/start" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.webboxes.start({
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
import { webboxesStart } from "@continuous-labs/sdk/funcs/webboxes-start.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await webboxesStart(continuous, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("webboxesStart failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.StartWebboxRequest](../../models/operations/start-webbox-request.md)                                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.WebBox](../../models/web-box.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.APIError               | 401, 404, 409, 429            | application/problem+json      |
| errors.APIError               | 500, 503                      | application/problem+json      |
| errors.ContinuousDefaultError | 4XX, 5XX                      | \*/\*                         |

## listSteps

Lists the Web Box's steps in order. Each request that changed state is one step; a request that only reads registers none. A Web Box that is not running returns 409 webbox_stopped.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="list-webbox-steps" method="get" path="/v1/webbox/{id}/steps" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.webboxes.listSteps({
    id: "<id>",
  });

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
import { webboxesListSteps } from "@continuous-labs/sdk/funcs/webboxes-list-steps.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await webboxesListSteps(continuous, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    for await (const page of result) {
    console.log(page);
  }
  } else {
    console.log("webboxesListSteps failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListWebboxStepsRequest](../../models/operations/list-webbox-steps-request.md)                                                                                      | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ListWebboxStepsResponse](../../models/operations/list-webbox-steps-response.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.APIError               | 400, 401, 404, 409, 422       | application/problem+json      |
| errors.APIError               | 500, 503                      | application/problem+json      |
| errors.ContinuousDefaultError | 4XX, 5XX                      | \*/\*                         |

## stop

Stops a running Web Box: it saves its state, and releases its runtime. It returns at once with status stopping; get the Web Box until it is stopped. A stopped Web Box is returned unchanged; a starting one returns 409 webbox_starting.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="stop-webbox" method="post" path="/v1/webbox/{id}/stop" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.webboxes.stop({
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
import { webboxesStop } from "@continuous-labs/sdk/funcs/webboxes-stop.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await webboxesStop(continuous, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("webboxesStop failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.StopWebboxRequest](../../models/operations/stop-webbox-request.md)                                                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.WebBox](../../models/web-box.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.APIError               | 401, 404, 409                 | application/problem+json      |
| errors.APIError               | 500, 503                      | application/problem+json      |
| errors.ContinuousDefaultError | 4XX, 5XX                      | \*/\*                         |