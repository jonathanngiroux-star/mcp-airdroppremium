# mcp-airdroppremium

MCP server for Airdrop Intel Premium - alerts + scoring API tier (airdropintel extension).

## Tools

### get_airdrop_score
Get airdrop score for a project with detailed breakdown.

**Parameters:**
- `project_id` (string, required): Project ID

### get_alerts
Get real-time alerts for airdrop projects.

**Parameters:**
- `project_id` (string, optional): Filter by project
- `priority` (string, optional): "low", "medium", "high", or "all" (default: "all")

### calculate_ev
Calculate expected value for airdrop participation.

**Parameters:**
- `project_id` (string, required): Project ID
- `hours_per_week` (number, optional): Hours per week you can dedicate (default: 5)
- `capital_at_risk` (number, optional): Capital willing to risk in USD (default: 100)

### list_projects
List airdrop projects with filtering.

**Parameters:**
- `status` (string, optional): Filter by status
- `chain` (string, optional): Filter by chain
- `min_score` (number, optional): Minimum score threshold

## Installation

```bash
pip install -r requirements.txt
```

## Usage

```bash
python main.py
```

## Connecting to Claude Desktop

Add to your `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "airdroppremium": {
      "command": "python",
      "args": ["/path/to/mcp-airdroppremium/main.py"],
      "cwd": "/path/to/mcp-airdroppremium"
    }
  }
}
```

## License

MIT