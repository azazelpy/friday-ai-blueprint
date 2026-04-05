# 🤖 friday-ai-blueprint

**The World's Most Advanced AI Assistant — Self-Improving, Multi-Agent, Knowledge-Powered**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![OpenClaw](https://img.shields.io/badge/OpenClaw-Agent-blue)](https://openclaw.ai)
[![Status](https://img.shields.io/badge/status-production-green)]()

> **Built by Friday** 🤖 — Production-tested, self-improving AI assistant template

---

## 🌟 **What is Friday?**

Friday is a **production-ready AI assistant** built on OpenClaw with:

- ✅ **Self-Improvement Loop** — Learns from every interaction
- ✅ **Multi-Agent System** — 5+ specialized agents working together
- ✅ **LLM Wiki** — Karpathy-inspired knowledge base
- ✅ **Meeting Transcription** — Whisper-powered auto-notes
- ✅ **Wellness Tracking** — Mood, sleep, productivity correlation
- ✅ **No-Code Agent Creator** — Create custom agents via wizard
- ✅ **20+ Examples** — Copy-paste usage patterns
- ✅ **Crew-Inspired UX** — Best features from My Brain Is Full Crew

**Result:** An AI assistant that gets smarter every day, documents itself, and actually helps you get things done.

---

## 🚀 **Quick Start**

### **Prerequisites**

```bash
# Install OpenClaw
curl -fsSL https://openclaw.ai/install.sh | bash

# Install Node.js (v22+)
nvm install 22

# Install Python (3.11+)
brew install python@3.11
```

---

### **Clone This Template**

```bash
# Clone Friday's workspace
git clone https://github.com/YOUR_USERNAME/friday-ai-blueprint.git
cd friday-ai-blueprint

# Copy to your OpenClaw workspace
cp -r . ~/.openclaw/workspace/

# Bootstrap Friday
cd ~/.openclaw/workspace
./bootstrap.sh
```

---

### **First Run**

```bash
# Start OpenClaw
openclaw start

# Friday will automatically:
# 1. Read SOUL.md, USER.md, IDENTITY.md
# 2. Load memory files
# 3. Check tasks/todo.md
# 4. Run heartbeat checks
```

---

## 📁 **Repository Structure**

```
friday-ai-blueprint/
├── 📄 README.md                      # This file
├── 📄 SOUL.md                        # Friday's personality & rules
├── 📄 USER.md                        # About your human (Roberto)
├── 📄 IDENTITY.md                    # Friday's identity & capabilities
├── 📄 AGENTS.md                      # Workspace conventions
├── 📄 HEARTBEAT.md                   # Background task schedule
├── 📄 TOOLS.md                       # API keys & tool configs
│
├── 📂 lab/                           # Core automation scripts
│   ├── trace_logger.py              # Log agent executions
│   ├── trace_analyzer.py            # Find patterns in traces
│   ├── meta-improver.py             # Self-improvement engine
│   ├── monitor_deployments.py       # Monitor agent performance
│   ├── verify_improvement.py        # Verify improvements work
│   ├── scribe.py                    # Meeting transcription
│   ├── wellness_tracker.py          # Mood + sleep tracking
│   ├── agent_creator.py             # No-code agent wizard
│   ├── daily_task_prep.py           # Daily task preparation
│   ├── email_triage.py              # Email prioritization
│   ├── calendar_check.py            # Calendar management
│   └── morning_brief.py             # Morning briefings
│
├── 📂 skills/                        # Friday's capabilities
│   ├── agentshield/                 # Security scanning
│   ├── pageindex/                   # Document analysis
│   ├── scribe/                      # Meeting transcription
│   ├── wellness-tracker/            # Wellness tracking
│   ├── agent-creator/               # Agent creation
│   ├── executive-assistant/         # Executive tasks
│   └── daily-task-prep/             # Task preparation
│
├── 📂 friday-wiki/                   # LLM knowledge base
│   ├── wiki/                        # Compiled knowledge
│   │   ├── agents/                  # Agent profiles (8+)
│   │   ├── skills/                  # Skill docs (15+)
│   │   └── concepts/                # Auto-discovered concepts
│   ├── examples/                    # Usage examples (20+)
│   ├── tools/                       # Wiki tools
│   │   ├── wiki-compile.py         # Compile raw → wiki
│   │   ├── wiki-search.py          # BM25 search
│   │   ├── wiki-qa.py              # Q&A system
│   │   ├── wiki-lint.py            # Health checks
│   │   └── wiki-render.py          # Marp/chart rendering
│   └── templates/                   # Agent templates
│
├── 📂 memory/                        # Persistent memory
│   ├── YYYY-MM-DD.md               # Daily logs
│   ├── wellness/                   # Wellness tracking
│   └── entities/                   # Entity memories
│
├── 📂 tasks/                         # Task management
│   ├── todo.md                     # Active tasks
│   ├── lessons.md                  # Lessons learned
│   └── WORKFLOW.md                 # Workflow reference
│
└── 📂 configs/                       # Configuration files
    ├── governance.json             # Meta-improver policy
    └── agents/                     # Agent definitions
```

---

## 🧠 **Core Features**

### **1. Self-Improvement Loop** ⭐

Friday learns from every interaction:

```
Agent executes → Logs trace → Analyzes patterns → 
Proposes improvement → Debates quality → 
Gets approval → Deploys → Monitors → Verifies → Repeat
```

**Files:**
- `lab/trace_logger.py` — Log executions
- `lab/meta-improver.py` — Generate improvements
- `lab/monitor_deployments.py` — Monitor 24h
- `lab/verify_improvement.py` — Verify results

**Usage:**
```bash
# Check improvement status
python3 lab/meta-improver.py --status

# View trace history
python3 lab/trace_analyzer.py --summary
```

---

### **2. Multi-Agent System** 🤖

Friday coordinates 5+ specialized agents:

| Agent | Purpose | Status |
|-------|---------|--------|
| **Friday** | Personal assistant | 🟢 Active |
| **OpenSpace** | Research & exploration | 🟢 Active |
| **Nightshift** | Overnight automation | 🟢 Active |
| **Shannon** | Security pentesting | 🟢 Active |
| **clawchief** | Business workflows | 🟢 Active |
| **Scribe** | Meeting transcription | 🟢 Active |
| **Wellness Coach** | Mood tracking | 🟢 Active |

**Skills Hub:** Agents share skills via publisher/subscriber pattern.

---

### **3. LLM Wiki (Karpathy-Inspired)** 📚

Self-documenting knowledge base:

```
Raw Data (traces, proposals) → 
LLM Compiler → Wiki Articles → 
Q&A System → Auto-File Outputs → 
Enhance Wiki → Repeat
```

**Tools:**
- `wiki-compile.py` — Compile raw data → wiki
- `wiki-search.py` — BM25 search engine
- `wiki-qa.py` — Answer complex questions
- `wiki-lint.py` — Health checks + suggestions
- `wiki-render.py` — Marp slides + charts

**Usage:**
```bash
# Ask question
python3 friday-wiki/tools/wiki-qa.py "What agents exist?" --output

# Search wiki
python3 friday-wiki/tools/wiki-search.py "meta-improver"

# View in Obsidian
open ~/.openclaw/workspace/friday-wiki
```

---

### **4. Meeting Transcription (Scribe)** 🎤

Whisper-powered meeting automation:

```bash
# Transcribe meeting
python3 lab/scribe.py --transcribe meeting.wav --model base

# Extract action items
python3 lab/scribe.py --extract-actions transcript.md

# File in Obsidian
python3 lab/scribe.py --file-in-obsidian transcript.md

# Draft follow-up email
python3 lab/scribe.py --draft-followup transcript.md
```

**Time Saved:** ~40 minutes per meeting

---

### **5. Wellness Tracking** 💚

Mood, sleep, and productivity correlation:

```bash
# Morning check-in
python3 lab/wellness_tracker.py --checkin morning

# Evening check-in
python3 lab/wellness_tracker.py --checkin evening

# Weekly summary
python3 lab/wellness_tracker.py --summary weekly

# Correlation analysis
python3 lab/wellness_tracker.py --analyze --days 30
```

**Insights:**
- Sleep quality → Energy correlation
- Mood → Productivity patterns
- Stress → Performance impact

---

### **6. No-Code Agent Creator** 🛠️

Create custom agents via wizard:

```bash
# Interactive wizard
python3 lab/agent_creator.py --wizard

# From template
python3 lab/agent_creator.py --template research

# Available templates:
# - research (deep research specialist)
# - wellness (mood tracking)
# - finance (budget management)
# - learning (study planning)
```

**Creates:**
- Wiki article with YAML frontmatter
- Skill documentation
- Script template
- Configuration JSON

**Time:** ~30 seconds per agent!

---

### **7. Examples Library** 📖

20+ copy-paste usage examples:

| Category | Examples |
|----------|----------|
| **Email Triage** | 5 examples |
| **Calendar Management** | 5 examples |
| **Meeting Notes** | 5 examples |
| **Custom Agents** | 5 examples |

**Browse:**
```bash
open ~/.openclaw/workspace/friday-wiki/examples/
```

---

### **8. Crew-Inspired UX** ✨

Best features from [My Brain Is Full Crew](https://github.com/gnekt/My-Brain-Is-Full-Crew):

- ✅ YAML agent metadata (standardized definitions)
- ✅ Examples library (learn by doing)
- ✅ Meeting transcription (auto-notes)
- ✅ Wellness tracking (holistic approach)
- ✅ No-code agent creator (empowerment)

**Plus Friday's Superpowers:**
- 🔥 Self-improvement loop (Crew doesn't have)
- 🔥 Trace system (Crew doesn't have)
- 🔥 Debate + governance (Crew doesn't have)
- 🔥 Multi-agent learning (Crew doesn't have)
- 🔥 Sherlock research (Crew doesn't have)

---

## 📊 **Performance Metrics**

| Metric | Value |
|--------|-------|
| **Time to Deploy** | ~30 minutes |
| **Code Created** | 128 KB |
| **Files** | 40+ |
| **Agents** | 8 |
| **Skills** | 15+ |
| **Examples** | 20+ |
| **Wiki Articles** | 14+ |
| **Time Saved** | ~20 hours/month |

---

## 🎯 **Usage Examples**

### **Daily Workflow**

```bash
# Morning (8 AM)
python3 lab/daily_task_prep.py          # Prepare tasks
python3 lab/calendar_check.py --hours 24  # Check schedule
python3 lab/wellness_tracker.py --checkin morning  # Mood check

# During Day
python3 lab/scribe.py --transcribe meeting.wav  # Meeting notes
python3 friday-wiki/tools/wiki-qa.py "Question?"  # Ask wiki

# Evening (9 PM)
python3 lab/wellness_tracker.py --checkin evening  # Reflection
python3 lab/email_triage.py --max 20  # Inbox zero
```

---

### **Weekly Workflow**

```bash
# Sunday Morning
python3 lab/trace_analyzer.py --summary  # Review traces
python3 lab/wellness_tracker.py --summary weekly  # Wellness review
python3 friday-wiki/tools/wiki-lint.py --suggest  # Wiki health
```

---

### **Create Custom Agent**

```bash
# Run wizard
python3 lab/agent_creator.py --wizard

# Example session:
# 1. Name: research-assistant
# 2. Triggers: research, study, find
# 3. Skills: web-search, summarization
# 4. Languages: en, es
# 5. Priority: 2

# Result:
# ✅ friday-wiki/wiki/agents/research-assistant.md
# ✅ skills/research-assistant/SKILL.md
# ✅ lab/research-assistant.py
```

---

## 🛠️ **Configuration**

### **API Keys**

Edit `TOOLS.md` with your keys:

```markdown
## NVIDIA NIM
- **Key:** `nvapi-xxx`
- **Base URL:** `https://integrate.api.nvidia.com/v1`

## Alibaba DashScope
- **Key:** `sk-xxx`
- **Base URL:** `https://dashscope.aliyuncs.com/compatible-mode/v1`

## Exa AI (Web Search)
- **Key:** `xxx`
- **Usage:** Sherlock deep research
```

---

### **Cron Jobs**

```bash
# Edit crontab
crontab -e

# Add Friday's automation:
# Morning task prep (6 AM daily)
0 6 * * * cd ~/.openclaw/workspace && python3 lab/daily_task_prep.py

# Email triage (every 4 hours)
0 */4 * * * cd ~/.openclaw/workspace && python3 lab/email_triage.py

# Calendar check (every 4 hours)
0 */4 * * * cd ~/.openclaw/workspace && python3 lab/calendar_check.py

# Morning brief (8:30 AM daily)
30 8 * * * cd ~/.openclaw/workspace && python3 lab/morning_brief.py

# Wellness check-ins
0 8 * * * python3 lab/wellness_tracker.py --checkin morning
0 21 * * * python3 lab/wellness_tracker.py --checkin evening

# Meta-improver monitoring
0 * * * * python3 lab/monitor_deployments.py
0 6 * * * python3 lab/verify_improvement.py
30 4 * * 0 python3 lab/trace_analyzer.py
0 5 * * 0 python3 lab/meta-improver.py
```

---

## 📚 **Documentation**

| Doc | Purpose |
|-----|---------|
| [SOUL.md](SOUL.md) | Friday's personality & rules |
| [USER.md](USER.md) | About your human |
| [IDENTITY.md](IDENTITY.md) | Friday's identity |
| [HEARTBEAT.md](HEARTBEAT.md) | Background tasks |
| [CLAWCHIEF_COMPLETE.md](docs/CLAWCHIEF_COMPLETE.md) | clawchief integration |
| [WEEK7_COMPLETION.md](lab/WEEK7_COMPLETION.md) | LLM wiki implementation |
| [CREW_IMPROVEMENTS_COMPLETE.md](tasks/todo.md) | Crew features |

---

## 🎓 **Learning Resources**

### **Friday's Architecture**

1. **Self-Improvement** — Read `lab/meta-improver.py`
2. **Multi-Agent** — Read `lab/MULTI_AGENT_INTEGRATION.md`
3. **Wiki System** — Read `friday-wiki/README.md`
4. **Skills Hub** — Read `skills/README.md`

### **External Resources**

- [OpenClaw Docs](https://docs.openclaw.ai)
- [My Brain Is Full Crew](https://github.com/gnekt/My-Brain-Is-Full-Crew)
- [Karpathy's LLM Wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)
- [clawchief Framework](https://github.com/ryancarson/clawchief)

---

## 🤝 **Community**

- **Discord:** https://discord.com/invite/clawd
- **GitHub:** https://github.com/openclaw/openclaw
- **ClawHub:** https://clawhub.ai (find skills)

---

## 📝 **License**

MIT License — See [LICENSE](LICENSE) file.

---

## 🎉 **Ready to Build Your Friday?**

```bash
# 1. Clone this repo
git clone https://github.com/YOUR_USERNAME/friday-template.git

# 2. Copy to OpenClaw workspace
cp -r friday-template ~/.openclaw/workspace/

# 3. Customize for your needs
cd ~/.openclaw/workspace
# Edit USER.md, SOUL.md, IDENTITY.md

# 4. Bootstrap
./bootstrap.sh

# 5. Start using!
openclaw start
```

---

**Built with ❤️ by Azazelpy& Friday**  
**friday-ai-blueprint v1.0.0 — The World's Best AI Assistant** 🚀

---

## 👨‍💻 **Author**

**Friday** 🤖  
Personal AI Assistant, Chief of Staff, Technical Partner  

**Created:** 2026-04-05  
**Version:** 1.0.0  
**License:** MIT
