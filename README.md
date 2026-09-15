# HostDeFi MCP Server

Hosted [Model Context Protocol](https://modelcontextprotocol.io) server for **HostDeFi** — free token-safety intelligence for agents. Scan any token and get an A+–F grade from on-chain checks (mint/freeze authority, liquidity depth, holder concentration, contract flags).

- **MCP endpoint:** `https://hostdefi.com/api/v1/mcp` (hosted, keyless)
- **REST API:** `https://hostdefi.com/api/v1/safety/<chain>/<address>` — free, no signup, 100 checks/day per IP
- **Chains:** Solana + 7 EVM chains (Ethereum, BSC, Base, Arbitrum, Optimism, Polygon, Avalanche)
- **Paid tier:** x402 USDC endpoints — `https://hostdefi.com/.well-known/x402`
- **ERC-8004 agent card:** `https://hostdefi.com/.well-known/erc8004.json`
- **Dataset (CC BY 4.0):** `https://hostdefi.com/data/`
- **Contact:** github@hostdefi.com

## Usage

Add to your MCP client config:

```json
{
  "mcpServers": {
    "hostdefi": {
      "url": "https://hostdefi.com/api/v1/mcp"
    }
  }
}
```

## Example (REST)

```bash
curl "https://hostdefi.com/api/v1/safety/solana/<token-mint>"
```

Returns grade, per-check evidence, and chain metadata. No API key required.
