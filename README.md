# DB Skills Collection

A small collection of Codex skills focused on databases, data platforms, and AI.

## Skills

- `skills/db-ai-trendwatch`: Monitor and analyze AI capability trends across
  databases and data platforms.
- `skills/db-saas-trendwatch`: Monitor and analyze trends in how SaaS products
  use databases (multi-tenant patterns, scaling, migrations, analytics/search/AI).
- `skills/hn-data-ai-7d`: Summarize the last 7 days of HN discussion on data + AI
  database topics.

## Install
Clone and copy the skill you want into your Codex skills directory:
```
git clone https://github.com/BornChanger/db-ai-trendwatch
cd db-ai-trendwatch
cp -R skills/<skill-name> ~/.codex/skills/
```

Or symlink it:
```
ln -s /path/to/db-ai-trendwatch/skills/<skill-name> ~/.codex/skills/<skill-name>
```

## How to use
Invoke a skill by name in Codex, for example:
- "Use db-ai-trendwatch to generate a weekly brief for the last 30 days."
- "Use db-saas-trendwatch to summarize SaaS database architecture trends."
- "Use hn-data-ai-7d to summarize HN threads from the last 7 days."

## License
Apache-2.0. See `LICENSE` and `NOTICE`.
