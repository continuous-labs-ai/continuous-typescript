<!-- Start SDK Example Usage [usage] -->
```typescript
import { Continuous } from "@continuous-labs/sdk";

const continuous = new Continuous({
  apiKeyAuth: process.env["CONTINUOUS_API_KEY_AUTH"] ?? "",
});

async function run() {
  const result = await continuous.simulations.listSimulations({});

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->