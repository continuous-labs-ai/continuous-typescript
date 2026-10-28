# SimulatorResearchStatus

pending until the stage starts; running while the research agent indexes the documents and saves the vendor pages they lack; complete when it wrote an index that names every document; failed when it could not finish, which fails the build, or when the build ended first; provided when research did not run because the build already had an index.

## Example Usage

```typescript
import { SimulatorResearchStatus } from "@continuous-labs/sdk/models";

let value: SimulatorResearchStatus = "complete";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"pending" | "running" | "complete" | "failed" | "provided" | Unrecognized<string>
```