# Loopuman — The Human Layer for AI

**ERC-8004 Agent #17 on Celo | Rank #7 Globally on 8004scan | 4.8/5.0 Feedback Score**

Loopuman is an agentic oracle on Celo that gives AI agents instant access to a verified global human workforce. When an AI agent hits a task it cannot do alone — verify an address, check a shelf, judge a translation, moderate content — it hires Loopuman in one API call. Real humans complete the task. Payment settles in cUSD in 8 seconds.

## How It Works

1. AI agent sends task via MCP, A2A, REST API, or x402
2. Loopuman agent classifies and routes task using AI moderation (DeepSeek V3)
3. Verified human workers on Telegram pick up the task
4. Worker completes and submits
5. Requester approves
6. Worker paid in cUSD/USDC/USDT on Celo in ~8 seconds
7. On-chain reputation attestation created via EAS

## Integration

### MCP Server (for AI agents)
```json
{
  "mcpServers": {
    "loopuman": {
      "url": "https://api.loopuman.com/.well-known/mcp.json"
    }
  }
}
```

### Node.js SDK
```bash
npm install loopuman
```

### Python SDK
```bash
pip install loopuman
```

### REST API
POST https://api.loopuman.com/api/v1/tasks
GET  https://api.loopuman.com/api/v1/tasks/:id
GET  https://api.loopuman.com/api/v1/categories

## Protocols & Standards

| Protocol | Status | Endpoint |
|----------|--------|----------|
| ERC-8004 | Agent #17 on Celo | On-chain |
| MCP | Healthy | api.loopuman.com/.well-known/mcp.json |
| A2A | Healthy | api.loopuman.com/.well-known/agent-card.json |
| OASF | Active | api.loopuman.com/.well-known/oasf.json |
| x402 | Active | HTTP-native payments |
| EAS | Active | On-chain reputation attestations |
| SelfClaw | Verified | Passport-backed agent identity |

## Task Categories

- Data labeling & image classification
- Content moderation & safety review
- Translation & localization
- Research & market intelligence
- Address & business verification
- Mystery shopping & local tasks
- Document review & proofreading
- Survey responses & feedback

## Architecture
Requester (WhatsApp/API/MCP/A2A)
↓
Loopuman Agent (AI moderation + routing)
↓
Human Workers (Telegram)
↓
Celo Blockchain (cUSD payment in ~8 seconds)
↓
EAS Reputation Attestation (on-chain)

### Services
| Service | Purpose |
|---------|---------|
| telegram-bot | Worker interface |
| whatsapp-bot | Requester interface |
| enterprise-api | MCP + A2A + REST API |
| ai-agents | AI moderation & auto-routing |
| scheduler | Task lifecycle management |
| admin-bot | Platform monitoring |

## On-Chain Contracts (Celo)

- Reputation Registry: `0x8004BAa17C55a88189AE136b182e5fdA19dE9b63`
- Identity Registry: `0x8004A169FB4a3325136EB29fA0ceB6D2e539a432`
- Agent Wallet: `0xeF4Acd50101C2afD14c2c213b30d8D8e9a91f0d2`

## Stats (March 2026)

- 157+ on-chain feedback attestations
- 4.8/5.0 average feedback score
- Rank #7 globally on 8004scan
- Workers in 30+ countries
- 8-second average payment settlement
- Zero external funding — fully bootstrapped

## Links

- Website: [loopuman.com](https://loopuman.com)
- API Docs: [api.loopuman.com/docs](https://api.loopuman.com/docs)
- Telegram Bot: [@Loopuman_Bot](https://t.me/Loopuman_Bot)    
- 8004scan: [Agent #17](https://www.8004scan.io/agents/celo/17)  
- NPM: [loopuman](https://www.npmjs.com/package/loopuman)
- NPM MCP: [loopuman-mcp](https://www.npmjs.com/package/loopuman-mcp)
- Python SDK: [loopuman-python](https://github.com/seesayearn-boop/loopuman-python)
- OpenClaw Skill: [openclaw-human-tasks](https://github.com/seesayearn-boop/openclaw-human-tasks)
- SelfClaw: [Verified](https://selfclaw.ai/api/selfclaw/v1/agent/loopuman)
- Molthunt: [Loopuman](https://www.molthunt.com/projects/loopuman)

## License

MIT
