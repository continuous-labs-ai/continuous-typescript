# SimulatorMode

api for a Simulator of the vendor's API; web_app for one of its logged-in web app.

## Example Usage

```typescript
import { SimulatorMode } from "@continuous-labs/sdk/models";

let value: SimulatorMode = "api";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"api" | "web_app" | Unrecognized<string>
```