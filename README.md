# Acronis Cyber Protect Cloud MCP setup and connection checker

Generate Acronis Cyber Protect Cloud MCP client configuration, inspect available tools and validate hosted endpoint access through PipMCP.

Maintainer: jannikco · License: MIT · Verification: **mock-only**

## Quick start

Requires Node.js 22 or later.

```sh
npm ci
npm test
npm start
```

The default example runs locally without credentials and makes no external changes. Verification status describes recorded evidence; local configuration tests do not establish that provider authentication or execution works.

## Connect acronis-cyber-protect-cloud-ca18

[Create or sign in to PipMCP](https://pipmcp.com/register?app=acronis-cyber-protect-cloud-ca18&utm_source=github&utm_campaign=github-acronis-cyber-protect-cloud-ca18-mcp) and select the integration. Connect your authorized provider account and copy its hosted MCP endpoint. Set PIPMCP_ENDPOINT and, if required, PIPMCP_TOKEN in your environment. Run npm start to produce client configuration; run npm start -- --live for a read-only connection check. Provider app presence is catalog evidence, not live verification.

## Managed service

[Continue with PipMCP](https://pipmcp.com/register?app=acronis-cyber-protect-cloud-ca18&utm_source=github&utm_campaign=github-acronis-cyber-protect-cloud-ca18-mcp). This repository is maintained by the integration team and does not imply endorsement by LinkedIn or other providers.

## Provenance and support

Source revision: 5e67f3b8b62cb3e9a87a2731c4b6b948ed1516e7fe055aaef2d48e4ec76f5f68. The complete manifest is in integration.json; SHA256SUMS covers the reviewed artifact. Open a repository issue without credentials or personal data. See SECURITY.md for sensitive reports. No telemetry is sent by this code; signup links include explicit campaign parameters.

## Provider setup inventory

Run `npm start -- --setup` to inspect this app's recorded authentication requirements and setup links offline. Credentials are entered in PipMCP; this repository lists required field names only.

```json
{
  "type": "token_exchange",
  "requiredCredentialFields": [
    "provider_exchange_credentials"
  ],
  "requiredHeaderNames": [],
  "helpUrl": "https://developer.acronis.com/doc/account-management/v2/guide/getting-started/authenticating.html",
  "tenantRequired": true,
  "accountParameterNames": []
}
```

Provider documentation: https://developer.acronis.com/doc/account-management/v2/reference/openapi.json
Provider website: https://www.acronis.com/en/products/cloud/cyber-protect/
