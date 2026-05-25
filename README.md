# Covalent (covalent)
Covalent is the blockchain data infrastructure company behind GoldRush — a unified multi-chain data platform serving 70,000+ developers across 100+ chains (Ethereum, Base, BNB Smart Chain, Polygon, Optimism, Arbitrum, Solana, Bitcoin, HyperCore/HyperEVM, and many more). The product suite covers historical REST data via the Foundational API, real-time GraphQL-over-WebSocket Streaming API, managed ETL via the Pipeline API, Hyperliquid Info and WebSocket APIs (with GoldRush-exclusive l2BookDiff and l4Book channels), and pay-per-request x402 endpoints for AI agents. Covalent also publishes language SDKs, the GoldRush CLI with native MCP support, agent skills, and a curated spam list dataset.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/covalent/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - Blockchain, Web3, Multi-Chain, Data Infrastructure, Crypto, DeFi, NFT, Hyperliquid, GoldRush, AI Agents

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Pricing

| Plan | Price | Monthly credits | RPS | Audience |
|---|---|---|---|---|
| Free Trial | $0 | 25,000 | 4 | Testing and prototyping |
| Vibe Coding | $10/mo | 10,000 (+Flex $0.00077/credit) | 4 | AI agents, copilots, indie devs |
| Professional | $250/mo | 300,000 (+Flex $0.00077/credit) | 50 | Production applications |
| Inner Circle (Enterprise) | Custom | Custom | Custom | SLAs, NDAs, dedicated support |

## APIs

### GoldRush Foundational API
Structured historical blockchain data across 100+ chains via REST. Resource families: Balances (native, ERC20, ERC721, ERC1155, historical portfolios, token holders), Transactions (v3 paginated, time-bucketed, by-block, by-hash), NFTs (ownership, holdings), Base service (blocks, logs, gas prices, address resolution, chain status), Cross-Chain Activity, Pricing (historical token prices, pool spot prices), Security (token approvals), and Bitcoin (HD and non-HD).

**Base URL:** `https://api.covalenthq.com`

**Human URL:** [https://goldrush.dev/docs/api-reference/foundational-api/](https://goldrush.dev/docs/api-reference/foundational-api/)

- [OpenAPI](openapi/covalent-foundational-api-openapi.yml)
- [JSON Schema — Balance](json-schema/covalent-balance-schema.json)
- [JSON Schema — Transaction](json-schema/covalent-transaction-schema.json)
- [JSON-LD](json-ld/covalent-context.jsonld)
- [Naftiko Capability — Balances](capabilities/foundational-balances.yaml)
- [Naftiko Capability — Transactions](capabilities/foundational-transactions.yaml)
- [Naftiko Capability — NFTs](capabilities/foundational-nft.yaml)
- [Naftiko Capability — Base Service](capabilities/foundational-base.yaml)
- [Naftiko Capability — Cross-Chain](capabilities/foundational-cross-chain.yaml)
- [Naftiko Capability — Pricing](capabilities/foundational-pricing.yaml)
- [Naftiko Capability — Security](capabilities/foundational-security.yaml)

### GoldRush Streaming API
GraphQL-over-WebSocket interface for sub-second blockchain events. One-shot queries: `ohlcvPairs`, `ohlcvTokens`, `tokenSearch`, `topTraderWalletsForToken`, `walletPnlByToken`. Subscriptions: `newDexPairs`, `ohlcvPairs`, `ohlcvTokens`, `updatePairs`, `updateTokens`, `walletActivity`.

**Base URL:** `https://streaming.goldrush.dev` / `wss://streaming.goldrush.dev`

**Human URL:** [https://goldrush.dev/docs/api-reference/streaming-api/](https://goldrush.dev/docs/api-reference/streaming-api/)

- [OpenAPI](openapi/covalent-streaming-api-openapi.yml)
- [Naftiko Capability — OHLCV Queries](capabilities/streaming-ohlcv.yaml)
- [Naftiko Capability — DEX Pairs and Updates](capabilities/streaming-pairs.yaml)
- [Naftiko Capability — Wallet Activity](capabilities/streaming-wallet-activity.yaml)

### GoldRush Pipeline API
Managed ETL that streams decoded blockchain data across 20+ chains into customer destinations — ClickHouse, Kafka, S3/GCS/R2, Postgres, AWS SQS, Webhook. Pipelines configure source chains, ABI decoding (events + functions), SQL transforms, and destination connections. Service Keys are the credential type for programmatic management.

**Base URL:** `https://pipeline.goldrush.dev`

**Human URL:** [https://goldrush.dev/docs/api-reference/pipeline-api/](https://goldrush.dev/docs/api-reference/pipeline-api/)

- [OpenAPI](openapi/covalent-pipeline-api-openapi.yml)
- [Naftiko Capability — Jobs](capabilities/pipeline-jobs.yaml)
- [Naftiko Capability — Destinations, ABIs, Transforms](capabilities/pipeline-destinations.yaml)

### GoldRush Hyperliquid Info API
Drop-in replacement for the public Hyperliquid `/info` endpoint hosted at `hypercore.goldrushdata.com`. Single POST endpoint dispatching by `type` — 18 supported types covering clearinghouse state, asset contexts, frontend orders, user fills, funding, ledger updates, TWAP slice fills, sub-accounts, delegator history/rewards/summary, and HIP-4 outcome meta.

**Base URL:** `https://hypercore.goldrushdata.com`

**Human URL:** [https://goldrush.dev/docs/api-reference/hyperliquid/info-api/](https://goldrush.dev/docs/api-reference/hyperliquid/info-api/)

- [OpenAPI](openapi/covalent-hyperliquid-info-api-openapi.yml)
- [Naftiko Capability — Markets](capabilities/hyperliquid-markets.yaml)
- [Naftiko Capability — Users](capabilities/hyperliquid-users.yaml)

### GoldRush Hyperliquid WebSocket API
WebSocket channels for Hyperliquid markets including `l2Book` (wire-equal to public feed), `l2BookDiff` (GoldRush-exclusive differential updates), and `l4Book` (order-level GoldRush-exclusive), plus wallet firehose, liquidations and vault events, HIP-3 markets, and HIP-4 outcome streams.

**Base URL:** `wss://hypercore.goldrushdata.com/ws`

**Human URL:** [https://goldrush.dev/docs/api-reference/hyperliquid/websocket-api/](https://goldrush.dev/docs/api-reference/hyperliquid/websocket-api/)

- [Naftiko Capability — Order Book](capabilities/hyperliquid-orderbook.yaml)

### GoldRush x402 API
Pay-per-request HTTP 402 endpoints designed for autonomous AI agents and onchain micropayments. Lists and searches available x402 endpoints, exposes balance and recent-transaction lookups via the 402 settlement flow, and returns per-endpoint metadata for agents to discover and pay for data without a long-lived API key.

**Base URL:** `https://api.covalenthq.com`

**Human URL:** [https://goldrush.dev/docs/api-reference/foundational-api/x402](https://goldrush.dev/docs/api-reference/foundational-api/x402)

- [OpenAPI](openapi/covalent-x402-api-openapi.yml)
- [Naftiko Capability — x402 Endpoints](capabilities/x402-endpoints.yaml)

## SDKs, Tools, and Agents

- **JavaScript / TypeScript Client SDK** — [`@covalenthq/client-sdk`](https://www.npmjs.com/package/@covalenthq/client-sdk)
- **Go SDK** — [`github.com/covalenthq/covalent-api-sdk-go`](https://github.com/covalenthq/covalent-api-sdk-go) (BalanceService, TransactionService, NFTService, BaseService, SecurityService, PricingService, XykService)
- **GoldRush CLI** — [`@covalenthq/goldrush-cli`](https://www.npmjs.com/package/@covalenthq/goldrush-cli) — 17 commands, real-time streaming, native MCP support; `npx @covalenthq/goldrush-cli`
- **GoldRush Agent Skills** — [github.com/covalenthq/goldrush-agent-skills](https://github.com/covalenthq/goldrush-agent-skills)
- **GoldRush MCP Server** — [github.com/covalenthq/goldrush-mcp-server](https://github.com/covalenthq/goldrush-mcp-server) (archived; superseded by CLI native MCP)
- **GoldRush Kit** — React components (archived) — [github.com/covalenthq/goldrush-kit](https://github.com/covalenthq/goldrush-kit)
- **AI Agent SDK** — Zero-Employee Enterprise (archived) — [github.com/covalenthq/ai-agent-sdk](https://github.com/covalenthq/ai-agent-sdk)
- **Enhanced Spam Lists** — ERC20 + NFT — [github.com/covalenthq/goldrush-enhanced-spam-lists](https://github.com/covalenthq/goldrush-enhanced-spam-lists)
- **Block Specimen Producers** — [refiner](https://github.com/covalenthq/refiner), [bsp-agent](https://github.com/covalenthq/bsp-agent), [bsp-geth](https://github.com/covalenthq/bsp-geth), [bsp-prysm](https://github.com/covalenthq/bsp-prysm) — Covalent Network data infrastructure

## Authentication

All HTTP APIs use Bearer-token auth: `Authorization: Bearer cqt_xxxxxxxxxxxxxxxxxxxx`. Keys are minted in the [GoldRush Platform dashboard](https://goldrush.dev/platform/). The Pipeline API uses a separate **Service Key** credential type for programmatic management.

## Supported Chains (selected)

- **Foundational support:** Base, BNB Smart Chain, Ethereum, Gnosis, Optimism, Polygon
- **Frontier support:** Arbitrum, Avalanche C-Chain, Berachain, Bitcoin, HyperCore, HyperEVM, Linea, Mantle, MegaETH, Monad, Plasma, Scroll, Sei, Solana, Sonic, Taiko, Unichain, World Chain, zkSync Era, and more
- **Community support:** Blast, Canto, Celo, Cronos zkEVM, Fantom, Manta Pacific Testnet, Moonbeam, Moonriver, opBNB, ZetaChain, and more

Full list: [https://goldrush.dev/chains/](https://goldrush.dev/chains/)

## Compliance

- **SOC 2** compliant — enterprise security controls audited

## Links

- **Homepage:** [covalenthq.com](https://www.covalenthq.com) / [goldrush.dev](https://goldrush.dev)
- **Docs:** [goldrush.dev/docs](https://goldrush.dev/docs/)
- **Changelog:** [goldrush.dev/docs/changelog](https://goldrush.dev/docs/changelog)
- **Blog:** [goldrush.dev/blog](https://goldrush.dev/blog/)
- **Status:** [status.goldrush.dev](https://status.goldrush.dev)
- **Pricing:** [goldrush.dev/pricing](https://goldrush.dev/pricing/)
- **Support:** [goldrush.dev/support](https://goldrush.dev/support/)
- **GitHub:** [github.com/covalenthq](https://github.com/covalenthq)
- **LinkedIn:** [linkedin.com/company/covalent-hq](https://www.linkedin.com/company/covalent-hq)
- **X / Twitter:** [@Covalent_HQ](https://twitter.com/Covalent_HQ)
