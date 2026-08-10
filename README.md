# Japan Holiday Skill

WorkBuddy skill for querying Japanese public holidays and analyzing consecutive holiday patterns.

## Features

- Query Japanese national holidays for any date range
- Analyze consecutive holiday patterns (連休)
- Detect "flying stone" holidays (飛び石連休) where 1 day of paid leave creates a long weekend
- Identify major holiday periods: Golden Week (GW), Obon, Silver Week (SW), New Year
- Visual calendar output with color-coded holiday types
- Triple-source fallback: Calendarific API → bestcalendar.jp → Japanese Holiday API

## Installation

```bash
cp -r japan-holiday ~/.workbuddy/skills/
```

## Setup

1. Copy `config.example.json` to `config.json`:
   ```bash
   cp config.example.json config.json
   ```

2. Get a free Calendarific API key from https://calendarific.com/sign-up

3. Replace `YOUR_CALENDARIFIC_API_KEY` in `config.json` with your actual key.

## Usage

In WorkBuddy, trigger with any of these keywords:
- 日本假期 / 日本休日 / 日本公休日 / 日本祝日
- Japan holiday
- 日本连休 / 日本GW / 日本黄金周

Examples:
- "9月有什么假日"
- "2026年5月日本假期"
- "日本GW是什么时候"
- "日本12月有什么假日"

## Data Sources

| Source | Type | Reliability |
|--------|------|-------------|
| Calendarific API | Primary | High, requires API key |
| bestcalendar.jp | Fallback | High, web scraping |
| Japanese Holiday API | Last resort | Low, may be outdated |
