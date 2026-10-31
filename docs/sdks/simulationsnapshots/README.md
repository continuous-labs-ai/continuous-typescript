# ~~SimulationSnapshots~~

> [!WARNING]
> This SDK is **DEPRECATED**

## Overview

Deprecated. Use API Box for APIs and Web Box for web apps. Save a running Simulation's state as a Snapshot, create Simulations from it, and rename and delete it.

### Available Operations

* [~~listSimulationSnapshots~~](#listsimulationsnapshots) - List Simulation Snapshots :warning: **Deprecated**
* [~~createSimulationSnapshot~~](#createsimulationsnapshot) - Create Simulation Snapshot :warning: **Deprecated**
* [~~deleteSimulationSnapshot~~](#deletesimulationsnapshot) - Delete Simulation Snapshot :warning: **Deprecated**
* [~~getSimulationSnapshot~~](#getsimulationsnapshot) - Get Simulation Snapshot :warning: **Deprecated**
* [~~updateSimulationSnapshot~~](#updatesimulationsnapshot) - Update Simulation Snapshot :warning: **Deprecated**

## ~~listSimulationSnapshots~~

Returns the workspace's Snapshots, newest first. Filter by simulation_id for the Snapshots of one Simulation.

Deprecated. Use API Box for APIs and Web Box for web apps.

> :warning: **DEPRECATED**: Use API Box for APIs and Web Box for web apps.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="list-simulation-snapshots" method="get" path="/v1/simulation-snapshots" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.simulationSnapshots.listSimulationSnapshots({});

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
import { simulationSnapshotsListSimulationSnapshots } from "@continuous-labs/sdk/funcs/simulation-snapshots-list-simulation-snapshots.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await simulationSnapshotsListSimulationSnapshots(continuous, {});
  if (res.ok) {
    const { value: result } = res;
    for await (const page of result) {
    console.log(page);
  }
  } else {
    console.log("simulationSnapshotsListSimulationSnapshots failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListSimulationSnapshotsRequest](../../models/operations/list-simulation-snapshots-request.md)                                                                      | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ListSimulationSnapshotsResponse](../../models/operations/list-simulation-snapshots-response.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ErrorT                 | 400, 401, 422                 | application/problem+json      |
| errors.ErrorT                 | 500, 503                      | application/problem+json      |
| errors.ContinuousDefaultError | 4XX, 5XX                      | \*/\*                         |

## ~~createSimulationSnapshot~~

Starts saving a running Simulation's current state and returns the Snapshot with status creating. Poll it until it is ready, or failed with an error. Saving closes the Simulation's open event streams and WebSockets and does not change its state; while it saves, an advance returns 409 clock_conflict, and a stop waits for it. Create Simulations from a ready Snapshot with snapshot_id; it outlives its Simulation. A stopped Simulation returns 409 simulation_stopped. Reuse the Idempotency-Key to retry safely.

Deprecated. Use API Box for APIs and Web Box for web apps.

> :warning: **DEPRECATED**: Use API Box for APIs and Web Box for web apps.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="create-simulation-snapshot" method="post" path="/v1/simulation-snapshots" example="bad_request_body" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.simulationSnapshots.createSimulationSnapshot({
    idempotencyKey: "<value>",
    body: {
      name: "before-refund",
      simulationId: "sim_01J8Z5X4K7M2N9P0Q1R2S3T4V6",
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
import { simulationSnapshotsCreateSimulationSnapshot } from "@continuous-labs/sdk/funcs/simulation-snapshots-create-simulation-snapshot.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await simulationSnapshotsCreateSimulationSnapshot(continuous, {
    idempotencyKey: "<value>",
    body: {
      name: "before-refund",
      simulationId: "sim_01J8Z5X4K7M2N9P0Q1R2S3T4V6",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("simulationSnapshotsCreateSimulationSnapshot failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CreateSimulationSnapshotRequest](../../models/operations/create-simulation-snapshot-request.md)                                                                    | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.SimulationSnapshot](../../models/simulation-snapshot.md)\>**

### Errors

| Error Type                                  | Status Code                                 | Content Type                                |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| errors.ErrorT                               | 400, 401, 403, 404, 408, 409, 413, 415, 422 | application/problem+json                    |
| errors.ErrorT                               | 500, 503                                    | application/problem+json                    |
| errors.ContinuousDefaultError               | 4XX, 5XX                                    | \*/\*                                       |

## ~~deleteSimulationSnapshot~~

Deletes a Snapshot and its saved state. Simulations created from it keep running, and their snapshot_id becomes null. While it is creating, the response is 409 snapshot_not_ready; while a Simulation is starting from it, 409 snapshot_in_use.

Deprecated. Use API Box for APIs and Web Box for web apps.

> :warning: **DEPRECATED**: Use API Box for APIs and Web Box for web apps.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="delete-simulation-snapshot" method="delete" path="/v1/simulation-snapshots/{id}" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  await continuous.simulationSnapshots.deleteSimulationSnapshot({
    id: "<id>",
  });


}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { ContinuousCore } from "@continuous-labs/sdk/core.js";
import { simulationSnapshotsDeleteSimulationSnapshot } from "@continuous-labs/sdk/funcs/simulation-snapshots-delete-simulation-snapshot.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await simulationSnapshotsDeleteSimulationSnapshot(continuous, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    
  } else {
    console.log("simulationSnapshotsDeleteSimulationSnapshot failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.DeleteSimulationSnapshotRequest](../../models/operations/delete-simulation-snapshot-request.md)                                                                    | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<void\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ErrorT                 | 401, 404, 409                 | application/problem+json      |
| errors.ErrorT                 | 500, 503                      | application/problem+json      |
| errors.ContinuousDefaultError | 4XX, 5XX                      | \*/\*                         |

## ~~getSimulationSnapshot~~

Returns a Snapshot.

Deprecated. Use API Box for APIs and Web Box for web apps.

> :warning: **DEPRECATED**: Use API Box for APIs and Web Box for web apps.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get-simulation-snapshot" method="get" path="/v1/simulation-snapshots/{id}" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.simulationSnapshots.getSimulationSnapshot({
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
import { simulationSnapshotsGetSimulationSnapshot } from "@continuous-labs/sdk/funcs/simulation-snapshots-get-simulation-snapshot.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await simulationSnapshotsGetSimulationSnapshot(continuous, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("simulationSnapshotsGetSimulationSnapshot failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetSimulationSnapshotRequest](../../models/operations/get-simulation-snapshot-request.md)                                                                          | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.SimulationSnapshot](../../models/simulation-snapshot.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ErrorT                 | 401, 404                      | application/problem+json      |
| errors.ErrorT                 | 500, 503                      | application/problem+json      |
| errors.ContinuousDefaultError | 4XX, 5XX                      | \*/\*                         |

## ~~updateSimulationSnapshot~~

Renames a Snapshot. Omitted fields keep their current values.

Deprecated. Use API Box for APIs and Web Box for web apps.

> :warning: **DEPRECATED**: Use API Box for APIs and Web Box for web apps.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="update-simulation-snapshot" method="patch" path="/v1/simulation-snapshots/{id}" example="bad_request_body" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.simulationSnapshots.updateSimulationSnapshot({
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
import { simulationSnapshotsUpdateSimulationSnapshot } from "@continuous-labs/sdk/funcs/simulation-snapshots-update-simulation-snapshot.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await simulationSnapshotsUpdateSimulationSnapshot(continuous, {
    id: "<id>",
    body: {},
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("simulationSnapshotsUpdateSimulationSnapshot failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.UpdateSimulationSnapshotRequest](../../models/operations/update-simulation-snapshot-request.md)                                                                    | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.SimulationSnapshot](../../models/simulation-snapshot.md)\>**

### Errors

| Error Type                        | Status Code                       | Content Type                      |
| --------------------------------- | --------------------------------- | --------------------------------- |
| errors.ErrorT                     | 400, 401, 404, 408, 413, 415, 422 | application/problem+json          |
| errors.ErrorT                     | 500, 503                          | application/problem+json          |
| errors.ContinuousDefaultError     | 4XX, 5XX                          | \*/\*                             |