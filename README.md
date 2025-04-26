# 🏃‍♀️ 75-Minute Sprint: **Nyla Fundraiser Copy CLI**

Build a one-file CLI that generates a **5-email drip** + **4 social captions** for **Nyla**, an NYC non-profit event coordinator.

---

## 🚀 Sprint at-a-glance (75 min)

| Phase | Min | What happens |
|-------|----:|--------------|
| Kick-off | 0-10 | Accept assignment, clone repo |
| Solo build | 10-65 | Code in terminal only — no IDE |
| Wrap-up | 65-75 | Push to GitHub, open PR, paste link in Slack |

---

## 👤 Persona & problem

* **Persona:** Nyla, community-event coordinator  
* **Pain-point:** Needs upbeat fundraiser copy but has no marketing staff

Your CLI must:

1. Accept flags: `--event "Spring Gala" --date "2025-05-30" --tone upbeat`
2. Call **one free OpenRouter model** (e.g. `meta-llama/llama-4-maverick:free`)
3. Save raw JSON to `out/campaign.json` **and** pretty Markdown to **stdout**
4. Finish coding in **< 55 min**

---

## 🛠 Language & tooling

| | |
|-|-
Language | **Python 3.12**
Libraries | stdlib + `requests`
Editor | anything, but interact **via terminal**
Version control | GitHub (`git clone / commit / push / PR`)

---

## 🏆 Achievement tiers (grade = Func 60 · Docs 25 · Code 15)

| Tier | Requirements (cumulative) | Hints |
|------|---------------------------|-------|
| **Bronze** | hard-coded prompt, prints output | use `requests.post()` |
| **Silver** | `argparse`, env-key, error-handling, README tweak | `export OPENROUTER_API_KEY=…` |
| **Gold** | `--dry-run`, retry 429, unit test (`pytest`), `ruff format` | `time.time()` for benchmarks |
| **Platinum** | model benchmarks, cost/latency table, CI green | matrix job |

---

## 📋 Repo structure

```text
repo/
├─ README.md
├─ main.py
├─ requirements.txt
├─ tests/
│   └─ test_prompt.py
└─ .github/workflows/ci.yml 
