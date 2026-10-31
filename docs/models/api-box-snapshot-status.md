# APIBoxSnapshotStatus

pending while waiting for capacity; building while the build runs; ready when API Boxes can start from it; failed when the build failed; canceled when a cancel request took effect.

## Example Usage

```typescript
import { APIBoxSnapshotStatus } from "@continuous-labs/sdk/models";

let value: APIBoxSnapshotStatus = "ready";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"pending" | "building" | "ready" | "failed" | "canceled" | Unrecognized<string>
```