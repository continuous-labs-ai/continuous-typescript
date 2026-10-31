# WebBoxSnapshotStatus

pending while waiting for capacity; building while the build runs; ready when Web Boxes can start from it; failed when the build failed; canceled when a cancel request took effect.

## Example Usage

```typescript
import { WebBoxSnapshotStatus } from "@continuous-labs/sdk/models";

let value: WebBoxSnapshotStatus = "canceled";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"pending" | "building" | "ready" | "failed" | "canceled" | Unrecognized<string>
```