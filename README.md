# Covalent (covalent)

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/covalent/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/covalent/refs/heads/main/apis.yml)

## Scope

- **Access:** 3rd-Party

## Tags

- Blockchain
- Web3
- Multi-Chain
- Data Infrastructure
- Crypto
- DeFi
- NFT
- Hyperliquid
- GoldRush
- AI Agents

## APIs

### GoldRush Foundational API

REST API providing structured historical blockchain data across 100+ chains. Resource families include Balances (native, ERC20, ERC721, ERC1155, historical portfolios, token holders), Transactions (v3 paginated, time-bucketed, by-block), NFTs (ownership, holdings, metadata), Base service (blocks, logs, gas prices, address resolution), Cross-Chain Activity (locate active chains for an address in one call), Pricing (historical token prices, pool spot prices), and Security (token approvals). Bearer-token authentication, credit-metered, realtime processing.

- **Human URL:** [https://goldrush.dev/docs/api-reference/foundational-api/](https://goldrush.dev/docs/api-reference/foundational-api/)
- **Base URL:** `https://api.covalenthq.com`

#### Tags

- Blockchain
- Web3
- Balances
- Transactions
- NFT
- Multi-Chain
- Historical Data

#### Properties

- [Documentation](https://goldrush.dev/docs/api-reference/foundational-api/)
- [Documentation](https://goldrush.dev/docs/api-reference/foundational-api/balance-service)
- [Documentation](https://goldrush.dev/docs/api-reference/foundational-api/transactions-service)
- [Documentation](https://goldrush.dev/docs/api-reference/foundational-api/nft-service)
- [Documentation](https://goldrush.dev/docs/api-reference/foundational-api/base-service)
- [Documentation](https://goldrush.dev/docs/api-reference/foundational-api/cross-chain-activity)
- [Documentation](https://goldrush.dev/docs/api-reference/foundational-api/security-service)
- [Documentation](https://goldrush.dev/docs/api-reference/foundational-api/pricing-service)
- [OpenAPI](openapi/covalent-foundational-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/covalent-foundational-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/covalent-foundational-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/covalent-balance-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/covalent-transaction-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/covalent-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### GoldRush Streaming API

Real-time blockchain events via GraphQL over WebSockets with sub-second latency. Includes one-shot queries (OHLCV pairs and tokens, token search, top trader wallets, wallet PnL by token) and live subscriptions (new DEX pairs stream, OHLCV pairs and tokens streams, update pairs and tokens streams, wallet activity stream). Designed for trading bots, dashboards, gaming, and AI agents that need push-based updates.

- **Human URL:** [https://goldrush.dev/docs/api-reference/streaming-api/](https://goldrush.dev/docs/api-reference/streaming-api/)
- **Base URL:** `https://streaming.goldrush.dev`

#### Tags

- Blockchain
- Streaming
- GraphQL
- WebSocket
- Real-Time
- DEX
- OHLCV

#### Properties

- [Documentation](https://goldrush.dev/docs/api-reference/streaming-api/)
- [OpenAPI](openapi/covalent-streaming-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/covalent-streaming-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/covalent-streaming-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [AsyncAPI](asyncapi/covalent-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)

### GoldRush Pipeline API

Managed data pipeline that streams decoded blockchain data into your own infrastructure across 20+ chains. Pipelines configure source chains, ABI decoding (event logs and functions), SQL transforms, and destinations including ClickHouse, Kafka, S3/GCS/R2 object storage, Postgres, AWS SQS, and Webhooks. Service Keys are the credential type for programmatic pipeline management. Use cases include data warehousing, analytics, ETL, and backend indexing.

- **Human URL:** [https://goldrush.dev/docs/api-reference/pipeline-api/](https://goldrush.dev/docs/api-reference/pipeline-api/)
- **Base URL:** `https://pipeline.goldrush.dev`

#### Tags

- Blockchain
- Data Pipeline
- ETL
- ABI Decoding
- ClickHouse
- Kafka
- Webhook
- SQL

#### Properties

- [Documentation](https://goldrush.dev/docs/api-reference/pipeline-api/)
- [Documentation](https://goldrush.dev/docs/api-reference/pipeline-api/quickstart)
- [Documentation](https://goldrush.dev/docs/api-reference/pipeline-api/architecture)
- [Documentation](https://goldrush.dev/docs/api-reference/pipeline-api/destinations)
- [Documentation](https://goldrush.dev/docs/api-reference/pipeline-api/abi-decoding)
- [OpenAPI](openapi/covalent-pipeline-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/covalent-pipeline-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/covalent-pipeline-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### GoldRush Hyperliquid Info API

Drop-in replacement for the public Hyperliquid /info API hosted at hypercore.goldrushdata.com. Supports 18 info types including clearinghouseState, batchClearinghouseState, spotClearinghouseState, spotMetaAndAssetCtxs, metaAndAssetCtxs, frontendOpenOrders, userFills / userFillsByTime, userFunding, userTwapSliceFills, userNonFundingLedgerUpdates, userVaultEquities, delegatorHistory, delegatorRewards, delegatorSummary, subAccounts, batchSpotClearinghouseState, and outcomeMeta. Adds caching, batching, and HIP-3 / HIP-4 outcome market coverage on top of the canonical Hyperliquid feed.

- **Human URL:** [https://goldrush.dev/docs/api-reference/hyperliquid/info-api/](https://goldrush.dev/docs/api-reference/hyperliquid/info-api/)
- **Base URL:** `https://hypercore.goldrushdata.com`

#### Tags

- Blockchain
- Hyperliquid
- Trading
- Perpetuals
- DEX
- Markets

#### Properties

- [Documentation](https://goldrush.dev/docs/api-reference/hyperliquid/info-api/)
- [Documentation](https://goldrush.dev/docs/api-reference/hyperliquid/info-api/migration-guide)
- [Documentation](https://goldrush.dev/docs/api-reference/hyperliquid/info-api/limits)
- [OpenAPI](openapi/covalent-hyperliquid-info-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/covalent-hyperliquid-info-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/covalent-hyperliquid-info-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### GoldRush Hyperliquid WebSocket API

WebSocket channels for Hyperliquid markets including l2Book (wire-equal to the public feed), l2BookDiff (GoldRush-exclusive differential updates), and l4Book (order-level GoldRush-exclusive channel) plus wallet firehose, liquidations and vault events, HIP-3 markets, and HIP-4 outcome market streams. Hosted at wss://hypercore.goldrushdata.com/ws for ultra-low-latency trading and analytics.

- **Human URL:** [https://goldrush.dev/docs/api-reference/hyperliquid/websocket-api/](https://goldrush.dev/docs/api-reference/hyperliquid/websocket-api/)
- **Base URL:** `wss://hypercore.goldrushdata.com/ws`

#### Tags

- Blockchain
- Hyperliquid
- WebSocket
- Order Book
- Real-Time
- Trading

#### Properties

- [Documentation](https://goldrush.dev/docs/api-reference/hyperliquid/websocket-api/)
- [Documentation](https://goldrush.dev/docs/api-reference/hyperliquid/websocket-api/l2-order-book)
- [Documentation](https://goldrush.dev/docs/api-reference/hyperliquid/websocket-api/l2-order-book-diff)
- [Documentation](https://goldrush.dev/docs/api-reference/hyperliquid/websocket-api/l4-order-book)
- [Postman Collection](collections/covalent-foundational-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/covalent-foundational-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/covalent-hyperliquid-info-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/covalent-hyperliquid-info-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/covalent-pipeline-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/covalent-pipeline-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/covalent-streaming-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/covalent-streaming-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/covalent-x402-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/covalent-x402-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### GoldRush x402 API

Pay-per-request HTTP 402 endpoints designed for autonomous AI agents and onchain micropayments. Lists and searches available x402 endpoints, exposes token balance and recent transaction lookups via the 402 settlement flow, and returns per-endpoint metadata for agents to discover and pay for data without a long-lived API key.

- **Human URL:** [https://goldrush.dev/docs/api-reference/foundational-api/x402](https://goldrush.dev/docs/api-reference/foundational-api/x402)
- **Base URL:** `https://api.covalenthq.com`

#### Tags

- Blockchain
- x402
- Pay-Per-Request
- HTTP 402
- AI Agents

#### Properties

- [Documentation](https://goldrush.dev/docs/api-reference/foundational-api/x402)
- [OpenAPI](openapi/covalent-x402-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/covalent-x402-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/covalent-x402-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/covalent-hq)
- [Twitter](https://twitter.com/Covalent_HQ)
- [Git Hub](https://github.com/covalenthq)
- [Website](https://www.covalenthq.com)
- [Website](https://goldrush.dev)
- [Portal](https://goldrush.dev/docs/)
- [Documentation](https://goldrush.dev/docs/api-reference/foundational-api/)
- [Documentation](https://goldrush.dev/docs/api-reference/streaming-api/)
- [Documentation](https://goldrush.dev/docs/api-reference/pipeline-api/)
- [Documentation](https://goldrush.dev/docs/api-reference/hyperliquid/)
- [Changelog](https://goldrush.dev/docs/changelog)
- [Blog](https://goldrush.dev/blog/)
- [Status Page](https://status.goldrush.dev)
- [Pricing](https://goldrush.dev/pricing/)
- [Sign In](https://goldrush.dev/platform/)
- [Support](https://goldrush.dev/support/)
- [Documentation](https://goldrush.dev/chains/)
- [Documentation](https://goldrush.dev/guides/)
- [Case Studies](https://goldrush.dev/case-studies/)
- [Documentation](https://goldrush.dev/agents/)
- [SDK](https://www.npmjs.com/package/@covalenthq/client-sdk)
- [SDK](https://github.com/covalenthq/covalent-api-sdk-go)
- [SDK](https://github.com/covalenthq/goldrush-mcp-server)
- [SDK](https://github.com/covalenthq/goldrush-agent-skills)
- [C L I](https://www.npmjs.com/package/@covalenthq/goldrush-cli)
- [SDK](https://github.com/covalenthq/goldrush-kit)
- [SDK](https://github.com/covalenthq/ai-agent-sdk)
- [Tools](https://github.com/covalenthq/goldrush-enhanced-spam-lists)
- [Tools](https://github.com/covalenthq/refiner)
- [Tools](https://github.com/covalenthq/bsp-agent)
- [Tools](https://github.com/covalenthq/bsp-geth)
- [Authentication](https://goldrush.dev/docs/api-reference/foundational-api/authentication)
- [Rate Limits](https://goldrush.dev/docs/api-reference/foundational-api/rate-limits)
- [Plans](plans/covalent-plans-pricing.yml)
- [Rate Limits](rate-limits/covalent-rate-limits.yml)
- [Fin Ops](finops/covalent-finops.yml)
- [Plans](https://goldrush.dev/pricing/)
- [Authentication](undefined)
- [Documentation](undefined)
- [Compliance](undefined)

## Maintainers

**FN:** Covalent
**Email:** support@covalenthq.com
**URL:** https://goldrush.dev/support/
