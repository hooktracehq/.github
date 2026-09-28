<h1 align="center">HookTrace</h1>

<p align="center">
  <strong>Open-source webhook infrastructure for developers.</strong><br />
  Receive, inspect, deliver, retry, and replay webhooks with a self-hostable stack built for visibility and control.
</p>

<p align="center">
  <a href="LICENSE"><img alt="License: Apache 2.0" src="https://img.shields.io/badge/license-Apache%202.0-blue.svg" /></a>
  <img alt="Self-hosted" src="https://img.shields.io/badge/self--hosted-yes-success" />
  <img alt="Status: v0.1.0" src="https://img.shields.io/badge/version-v0.1.0-lightgrey" />
</p>

<!-- Replace with a real dashboard screenshot or GIF, e.g. docs/assets/dashboard.png -->
<!-- <p align="center"><img src="docs/assets/dashboard.png" alt="HookTrace dashboard" width="900" /></p> -->

---

## Why HookTrace?

Webhooks fail, and they usually fail silently. HookTrace shows you what happened to every event.

| When... | HookTrace lets you... |
| --- | --- |
| Webhooks fail silently | See whether an event arrived, what payload was received, and what happened during delivery. |
| Downstream services go down | Retry failed deliveries instead of losing events. |
| You need to debug production events | Inspect payloads, headers, providers, and delivery attempts. |
| You need to reproduce an event | Replay it without triggering the provider again. |

## How it works

```text
Webhook Provider
       ↓
   HookTrace
       ↓
Receive → Inspect → Store → Deliver
                         ↓
                   Retry / Replay
                         ↓
                 Your Application
```

## Features

- **Receive** webhooks from any provider
- **Inspect** payloads, headers, and providers
- **Store** every event
- **Deliver** to your configured targets
- **Retry** failed deliveries
- **Replay** past events on demand
- **Local webhook tunnels** for development
- **Provider integrations** (see below)
- **Metrics and observability**
- **Self-hosting** with Docker Compose

## Quick start

```bash
git clone https://github.com/hooktracehq/hooktrace.git
cd hooktrace
cp .env.example .env
docker compose up -d
```

Once the stack is running:

| Service | URL |
| --- | --- |
| Dashboard | http://localhost:3000 |
| API | http://localhost:3001 |
| API Docs | http://localhost:3001/docs |

## Local development with tunnels

HookTrace tunnels let you receive real webhook requests locally without exposing your application directly to the public internet.

<!-- Add tunnel setup steps here, matching the actual CLI/UI in the repo. -->

## Integrations

Provider concepts currently covered:

- Stripe
- GitHub
- Razorpay
- Shopify
- Slack
- Discord
- Notion
- Supabase
- Generic webhooks

> Note: check each provider against the current code before release and mark anything that is not yet production-ready.

## Architecture

```text
                    ┌───────────────┐
                    │ Webhook       │
                    │ Providers     │
                    └───────┬───────┘
                            │
                            ▼
                    ┌───────────────┐
                    │   HookTrace   │
                    │      API      │
                    └───────┬───────┘
                            │
                 ┌──────────┼──────────┐
                 ▼          ▼          ▼
            PostgreSQL    Redis      Workers
                                      │
                                      ▼
                              Delivery Targets
```

## Configuration

Copy `.env.example` to `.env` and adjust the values for your environment.

<!-- Document key environment variables here. -->

## Contributing

Contributions are welcome. Open an issue to discuss larger changes, then submit a pull request.

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Open a pull request

## License

HookTrace is open source and released under the [Apache License 2.0](LICENSE). Inspect the code, self-host the stack, modify it for your needs, and contribute.

## Links

- GitHub: https://github.com/hooktracehq/hooktrace
- Docs: http://localhost:3001/docs (when self-hosting)
