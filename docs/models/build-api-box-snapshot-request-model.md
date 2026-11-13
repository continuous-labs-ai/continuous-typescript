# BuildAPIBoxSnapshotRequestModel

Model that builds and reviews the Snapshot. Omission means combined without parent_id and the parent's model with it. Its provider is derived from the model. combined currently builds, reviews, and runs QA exactly as claude-opus-5-5 does.

## Example Usage

```typescript
import { BuildAPIBoxSnapshotRequestModel } from "@continuous-labs/sdk/models";

let value: BuildAPIBoxSnapshotRequestModel = "claude-fable-5-2";
```

## Values

```typescript
"gpt-6-astra" | "gpt-6.1-sol" | "claude-opus-5-5" | "claude-fable-5-2" | "combined"
```