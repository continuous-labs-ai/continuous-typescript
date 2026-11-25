# Type

live_credentials while the build waits for the credentials it names to be refreshed; live_rate_limit while it waits for the live system's rate limit to reset; unavailable while it waits for a live system it could not reach; time_limit while it waits for a resume that adds time with add_seconds.

## Example Usage

```typescript
import { Type } from "@continuous-labs/sdk/models";

let value: Type = "live_credentials";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"live_credentials" | "live_rate_limit" | "unavailable" | "time_limit" | Unrecognized<string>
```