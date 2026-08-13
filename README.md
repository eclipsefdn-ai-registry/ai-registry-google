# AI Registry — Google (Inferred)

> **Inferred vendor repository.** This repo is maintained by the [AI Registry](https://github.com/eclipsefdn-ai-registry/ai-registry-core) project, not by Google. It pre-seeds the registry with skills published by Google at [github.com/google/skills](https://github.com/google/skills) and [github.com/googleworkspace/cli](https://github.com/googleworkspace/cli), an Agent Plugin published at [github.com/gemini-cli-extensions/bigquery-data-analytics](https://github.com/gemini-cli-extensions/bigquery-data-analytics), and MCP servers Google operates itself.
>
> *This entry is based solely on information published through Google's official public channels. Google has not endorsed, approved or validated this listing, and is not necessarily participating in the AI Registry.*

## What this repo contains

Skill approvals for:

- All skills found under the `ads`, `analytics`, and `cloud` categories in the [google/skills](https://github.com/google/skills) repository (Google's official Agent Skills repository, covering Google Cloud and Ads/Analytics products).
- All skills found under `skills/` in the [googleworkspace/cli](https://github.com/googleworkspace/cli) repository (Google Workspace CLI's bundled Agent Skills for Gmail, Drive, Docs, Sheets, Calendar, Chat, and more).

Each approval file uses glob source paths so newly published skills are picked up automatically on the next registry consolidation.

Plugin approval for:

- [`gemini-cli-extensions/bigquery-data-analytics`](https://github.com/gemini-cli-extensions/bigquery-data-analytics) — a [agent-plugins.org](https://agent-plugins.org)-conformant plugin bundling BigQuery-focused Agent Skills, published under the Gemini CLI Extensions org (part of the Google Cloud Data Agent Kit ecosystem).

MCP server approvals for:

- [**MCP Toolbox for Databases**](https://github.com/googleapis/mcp-toolbox) (`io.github.googleapis/mcp-toolbox`) — Google Cloud's open-source MCP server for connecting agents to databases (AlloyDB, BigQuery, Cloud SQL, Spanner, Firestore, and more), announced repeatedly on the official Google Cloud Blog. Registry-listed; also carries a self-published generic config (`npx @toolbox-sdk/server --stdio --prebuilt=<database>`) since the registry only lists the OCI/Docker package.
- [**Google Maps Platform Code Assist**](https://github.com/googlemaps/platform-ai) (`io.github.googlemaps/platform-ai`) — grounds AI coding assistants in official Google Maps Platform docs and code samples. Not found in the MCP registry under this name (an unrelated third party registered the same server under their own GitHub identity, which this approval deliberately does not use), so this approval supplies fallback `metadata` plus a self-published generic config pointing at Google's hosted endpoint (`https://mapscodeassist.googleapis.com/mcp`), recovered from the official repo's README.
- [**Google Workspace Developer Tools**](https://github.com/googleworkspace/developer-tools) (`goog.workspace-developer/developer-tools`) — a docs-search MCP server for Google Workspace API development, bundled into a VS Code/Gemini CLI extension. Registry-listed under Google's own `.goog`-TLD reverse-DNS namespace; self-published generic config points at its hosted endpoint (`https://workspace-developer.goog/mcp`).

No approval is included for Anthropic's MCP-adjacent repos: `anthropics/github-mcp-server` is a fork of GitHub's own server, `anthropics/claude-ai-mcp` tracks issues for Claude.ai's own MCP *client* integration, and `modelcontextprotocol/servers` is explicitly community-built and no longer Anthropic's after MCP's donation to the Linux Foundation's Agentic AI Foundation. None of them is an MCP server Anthropic itself operates as a product integration, unlike the entries above — see `ai-registry-anthropic` for Anthropic's own inferred-vendor repo.

Google Cloud also documents a larger family of managed remote MCP servers (BigQuery, Cloud Run, Cloud Storage, AlloyDB, Spanner, and others) at a predictable `https://<service>.googleapis.com/mcp` endpoint pattern — see [google/mcp](https://github.com/google/mcp) for the full, Google-maintained catalog. Only the three above have been added so far; the rest are candidates for future approvals.

## Documentation

See the [Vendor Guide](https://github.com/eclipsefdn-ai-registry/ai-registry-core#vendor-guide) in the central repository for how vendor repos work, how to add approvals, and how validation runs.
