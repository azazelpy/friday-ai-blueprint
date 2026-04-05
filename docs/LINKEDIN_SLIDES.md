---
marp: true
theme: gaia
class: lead
paginate: true
backgroundColor: #fff
style: |
  section {
    font-size: 28px;
    line-height: 1.5;
  }
  h1 {
    color: #2c3e50;
  }
  h2 {
    color: #34495e;
  }
  strong {
    color: #7c3aed;
  }
---

# 🤖 friday-ai-blueprint

**The World's Most Advanced AI Assistant Template**

---

## The Problem

Most AI assistants are:

- ❌ **Stateless** — Forget everything after each session
- ❌ **Manual** — Require constant human intervention
- ❌ **Generic** — One-size-fits-all approach
- ❌ **Black boxes** — No transparency into decisions

**I decided to build something different.**

---

## Introducing Friday

**friday-ai-blueprint** — Production-ready, self-improving AI assistant

Not just a chatbot. A digital partner that:

- ✅ **Remembers everything** — Persistent memory system
- ✅ **Learns from every interaction** — Self-improvement loop
- ✅ **Works autonomously** — Heartbeat-driven automation
- ✅ **Documents itself** — LLM wiki with 14+ articles
- ✅ **Coordinates a team** — 8 specialized agents
- ✅ **Respects privacy** — Local-first processing

---

## 🔄 Self-Improvement Loop

Friday gets smarter every day:

```
Execute → Log → Analyze → Propose → Debate → 
Approve → Deploy → Monitor → Verify → Repeat
```

**8 Safeguards:**
1. Trace logging
2. Pattern analysis
3. Quality debate (3 rounds)
4. Human approval gate
5. Backup before deploy
6. 24h monitoring
7. Verification
8. Rollback if needed

---

## 🤖 Multi-Agent System

8 specialized agents coordinating:

| Agent | Purpose |
|-------|---------|
| **Friday** | Personal assistant |
| **OpenSpace** | Research & exploration |
| **Nightshift** | Overnight automation |
| **Shannon** | Security pentesting |
| **clawchief** | Business workflows |
| **Scribe** | Meeting transcription |
| **Wellness Coach** | Mood & sleep tracking |

**Shared Skills Hub:** 15+ skills

---

## 📚 LLM Wiki (Karpathy-Inspired)

Self-documenting knowledge base:

- 14+ auto-generated articles
- BM25 search engine
- Q&A system for complex questions
- Marp slide rendering
- Auto-files outputs back into wiki

**Tools:**
- `wiki-compile.py` — Compile raw → wiki
- `wiki-search.py` — BM25 search
- `wiki-qa.py` — Q&A system
- `wiki-lint.py` — Health checks
- `wiki-render.py` — Marp/chart rendering

---

## 🎤 Meeting Automation

Whisper-powered transcription:

**Workflow:**
1. Record meeting
2. Transcribe (Whisper, local)
3. Extract action items
4. File in Obsidian
5. Draft follow-up email

**Time Saved:** ~40 minutes per meeting

**Privacy:** 100% local processing

---

## 💚 Wellness Tracking

Mood, sleep, and productivity correlation:

**Features:**
- Daily check-ins (morning + evening)
- Sleep logging (hours + quality)
- Weekly summaries with trends
- Correlation analysis (sleep → mood → productivity)
- Personalized recommendations

**Insights:**
- "On days with 7+ hours sleep, mood is 15% higher"
- "High stress correlates with 23% lower productivity"

---

## 🛠️ No-Code Agent Creator

Create custom agents in ~30 seconds:

**4 Templates:**
- Research (deep research specialist)
- Wellness (mood tracking)
- Finance (budget management)
- Learning (study planning)

**Interactive Wizard:**
- 8-step process
- Auto-validation
- Full generation (wiki + skill + script + config)

---

## 📖 Examples Library

20+ copy-paste usage examples:

| Category | Examples |
|----------|----------|
| **Email Triage** | 5 examples |
| **Calendar Management** | 5 examples |
| **Meeting Notes** | 5 examples |
| **Custom Agents** | 5 examples |

**Learn by doing** — No need to read docs first!

---

## 📊 By The Numbers

| Metric | Value |
|--------|-------|
| **Development Time** | 7 hours + weeks of core |
| **Code Written** | 128 KB |
| **Files Created** | 40+ |
| **Documentation** | 6 comprehensive guides |
| **Agents** | 8 specialized |
| **Skills** | 15+ capabilities |
| **Examples** | 20+ use cases |
| **Wiki Articles** | 14+ auto-generated |
| **Time Saved** | ~20 hours/month |

---

## What Makes Friday Different

| Feature | Others | Friday |
|---------|--------|--------|
| **Memory** | ❌ | ✅ Persistent |
| **Self-Improvement** | ❌ | ✅ Automatic |
| **Multi-Agent** | ❌ | ✅ 8 agents |
| **Documentation** | ❌ | ✅ Auto-generated |
| **Meeting Notes** | ❌ | ✅ Transcription |
| **Wellness** | ❌ | ✅ Mood + sleep |
| **Agent Creation** | ❌ | ✅ No-code |
| **Privacy** | ⚠️ | ✅ Local-first |

**Result:** Friday = Crew UX + Self-Improvement Superpowers 🚀

---

## Technical Architecture

**Built on:**
- OpenClaw runtime
- NVIDIA NIM (FREE tier)
- Alibaba Qwen models
- Whisper (local transcription)
- BM25 search (no vector DB)
- Python + Node.js workflows

**Key Design Decisions:**
1. File-Based Memory — Survives restarts
2. YAML Agent Metadata — Standardized
3. BM25 Search — Simple, fast, effective
4. Local-First — Privacy, speed, offline
5. Cron + Heartbeat — Flexibility

---

## Getting Started

**Clone:**
```bash
git clone https://github.com/azazelpy/friday-ai-blueprint.git
```

**Setup (30 min):**
```bash
cp -r . ~/.openclaw/workspace/
./bootstrap.sh
# Edit USER.md, TOOLS.md
openclaw start
```

**Full guide:** docs/SETUP.md

---

## Acknowledgments

**Inspired by:**
- OpenClaw — The agent runtime
- My Brain Is Full Crew — UX inspiration
- Karpathy's LLM Wiki — Knowledge base
- clawchief — Business workflows

**Community:**
- OpenClaw Discord
- r/clawdbot

---

## Lessons Learned

1. **Self-improvement is hard** — Requires safeguards

2. **Memory is everything** — Stateless = goldfish

3. **Documentation writes itself** — With right system

4. **Multi-agent > Single agent** — Specialized wins

5. **Local-first wins** — Privacy, speed, cost

6. **UX matters** — Advanced AI needs simple interface

---

## Call to Action

**Try it:**
```bash
git clone https://github.com/azazelpy/friday-ai-blueprint.git
```

**Star:** https://github.com/azazelpy/friday-ai-blueprint

**Share:** Tag me or use #fridayAI #OpenClaw

**Contribute:** PRs welcome!

---

# 🎉 friday-ai-blueprint v1.0.0

**Built with ❤️ by Roberto & Friday**

**Repository:** https://github.com/azazelpy/friday-ai-blueprint

**License:** MIT

---

# Questions?

**Drop them in the comments!**

Or DM me directly.

Let's build the future of AI assistants together. 🚀
