# Type

live_credentials while QA waits for the credentials it names to be refreshed; live_rate_limit while QA waits for the live systems' rate limit to reset; time_limit while the build waits for a resume that adds time with add_seconds.

## Example Usage

```typescript
import { Type } from "@continuous-labs/sdk/models";

let value: Type = "live_credentials";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"live_credentials" | "live_rate_limit" | "time_limit" | Unrecognized<string>
```