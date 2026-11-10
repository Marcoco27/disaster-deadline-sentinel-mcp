# Disaster Deadline Sentinel

After a federal disaster, two clocks start for every designated US county: the last day to apply for individual assistance, and the date to which federal tax deadlines are postponed.

For 1 to 25 county FIPS codes, this MCP server and HTTP API return the disasters declared in the last 18 months, whether individual assistance was granted, the application deadline and the days left, the IRS postponement date read from the matching IRS news release (with its URL), the end of the mandatory 60-day postponement of 26 CFR 301.7508A-1(g), and the latest of the two. Days are counted in the county's own time zone, including the few counties split by a time-zone border.

- MCP (streamable HTTP): `https://disasters.amacunia.fr/mcp`, tools `disasters_lookup` (paid, 0.01 USDC per call via x402 on Base) and `disasters_example` (free).
- HTTP: `GET https://disasters.amacunia.fr/v1/disasters?fips=12005` (x402, 0.01 USDC; free trial: 3 calls per day).
- Machine-readable: `/llms.txt`, `/.well-known/x402`, `/terms`.
- Paying client example: [`examples/pay_mcp.py`](examples/pay_mcp.py).

No account, no API key, no personal data.

## Disclaimer

Information only, not legal or tax advice; it does not replace a qualified attorney or tax professional. This product uses the Federal Emergency Management Agency's OpenFEMA API, but is not endorsed by FEMA. The Federal Government or FEMA cannot vouch for the data or analyses derived from these data after the data have been retrieved from the Agency's website(s). Not affiliated with or endorsed by FEMA, the IRS or any U.S. government agency. Terms of use: https://disasters.amacunia.fr/terms
