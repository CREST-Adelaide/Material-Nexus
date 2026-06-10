# Example: Day-Based Course (Bootcamp)

Pattern used by **OpenClaw Mastery for Everyone** — one capability per day, theory + hands-on split.

## Tree

```
courses/openclaw-mastery/
├── README.md
├── FAQ.md
├── getting-your-api-key.md
├── best-resources.md
├── diagrams/
│   ├── hero-image.png
│   └── certificate-sample.png
└── days/
    ├── day-01-install-secure/
    │   ├── learn.md
    │   ├── build.md
    │   └── agent-instructions-security.md
    ├── day-02-give-it-a-soul/
    │   ├── learn.md
    │   └── build.md
    ├── day-03-connect-a-channel/
    │   ├── learn.md
    │   └── build.md
    ...
    └── day-10-what-comes-next/
        ├── learn.md
        └── build.md
```

## Course README Template

```markdown
# OpenClaw Mastery for Everyone

10 days, ~20 min/day. Build a personal AI assistant step by step.

## How it works
- **learn.md** — theory for the day
- **build.md** — hands-on; paste prompts that reference agent-instructions files

## Days
| Day | Topic |
|-----|-------|
| [Day 1](days/day-01-install-secure/learn.md) | Install & secure |
| [Day 2](days/day-02-give-it-a-soul/learn.md) | Identity files |
...

## Certification
[Take assessment →](https://forms.example.com)
```

## learn.md Template

```markdown
# Day 4: Make It Proactive

## What you'll build
An evening reflection delivered on a schedule.

## Why it matters
...

## How it works under the hood
...
```

## build.md Template

```markdown
# Day 4: Build — Make It Proactive

## Prerequisites
- Completed Day 3

## Steps
1. Open your agent chat
2. Paste this prompt: (references `./agent-instructions-create-cron.md`)
3. Confirm the schedule in your UI

## Verify
- [ ] Cron job appears in config
- [ ] Test message received on phone
```

## When to use

- Daily bootcamps
- Build-along where learners ship something each day
- Agent-assisted setup (optional instruction files)
