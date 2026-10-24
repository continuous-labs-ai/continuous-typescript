# ListSimulationsStatus

Optional status filter. paused is deprecated and matches the same Simulations as running.

## Example Usage

```typescript
import { ListSimulationsStatus } from "@continuous-labs/sdk/models/operations";

let value: ListSimulationsStatus = "paused";
```

## Values

```typescript
"running" | "paused" | "stopped"
```