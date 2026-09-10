# Simulators

## Overview

Build Simulators from OpenAPI or WSDL documents, check or cancel a build, and delete Simulators.

### Available Operations

* [listSimulators](#listsimulators) - List Simulators
* [buildSimulator](#buildsimulator) - Build Simulator
* [deleteSimulator](#deletesimulator) - Delete Simulator
* [getSimulator](#getsimulator) - Get Simulator
* [cancelSimulatorBuild](#cancelsimulatorbuild) - Cancel Simulator Build

## listSimulators

Returns all Simulators that the API key can access. Results can be filtered by status or name.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="list-simulators" method="get" path="/v1/simulators" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.simulators.listSimulators({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { ContinuousCore } from "@continuous-labs/sdk/core.js";
import { simulatorsListSimulators } from "@continuous-labs/sdk/funcs/simulators-list-simulators.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await simulatorsListSimulators(continuous, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("simulatorsListSimulators failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListSimulatorsRequest](../../models/operations/list-simulators-request.md)                                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.ListSimulatorsResponse](../../models/list-simulators-response.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ErrorT                 | 400, 401, 403, 404, 422       | application/problem+json      |
| errors.ErrorT                 | 500, 503                      | application/problem+json      |
| errors.ContinuousDefaultError | 4XX, 5XX                      | \*/\*                         |

## buildSimulator

Starts an asynchronous Simulator build and returns the Simulator with status building. Send multipart/form-data with a JSON part named request. To build from a document, add a file part named spec with the OpenAPI or WSDL document. For an incremental build, omit spec and set parent_id and instructions.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="build-simulator" method="post" path="/v1/simulators" example="simulator_unknown_parent" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.simulators.buildSimulator({
    request: {
      filter: [],
      instructions: "Return stable example data for every operation.",
      name: "billing-api",
      specKind: "openapi",
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
import { simulatorsBuildSimulator } from "@continuous-labs/sdk/funcs/simulators-build-simulator.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await simulatorsBuildSimulator(continuous, {
    request: {
      filter: [],
      instructions: "Return stable example data for every operation.",
      name: "billing-api",
      specKind: "openapi",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("simulatorsBuildSimulator failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.BuildSimulatorRequest](../../models/operations/build-simulator-request.md)                                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.Simulator](../../models/simulator.md)\>**

### Errors

| Error Type                                       | Status Code                                      | Content Type                                     |
| ------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ |
| errors.ErrorT                                    | 400, 401, 403, 404, 408, 409, 413, 415, 422, 429 | application/problem+json                         |
| errors.ErrorT                                    | 500, 503                                         | application/problem+json                         |
| errors.ContinuousDefaultError                    | 4XX, 5XX                                         | \*/\*                                            |

## deleteSimulator

Deletes a Simulator that has no dependent Worlds, Simulations, or child Simulators.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="delete-simulator" method="delete" path="/v1/simulators/{id}" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  await continuous.simulators.deleteSimulator({
    id: "<id>",
  });


}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { ContinuousCore } from "@continuous-labs/sdk/core.js";
import { simulatorsDeleteSimulator } from "@continuous-labs/sdk/funcs/simulators-delete-simulator.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await simulatorsDeleteSimulator(continuous, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    
  } else {
    console.log("simulatorsDeleteSimulator failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.DeleteSimulatorRequest](../../models/operations/delete-simulator-request.md)                                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<void\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ErrorT                 | 400, 401, 403, 404, 409, 422  | application/problem+json      |
| errors.ErrorT                 | 500, 503                      | application/problem+json      |
| errors.ContinuousDefaultError | 4XX, 5XX                      | \*/\*                         |

## getSimulator

Returns a Simulator and its current build status.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get-simulator" method="get" path="/v1/simulators/{id}" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.simulators.getSimulator({
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
import { simulatorsGetSimulator } from "@continuous-labs/sdk/funcs/simulators-get-simulator.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await simulatorsGetSimulator(continuous, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("simulatorsGetSimulator failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetSimulatorRequest](../../models/operations/get-simulator-request.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.Simulator](../../models/simulator.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ErrorT                 | 400, 401, 403, 404, 422       | application/problem+json      |
| errors.ErrorT                 | 500, 503                      | application/problem+json      |
| errors.ContinuousDefaultError | 4XX, 5XX                      | \*/\*                         |

## cancelSimulatorBuild

Requests cancellation of an active Simulator build. The build can finish before cancellation takes effect.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="cancel-simulator-build" method="post" path="/v1/simulators/{id}/cancel" -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.simulators.cancelSimulatorBuild({
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
import { simulatorsCancelSimulatorBuild } from "@continuous-labs/sdk/funcs/simulators-cancel-simulator-build.js";

// Use `ContinuousCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const continuous = new ContinuousCore({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const res = await simulatorsCancelSimulatorBuild(continuous, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("simulatorsCancelSimulatorBuild failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CancelSimulatorBuildRequest](../../models/operations/cancel-simulator-build-request.md)                                                                            | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.Simulator](../../models/simulator.md)\>**

### Errors

| Error Type                    | Status Code                   | Content Type                  |
| ----------------------------- | ----------------------------- | ----------------------------- |
| errors.ErrorT                 | 400, 401, 403, 404, 409, 422  | application/problem+json      |
| errors.ErrorT                 | 500, 503                      | application/problem+json      |
| errors.ContinuousDefaultError | 4XX, 5XX                      | \*/\*                         |