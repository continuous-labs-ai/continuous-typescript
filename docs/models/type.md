# Type

live_credentials while QA waits for the credentials it names to be refreshed; time_limit while the build waits for a resume that adds time with add_seconds.

## Example Usage

```typescript
import { Type } from "@continuous-labs/sdk/models";

let value: Type = "live_credentials";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"live_credentials" | "time_limit" | Unrecognized<string>
```