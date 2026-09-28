Skip to content
hooktracehq
.github
Repository navigation
Code
Issues
Pull requests
Agents
Actions
Projects
Wiki
Security and quality
Insights
Settings
hooktracehq/.github is a special repository: this README.md will appear on your public organization profile, visible to anyone.
.github/profile
/
README.md
in
main

Edit

Preview
Indent mode

Spaces
Indent size

2
Line wrap mode

No wrap
Editing README.md file contents


  1
  2
  3
  4
  5
  6
  7
  8
  9
 10
 11
 12
 13
 14
 15
 16
 17
 18
 19
 20
 21
 22
 23
 24
 25
 26
 27
 28
 29
 30
 31
 32
 33
 34
 35
 36
 37
 38
 39
 40
 41
 42
 43
 44
 45
 46
 47
 48
 49
 50
 51
 52
 53
 54
 55
 56
 57
 58
 59
 60
 61
 62
 63
 64
 65
 66
 67
 68
 69
 70
 71
 72
 73
 74
 75
 76
 77
 78
 79
 80
 81
 82
 83
 84
 85
 86
 87
 88
 89
 90
 91
 92
 93
 94
 95
 96
 97
 98
 99
100
101
102
103
104
105
106
107
108
109
110
111
112
113
114
115
# HookTrace

**Open-source webhook infrastructure for developers.**

Receive, inspect, deliver, retry, and replay webhooks with a self-hostable stack built for visibility and control.

<p align="center">
  <a href="https://hooktrace.xyz">Website</a>
  ·
  <a href="https://github.com/hooktracehq/hooktrace">GitHub</a>
  ·
  <a href="https://github.com/hooktracehq/hooktrace/tree/main/docs">Documentation</a>
</p>

---

## What is HookTrace?

Webhooks are easy until something goes wrong.

A provider sends an event.
Your endpoint returns `500`.
A downstream service goes offline.
An event arrives twice.
You need to know what happened three hours ago.

HookTrace gives you visibility and control over that lifecycle.

```text
Webhook Provider
       │
       ▼
   HookTrace
       │
       ├── Receive
       ├── Inspect
       ├── Store
       ├── Deliver
       ├── Retry
       └── Replay
              │
              ▼
       Your Application
```

## Built for webhook debugging

* 🔌 **Receive** — Accept webhooks through configurable routes
* 🔎 **Inspect** — See payloads, headers, providers, and event types
* 🚚 **Deliver** — Forward events to configurable targets
* 🔁 **Retry** — Recover from temporary delivery failures
* ▶️ **Replay** — Re-process events when you need to
* 🛠️ **Tunnels** — Test webhooks against local development environments
* 📊 **Observe** — Monitor activity and infrastructure metrics
* 🔐 **Self-host** — Run the entire stack on infrastructure you control

## Open source

HookTrace is released under the **Apache License 2.0**.

You can inspect the code, self-host it, modify it, and contribute to the project.

## Stack

```text
Next.js        Dashboard
FastAPI        API
PostgreSQL     Event & application data
Redis          Queues & realtime infrastructure
Python         Workers & tunnel services
Prometheus     Metrics
Docker         Self-hosting
```

## Get started

```bash
git clone https://github.com/hooktracehq/hooktrace.git
cd hooktrace
cp .env.example .env
docker compose up -d
```

Then open:

```text
Dashboard → http://localhost:3000
API       → http://localhost:3001
API Docs  → http://localhost:3001/docs
```

### Learn more

**[Visit HookTrace →](https://hooktrace.xyz)**

**[Read the Documentation →](https://github.com/hooktracehq/hooktrace/tree/main/docs)**

**[Explore the Repository →](https://github.com/hooktracehq/hooktrace)**

---

## Contributing

HookTrace is built in public.

Bug reports, documentation improvements, integrations, tests, and code contributions are welcome.

**[Contributing Guide →](https://github.com/hooktracehq/hooktrace/blob/main/docs/development/contributing.md)**

---

**Receive. Inspect. Deliver. Retry. Replay.**

Built for developers who need to know what happened to their webhooks.

Use Control + Shift + m to toggle the tab key moving focus. Alternatively, use esc then tab to move to the next interactive element on the page.
No file chosen
Attach files by dragging & dropping, selecting or pasting them.
