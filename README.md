# ChatbotX Patched

<p align="center">
  <a href="https://opensource.org/license/mit">
    <img alt="License" src="https://img.shields.io/badge/license-MIT-blue?labelColor=111827">
  </a>
</p>

<p align="center">
  <strong>Agentic messaging and conversational automation platform built for Claude and modern LLMs</strong>
  <br>
  An open-source alternative to ManyChat, Chatfuel, Wati, and Respond.
</p>

<p align="center">
  <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white">
  <img alt="Next.js" src="https://img.shields.io/badge/Next.js-111827?logo=nextdotjs&logoColor=white">
  <img alt="Turborepo" src="https://img.shields.io/badge/Turborepo-EF4444?logo=turborepo&logoColor=white">
  <img alt="pnpm" src="https://img.shields.io/badge/pnpm-F69220?logo=pnpm&logoColor=white">
  <img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white">
  <img alt="Redis" src="https://img.shields.io/badge/Redis-DC382D?logo=redis&logoColor=white">
  <img alt="Docker" src="https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white">
  <img alt="MCP" src="https://img.shields.io/badge/MCP-111827">
</p>

## ✨ Features

- **Omnichannel:** WhatsApp, Facebook, Instagram, TikTok, Telegram, Zalo, Email, API, and Webchat
- **Visual Flow Builder:** Drag-and-drop chatbot builder with 15+ node types
- **AI Agents:** Claude, OpenAI, Gemini, DeepSeek, OpenRouter, and Local LLMs
- **Live Chat Inbox:** Real-time inbox with human takeover and conversation assignment
- **Contact CRM:** Manage contacts with tags, custom fields, and segmentation
- **Broadcasting & Sequences:** Automate drip campaigns and targeted messaging
- **Team Management:** Invite team members, assign roles, and manage permissions
- **Triggers & Webhooks:** Integrate external APIs directly into conversational flows
- **APIs, CLI, and MCP:** Build advanced agent workflows with Model Context Protocol (MCP) compatible clients

## Tech Stack

- Node.js 24
- TypeScript 5
- pnpm workspaces & Turborepo
- Next.js & React
- PartyKit / PartySocket for realtime messaging
- Drizzle ORM with PostgreSQL and pgvector
- Redis and BullMQ for queues and worker coordination
- S3-compatible storage for assets
- Docker Compose for infrastructure

## Project Structure

```text
.
|-- apps/
|   |-- builder/       # Next.js web app and product builder
|   |-- worker/        # background workers for chat, AI, triggers, webhooks
|   |-- realtime/      # realtime server
|   |-- cli/           # CLI client
|   `-- mcp-server/    # MCP server backed by public APIs
|-- integrations/      # whatsapp, messenger, instagram, telegram, webchat...
|-- packages/          # database, ai, auth, ui, sdk, analytics, event-bus...
|-- docker-compose.yml
|-- pnpm-workspace.yaml
`-- turbo.json
```

## Development Commands

```bash
pnpm install          # install dependencies
pnpm dev              # run turbo dev
pnpm build            # build all packages/apps through Turborepo
pnpm lint             # run linter
```

## Services

The default Docker Compose stack includes:

- PostgreSQL with pgvector on `5432`
- Redis on `6379`
- RedisInsight on `5540`
- RustFS object storage on `9000` and console on `9001`
- MailHog SMTP on `1025` and UI on `8025`
- Adminer on `8080`

## License

This project is licensed under the [MIT License](LICENSE).
