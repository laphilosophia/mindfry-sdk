# MindFry SDK

> **Official client libraries for MindFry** — the world's first conscious database

[![License: Apache-2.0](https://img.shields.io/badge/License-Apache--2.0-blue.svg)](LICENSE)

Connect to MindFry and manage memories that **decay**, **bond**, and **feel**.

---

> ⚠️ **EXPERIMENTAL:** MindFry simulates biological memory processes. Data may be inhibited based on the system's "mood". **Do not use for banking.**

---

## SDKs

| Language       | Status     | Package                                                                                                   |
| :------------- | :--------- | :-------------------------------------------------------------------------------------------------------- |
| **TypeScript** | ✅ Stable  | [![npm](https://img.shields.io/npm/v/@mindfry/client.svg)](https://www.npmjs.com/package/@mindfry/client) |
| **Go**         | 🚧 Planned | —                                                                                                         |
| **Python**     | 🚧 Planned | —                                                                                                         |
| **Rust**       | 🚧 Planned | Native bindings                                                                                           |

## TypeScript

```bash
npm install @mindfry/client
```

```typescript
import { MindFry } from '@mindfry/client'

const brain = new MindFry({ host: 'localhost', port: 9527 })
await brain.connect()

await brain.lineage.create({ key: 'fire', energy: 0.9 })
await brain.lineage.stimulate({ key: 'fire', delta: 0.5 })

await brain.disconnect()
```

📚 **Docs:** [mindfry-docs.vercel.app/sdk/typescript](https://mindfry-docs.vercel.app/sdk/typescript/)

### Packages

| Package                                                                | Description           |
| :--------------------------------------------------------------------- | :-------------------- |
| [`@mindfry/client`](https://www.npmjs.com/package/@mindfry/client)     | High-level client API |
| [`@mindfry/protocol`](https://www.npmjs.com/package/@mindfry/protocol) | Low-level MFBP codec  |

## Features

All SDKs implement the same core API:

- 🧠 **Lineage** — Create, stimulate, query ephemeral memories
- 🔗 **Bond** — Connect memories with weighted relationships
- 🔍 **Query** — Pattern matching, top-K, trauma detection
- ⚡ **Pipelining** — High-throughput TCP batching
- 🎭 **Mood-aware** — Behavior adapts to Cortex state

## Requirements

- MindFry Engine v1.6.0+
- Language-specific requirements in each SDK folder

## Related

- [MindFry Core](https://github.com/laphilosophia/mindfry) — Rust engine
- [Documentation](https://mindfry-docs.vercel.app) — Full docs
- [crates.io](https://crates.io/crates/mindfry) — Rust package

## Contributing

Want to add a new language SDK? See the TypeScript implementation in `packages/` as reference. All SDKs should implement the MFBP protocol and provide the same core API surface.

## License

Apache-2.0 © [Erdem Arslan](https://github.com/laphilosophia)
