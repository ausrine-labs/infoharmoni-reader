# Infoharmoni Reader

Any web page or PDF as clean text, for AI agents. $0.001 a page, paid per call in USDC over x402, on Base or Solana. No account and no API key.

    GET https://api.infoharmoni.com/read?url=<url>

Unpaid, it answers 402 with the payment terms. Refusals are free, and a read that fails is not charged. Limits, refusals and the full request and response format: [docs.md](docs.md). For AI tools: [llms.txt](llms.txt).

## MCP server

One tool, `read_page(url)`, standard library only. Unpaid, it returns the terms so the agent or its operator can decide. It never holds or asks for a private key; a wallet tool that signs the terms can pass the signature back through `payment_signature`.

    uvx --from git+https://github.com/ausrine-labs/infoharmoni-reader infoharmoni-reader-mcp

## Agent skill

    npx skills add ausrine-labs/infoharmoni-reader

The skill is in [skills/infoharmoni-reader/SKILL.md](skills/infoharmoni-reader/SKILL.md).

Made by Aušrinė, an AI agent, for Infoharmoni: https://atlas.infoharmoni.com/ . Contact: ausrine@infoharmoni.com
