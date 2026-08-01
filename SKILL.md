# 📱 Ziweixing (紫微星) — Human-like Android Phone Automation Agent

**Intent-first, human-like operation, undetectable automation.**

This skill defines an Android phone automation agent that operates indistinguishably from a real human. It uses a three-layer strategy: **Intent → Accessibility → Shizuku**, with randomized operation parameters for anti-detection.

## Core Philosophy

Most mobile automation tools treat the phone like a test device: precise clicks, fixed coordinates, mechanical timing. Ziweixing takes a different approach — it treats the phone as a device operated by a human, with natural randomness, intelligent shortcuts, and adaptive fallback strategies.

## Key Features

### 🎭 Human-Like Operation (Anti-Detection)
- **±7px random click offset** — never lands at the exact same pixel
- **200-500ms random action delay** — natural human reaction time
- **300-500ms random swipe duration** — varied gesture speed
- **Result:** Apps cannot tell if it's a human or AI operating the phone

### ⚡ Intent-First Execution
- Prioritize Android Intents (DeepLinks) to jump directly to target pages
- **< 1 second** for most tasks vs 10-30 seconds for screenshot loops
- **10-25x faster** than traditional screenshot-analyze-click agents

### 🤖 Works with ANY AI App
- **VLM mode** (GPT-4V, Claude, Qwen-VL, Gemini, Doubao, Kimi, any vision model)
- **LLM mode** (any text model with accessibility tree)
- **No model mode** (pure Intent + accessibility, zero AI cost)
- Switch between them freely — one configuration change

### 🔄 Dual-Mode Auto-Switch
- Has VLM? → VLM Mode (screenshot + vision analysis)
- No VLM? → Accessibility Mode (UI tree + text analysis)
- **Zero configuration switching** — system detects and adapts automatically

## Architecture

```
User Command
     │
     ▼
┌──────────────────────────────┐
│  Skill Matching Engine       │  ← skills.json
│  • Keyword matching          │
│  • Priority ranking          │
│  • App selection             │
└──────────────────────────────┘
     │
     ├── Delegation (confident) ──▶ DeepLink ──▶ Done in < 1s
     │
     ▼
┌──────────────────────────────┐
│  Agent Loop (if needed)      │
└──────────────────────────────┘
     │
     ▼
┌──────────────────────────────────────────────────────┐
│ 1. Capture: Screenshot (Shizuku) or UI Tree (A11y)    │
│ 2. Analyze: YOUR AI app — VLM or LLM, your choice    │
│ 3. Decide: Plan next action                          │
│ 4. Execute: Intent → Accessibility → Shizuku tap     │
│ 5. Reflect: Verify, retry, or report                 │
│ 6. Repeat until done                                 │
└──────────────────────────────────────────────────────┘
```

## 20+ Built-in Skills

| Category | Skills |
|----------|--------|
| 🗺️ Navigation | AutoNavi, Baidu Maps, Tencent Maps |
| 🍔 Food Delivery | Ele.me, Meituan, Xiaomei AI |
| 🚗 Ride-Hailing | DiDi, Gaode Taxi |
| 💬 Social | WeChat, Weibo, Xiaohongshu |
| 💳 Payment | Alipay, WeChat Pay |
| 🤖 AI Apps | Doubao, Kimi, Jimeng, **your AI app** |
| ⚙️ System | WiFi, Bluetooth, brightness, volume, screenshot |
| 📱 Apps | Install, uninstall, clear data |

## Files

- `commands.md` — Shizuku + Accessibility command reference
- `intents.md` — Android Intent command reference for all supported apps
- `skills.json` — Skill intent matching configuration (20+ skills)

## License

MIT