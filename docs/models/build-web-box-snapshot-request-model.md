# BuildWebBoxSnapshotRequestModel

Model that builds and reviews the Snapshot. Defaults to combined. Its provider is derived from the model. combined currently builds, reviews, and runs QA exactly as claude-opus-5-5 does.

## Example Usage

```typescript
import { BuildWebBoxSnapshotRequestModel } from "@continuous-labs/sdk/models";

let value: BuildWebBoxSnapshotRequestModel = "gpt-6-astra";
```

## Values

```typescript
"gpt-6-astra" | "gpt-6.1-sol" | "claude-opus-5-5" | "claude-fable-5-2" | "combined"
```