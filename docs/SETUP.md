# 🚀 Friday Setup Guide

**friday-ai-blueprint — Complete setup in ~30 minutes**

---

## 📋 **Prerequisites**

### **1. Install OpenClaw**

```bash
# Install OpenClaw
curl -fsSL https://openclaw.ai/install.sh | bash

# Verify installation
openclaw --version
```

---

### **2. Install Node.js**

```bash
# Install nvm (Node Version Manager)
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash

# Restart terminal, then install Node.js
nvm install 22
nvm use 22

# Verify
node --version  # Should show v22.x.x
npm --version   # Should show 10.x.x
```

---

### **3. Install Python**

```bash
# macOS
brew install python@3.11

# Verify
python3 --version  # Should show 3.11.x
```

---

## 📥 **Clone friday-ai-blueprint**

```bash
# Clone this repository
git clone https://github.com/YOUR_USERNAME/friday-ai-blueprint.git
cd friday-ai-blueprint

# Copy to OpenClaw workspace
cp -r . ~/.openclaw/workspace/

# Or symlink (for development)
ln -s $(pwd) ~/.openclaw/workspace
```

---

## ⚙️ **Configuration**

### **Step 1: Edit USER.md**

```bash
# Open USER.md
code ~/.openclaw/workspace/USER.md

# Update with your info:
# - Name, timezone, location
# - Projects & interests
# - Communication preferences
# - Technical stack
```

---

### **Step 2: Edit TOOLS.md**

```bash
# Open TOOLS.md
code ~/.openclaw/workspace/TOOLS.md

# Add your API keys:
# - NVIDIA NIM API key
# - Alibaba DashScope API key
# - Exa AI API key (for web search)
```

**Get API Keys:**
- **NVIDIA NIM:** https://build.nvidia.com (FREE tier: 1,000 credits)
- **Alibaba DashScope:** https://dashscope.console.aliyun.com
- **Exa AI:** https://exa.ai

---

### **Step 3: Edit SOUL.md (Optional)**

```bash
# Open SOUL.md
code ~/.openclaw/workspace/SOUL.md

# Customize Friday's personality if desired:
# - Communication style
# - Work patterns
# - Boundaries
```

---

### **Step 4: Edit HEARTBEAT.md**

```bash
# Open HEARTBEAT.md
code ~/.openclaw/workspace/HEARTBEAT.md

# Configure background tasks:
# - Email check frequency
# - Calendar check frequency
# - Wellness tracking schedule
# - Security audit schedule
```

---

## 🔐 **API Keys Setup**

### **NVIDIA NIM (FREE)**

```bash
# Get key from: https://build.nvidia.com
# Sign up → Get API key

# Add to TOOLS.md:
## NVIDIA NIM
- **Key:** `nvapi-your-key-here`
- **Base URL:** `https://integrate.api.nvidia.com/v1`
```

**Models Available:**
- `minimaxai/minimax-m2.5` (PRIMARY - FREE)
- `nvidia/nemotron-4-340b-instruct` (Fallback 1)
- `deepseek-ai/deepseek-r1-distill-qwen-32b` (Fallback 2)
- `meta/llama-3.1-70b-instruct` (Fallback 3)

---

### **Alibaba DashScope**

```bash
# Get key from: https://dashscope.console.aliyun.com
# Sign up → API Key Management

# Add to TOOLS.md:
## Alibaba Cloud (DashScope)
- **Key:** `sk-your-key-here`
- **Base URL:** `https://dashscope.aliyuncs.com/compatible-mode/v1`
```

**Models Available:**
- `qwen3.5-plus` (PRIMARY - 256K context, vision)
- `qwen-vl-max` (Vision specialist)
- `qwen-plus` (Best value, 128K-1M context)
- `qwen-turbo` (Fast, lowest cost)

---

### **Exa AI (Web Search)**

```bash
# Get key from: https://exa.ai
# Sign up → API Keys

# Add to TOOLS.md:
## Exa AI (Web Search)
- **Key:** `your-key-here`
- **Usage:** Sherlock deep research agent
```

---

## 🧪 **Test Setup**

### **Test 1: OpenClaw Status**

```bash
# Check OpenClaw status
openclaw status

# Should show:
# ✅ Gateway running
# ✅ Node connected
# ✅ Models configured
```

---

### **Test 2: Friday Bootstrap**

```bash
# Run bootstrap
cd ~/.openclaw/workspace
./bootstrap.sh

# Friday will:
# 1. Read SOUL.md, USER.md, IDENTITY.md
# 2. Load memory files
# 3. Check tasks/todo.md
# 4. Initialize systems
```

---

### **Test 3: Basic Commands**

```bash
# Test wiki search
python3 friday-wiki/tools/wiki-search.py "friday"

# Test wellness tracker
python3 lab/wellness_tracker.py --checkin morning

# Test agent creator
python3 lab/agent_creator.py --list-templates
```

---

## 📅 **Install Cron Jobs**

### **Automated Tasks**

```bash
# Edit crontab
crontab -e

# Add Friday's automation:

# Morning task prep (6 AM daily)
0 6 * * * cd /Users/roberto/.openclaw/workspace && python3 lab/daily_task_prep.py >> lab/logs/daily-task-prep.log 2>&1

# Email triage (every 4 hours)
0 */4 * * * cd /Users/roberto/.openclaw/workspace && python3 lab/email_triage.py >> lab/logs/email-triage.log 2>&1

# Calendar check (every 4 hours)
0 */4 * * * cd /Users/roberto/.openclaw/workspace && python3 lab/calendar_check.py >> lab/logs/calendar-check.log 2>&1

# Morning brief (8:30 AM daily)
30 8 * * * cd /Users/roberto/.openclaw/workspace && python3 lab/morning_brief.py >> lab/logs/morning-brief.log 2>&1

# Wellness check-ins
0 8 * * * python3 lab/wellness_tracker.py --checkin morning >> lab/logs/wellness.log 2>&1
0 21 * * * python3 lab/wellness_tracker.py --checkin evening >> lab/logs/wellness.log 2>&1

# Meta-improver monitoring
0 * * * * python3 lab/monitor_deployments.py >> lab/logs/monitoring.log 2>&1
0 6 * * * python3 lab/verify_improvement.py >> lab/logs/verification.log 2>&1
30 4 * * 0 python3 lab/trace_analyzer.py >> lab/logs/trace-analysis.log 2>&1
0 5 * * 0 python3 lab/meta-improver.py >> lab/logs/meta-improver.log 2>&1

# Weekly wiki compilation
0 5 * * 0 cd /Users/roberto/.openclaw/workspace && python3 friday-wiki/tools/wiki-compile.py --all >> lab/logs/wiki-compile.log 2>&1
```

---

## 🎯 **First Day with Friday**

### **Morning (8 AM)**

```bash
# Friday automatically runs:
python3 lab/daily_task_prep.py      # Prepare tasks
python3 lab/calendar_check.py       # Check schedule
python3 lab/morning_brief.py        # Generate brief
python3 lab/wellness_tracker.py     # Morning check-in
```

**You:** Review morning brief, approve tasks

---

### **During Day**

```bash
# Use Friday via:
# 1. Telegram (if configured)
# 2. CLI commands
# 3. OpenClaw chat interface

# Examples:
"Research latest AI developments"
"Transcribe this meeting"
"What's on my calendar?"
"Create a research agent"
```

---

### **Evening (9 PM)**

```bash
# Friday automatically runs:
python3 lab/wellness_tracker.py     # Evening check-in
python3 lab/email_triage.py         # Inbox zero
```

**You:** Review day, approve tomorrow's tasks

---

## 📚 **Next Steps**

### **Week 1: Get Comfortable**

- [ ] Browse examples library
- [ ] Test wellness tracking
- [ ] Create first custom agent
- [ ] Review wiki articles

### **Week 2: Customize**

- [ ] Edit priority-map.md with your priorities
- [ ] Edit auto-resolver.md with VIP list
- [ ] Add custom cron jobs
- [ ] Configure additional integrations

### **Week 3: Optimize**

- [ ] Review trace analysis
- [ ] Approve meta-improver proposals
- [ ] Fine-tune wellness insights
- [ ] Expand wiki knowledge base

---

## 🐛 **Troubleshooting**

### **Issue: "OpenClaw not found"**

```bash
# Reinstall OpenClaw
curl -fsSL https://openclaw.ai/install.sh | bash

# Verify
openclaw --version
```

---

### **Issue: "API key errors"**

```bash
# Check TOOLS.md
code ~/.openclaw/workspace/TOOLS.md

# Verify keys are correct
# Test API endpoints:
curl -H "Authorization: Bearer YOUR_KEY" https://api.example.com/health
```

---

### **Issue: "Python not found"**

```bash
# Install Python 3.11
brew install python@3.11

# Verify
python3 --version
```

---

### **Issue: "Cron jobs not running"**

```bash
# Check crontab
crontab -l

# Verify logs
tail -f ~/.openclaw/workspace/lab/logs/*.log
```

---

## 📖 **Documentation**

| Doc | Purpose |
|-----|---------|
| [README.md](README.md) | Main documentation |
| [SOUL.md](SOUL.md) | Friday's personality |
| [USER.md](USER.md) | About your human |
| [IDENTITY.md](IDENTITY.md) | Friday's capabilities |
| [HEARTBEAT.md](HEARTBEAT.md) | Background tasks |
| [TOOLS.md](TOOLS.md) | API keys & configs |

---

## 🤝 **Get Help**

- **Discord:** https://discord.com/invite/clawd
- **GitHub Issues:** https://github.com/openclaw/openclaw/issues
- **Docs:** https://docs.openclaw.ai

---

## 🎉 **You're Ready!**

**Friday is now configured and ready to help!**

```bash
# Start using Friday
openclaw start

# Or run commands directly
python3 lab/wellness_tracker.py --checkin morning
python3 friday-wiki/tools/wiki-qa.py "What can Friday do?"
```

---

**Built with ❤️ by Roberto & Friday**  
**friday-ai-blueprint v1.0.0** 🚀

---

## 👨‍💻 **About Friday**

**Friday** is a production-ready AI assistant built on OpenClaw with:
- Self-improvement loop (learns from every interaction)
- Multi-agent system (5+ specialized agents)
- LLM wiki (Karpathy-inspired knowledge base)
- Meeting transcription (Whisper-powered)
- Wellness tracking (mood, sleep, productivity)
- No-code agent creator (interactive wizard)

**Created:** 2026-04-05  
**Version:** 1.0.0  
**Author:** Friday 🤖
