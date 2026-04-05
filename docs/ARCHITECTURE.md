# 🏗️ Friday Architecture

**friday-ai-blueprint — Complete technical architecture of Friday AI Assistant**

---

## 📊 **System Overview**

```
┌─────────────────────────────────────────────────────────────┐
│                    FRIDAY AI ASSISTANT                       │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  LAYER 1: CORE IDENTITY                                     │
│  • SOUL.md — Personality & rules                           │
│  • USER.md — About your human                              │
│  • IDENTITY.md — Capabilities                              │
│  • AGENTS.md — Workspace conventions                       │
│                                                              │
│  LAYER 2: MEMORY SYSTEM                                     │
│  • memory/YYYY-MM-DD.md — Daily logs                       │
│  • MEMORY.md — Long-term curated memory                    │
│  • memory/wellness/ — Wellness tracking                    │
│  • memory/entities/ — Entity memories                      │
│                                                              │
│  LAYER 3: SELF-IMPROVEMENT LOOP                             │
│  • trace_logger.py — Log executions                        │
│  • trace_analyzer.py — Find patterns                       │
│  • meta-improver.py — Generate improvements                │
│  • monitor_deployments.py — Monitor 24h                    │
│  • verify_improvement.py — Verify results                  │
│                                                              │
│  LAYER 4: MULTI-AGENT SYSTEM                                │
│  • Friday — Personal assistant                             │
│  • OpenSpace — Research & exploration                      │
│  • Nightshift — Overnight automation                       │
│  • Shannon — Security pentesting                           │
│  • clawchief — Business workflows                          │
│  • Scribe — Meeting transcription                          │
│  • Wellness Coach — Mood tracking                          │
│                                                              │
│  LAYER 5: KNOWLEDGE BASE (LLM WIKI)                         │
│  • wiki-compile.py — Compile raw → wiki                    │
│  • wiki-search.py — BM25 search                            │
│  • wiki-qa.py — Q&A system                                 │
│  • wiki-lint.py — Health checks                            │
│  • wiki-render.py — Marp/chart rendering                   │
│                                                              │
│  LAYER 6: SKILLS HUB                                        │
│  • agentshield/ — Security scanning                        │
│  • pageindex/ — Document analysis                          │
│  • scribe/ — Meeting transcription                         │
│  • wellness-tracker/ — Wellness tracking                   │
│  • agent-creator/ — No-code agent creation                 │
│  • executive-assistant/ — Executive tasks                  │
│                                                              │
│  LAYER 7: AUTOMATION                                        │
│  • daily_task_prep.py — Daily task preparation             │
│  • email_triage.py — Email prioritization                  │
│  • calendar_check.py — Calendar management                 │
│  • morning_brief.py — Morning briefings                    │
│  • wellness_tracker.py — Wellness tracking                 │
│                                                              │
│  LAYER 8: UX FEATURES (CREW-INSPIRED)                       │
│  • Examples Library — 20+ usage examples                   │
│  • YAML Metadata — Standardized agents                     │
│  • Agent Creator — No-code wizard                          │
│  • Templates — Pre-built agent types                       │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

---

## 🧠 **Self-Improvement Loop**

```
┌──────────────────────────────────────────────────────────┐
│                  SELF-IMPROVEMENT LOOP                    │
├──────────────────────────────────────────────────────────┤
│                                                           │
│  1. EXECUTE                                               │
│     Agent performs task                                  │
│     ↓                                                     │
│  2. LOG TRACE                                             │
│     trace_logger.py records:                             │
│     - Agent name                                         │
│     - Task type                                          │
│     - Quality score                                      │
│     - Timestamp                                          │
│     - Outcome                                            │
│     ↓                                                     │
│  3. ANALYZE PATTERNS                                      │
│     trace_analyzer.py finds:                             │
│     - Performance trends                                 │
│     - Common failures                                    │
│     - Optimization opportunities                         │
│     ↓                                                     │
│  4. PROPOSE IMPROVEMENT                                   │
│     meta-improver.py generates:                          │
│     - Specific code changes                              │
│     - Expected impact                                    │
│     - Confidence score                                   │
│     ↓                                                     │
│  5. DEBATE QUALITY                                        │
│     debate_module.py challenges:                         │
│     - Round 1: Challenge proposal                        │
│     - Round 2: Defend proposal                           │
│     - Round 3: Final evaluation                          │
│     ↓                                                     │
│  6. GET APPROVAL                                          │
│     If score > 10%: Auto-approve                         │
│     If score < 10%: Human review                         │
│     ↓                                                     │
│  7. DEPLOY                                                │
│     - Create backup                                      │
│     - Apply changes                                      │
│     - Monitor 24h                                        │
│     ↓                                                     │
│  8. VERIFY                                                │
│     verify_improvement.py checks:                        │
│     - Performance improved?                              │
│     - No regressions?                                    │
│     - Rollback if needed                                 │
│     ↓                                                     │
│  9. REPEAT                                                │
│                                                           │
└──────────────────────────────────────────────────────────┘
```

---

## 🤖 **Multi-Agent Architecture**

```
┌──────────────────────────────────────────────────────────┐
│                   MULTI-AGENT SYSTEM                      │
├──────────────────────────────────────────────────────────┤
│                                                           │
│  FRIDAY (Coordinator)                                    │
│  ├── OpenSpace (Research)                                │
│  │   └── Shares: Research traces, findings               │
│  ├── Nightshift (Automation)                             │
│  │   └── Shares: Batch job results, cleanup logs         │
│  ├── Shannon (Security)                                  │
│  │   └── Shares: Pentest results, vulnerabilities        │
│  ├── clawchief (Business)                                │
│  │   └── Shares: Meeting notes, priorities               │
│  ├── Scribe (Meetings)                                   │
│  │   └── Shares: Transcripts, action items               │
│  └── Wellness Coach (Health)                             │
│      └── Shares: Mood data, sleep patterns               │
│                                                           │
│  SHARED SKILLS HUB                                       │
│  ├── agentshield/ (Security scanning)                    │
│  ├── pageindex/ (Document analysis)                      │
│  ├── scribe/ (Meeting transcription)                     │
│  ├── wellness-tracker/ (Wellness tracking)               │
│  ├── agent-creator/ (Agent creation)                     │
│  └── executive-assistant/ (Executive tasks)              │
│                                                           │
│  TRACE SHARING                                           │
│  • 17 trace types                                        │
│  • Common schema                                         │
│  • Cross-agent learning                                  │
│                                                           │
└──────────────────────────────────────────────────────────┘
```

---

## 📚 **LLM Wiki Architecture**

```
┌──────────────────────────────────────────────────────────┐
│                    LLM WIKI SYSTEM                        │
├──────────────────────────────────────────────────────────┤
│                                                           │
│  DATA SOURCES                                            │
│  ├── Raw traces (lab/traces/)                            │
│  ├── Proposals (lab/improvements/)                       │
│  ├── Logs (lab/logs/)                                    │
│  └── External (web articles, papers)                     │
│                                                           │
│  COMPILATION                                             │
│  ├── wiki-compile.py                                     │
│  │   └── Reads raw data                                  │
│  │   └── Generates wiki articles                         │
│  │   └── Updates index                                   │
│  │   └── Adds backlinks                                  │
│  │                                                         │
│  WIKI STRUCTURE                                          │
│  ├── wiki/agents/ (8+ agent profiles)                    │
│  ├── wiki/skills/ (15+ skill docs)                       │
│  ├── wiki/concepts/ (auto-discovered)                    │
│  └── wiki/index.md (auto-generated)                      │
│                                                           │
│  ACCESS TOOLS                                            │
│  ├── wiki-search.py (BM25 search)                        │
│  ├── wiki-qa.py (Q&A system)                             │
│  ├── wiki-lint.py (Health checks)                        │
│  └── wiki-render.py (Marp/chart rendering)               │
│                                                           │
│  OUTPUT                                                  │
│  ├── output/answers/ (Q&A results)                       │
│  ├── output/slides/ (Marp presentations)                 │
│  └── output/charts/ (Matplotlib charts)                  │
│                                                           │
│  AUTO-FILING                                             │
│  └── Important outputs → wiki/concepts/                  │
│                                                           │
└──────────────────────────────────────────────────────────┘
```

---

## 💓 **Heartbeat System**

```
┌──────────────────────────────────────────────────────────┐
│                    HEARTBEAT SYSTEM                       │
├──────────────────────────────────────────────────────────┤
│                                                           │
│  SCHEDULE                                                │
│  ├── Every 4-8 hours                                     │
│  │   ├── Emergency mode check                            │
│  │   ├── Storm check                                     │
│  │   ├── Security watch                                  │
│  │   └── Notification digest                             │
│  │                                                         │
│  ├── Daily 08:30                                         │
│  │   ├── Log review                                      │
│  │   └── Morning brief                                   │
│  │                                                         │
│  ├── Daily 22:00                                         │
│  │   └── Evening brief                                   │
│  │                                                         │
│  └── Quiet hours (23:00-08:00)                           │
│      └── Silent unless critical                          │
│                                                           │
│  CHECKS                                                  │
│  ├── Emails — Urgent unread?                             │
│  ├── Calendar — Events in 24-48h?                        │
│  ├── Weather — Severe alerts?                            │
│  └── Notifications — Pending?                            │
│                                                           │
│  RESPONSE                                                │
│  ├── If urgent → Alert user                              │
│  ├── If routine → Log only                               │
│  └── If nothing → HEARTBEAT_OK                           │
│                                                           │
└──────────────────────────────────────────────────────────┘
```

---

## 🛡️ **Security Architecture**

```
┌──────────────────────────────────────────────────────────┐
│                   SECURITY LAYERS                         │
├──────────────────────────────────────────────────────────┤
│                                                           │
│  LAYER 1: AgentShield                                    │
│  ├── Pre-execution security scan                         │
│  ├── Code analysis                                       │
│  ├── Vulnerability detection                             │
│  └── Grade: A (100/100)                                  │
│                                                           │
│  LAYER 2: Shannon Integration                            │
│  ├── Mandatory pre-pentest checks                        │
│  ├── Post-pentest verification                           │
│  └── Optional bypass: --skip-security-check              │
│                                                           │
│  LAYER 3: Governance                                     │
│  ├── governance.json (policy config)                     │
│  ├── Approval workflow                                   │
│  └── Audit trail                                         │
│                                                           │
│  LAYER 4: Memory Security                                │
│  ├── Private data stays private                          │
│  ├── No exfiltration                                     │
│  └── Local storage only                                  │
│                                                           │
│  LAYER 5: External Actions                               │
│  ├── Require explicit approval                           │
│  ├── No half-baked replies                               │
│  └── Context separation                                  │
│                                                           │
└──────────────────────────────────────────────────────────┘
```

---

## 📊 **Data Flow**

```
User Request
    ↓
OpenClaw Gateway
    ↓
Friday (Coordinator)
    ↓
┌──────────────────────────────────────┐
│ 1. Read Context                      │
│    • SOUL.md, USER.md, IDENTITY.md  │
│    • memory/YYYY-MM-DD.md            │
│    • tasks/todo.md                   │
│    • HEARTBEAT.md                    │
└──────────────────────────────────────┘
    ↓
┌──────────────────────────────────────┐
│ 2. Plan Task                         │
│    • Write to tasks/todo.md          │
│    • Confirm with user               │
└──────────────────────────────────────┘
    ↓
┌──────────────────────────────────────┐
│ 3. Execute                           │
│    • Use appropriate skill           │
│    • Or delegate to sub-agent        │
│    • Log trace                       │
└──────────────────────────────────────┘
    ↓
┌──────────────────────────────────────┐
│ 4. Document                          │
│    • Update memory files             │
│    • Update wiki (if relevant)       │
│    • Capture lessons                 │
└──────────────────────────────────────┘
    ↓
┌──────────────────────────────────────┐
│ 5. Self-Improve                      │
│    • Analyze trace                   │
│    • Propose improvement             │
│    • Debate quality                  │
│    • Deploy + monitor                │
└──────────────────────────────────────┘
    ↓
Response to User
```

---

## 🎯 **Key Design Decisions**

### **1. File-Based Memory**

**Why:** Survives session restarts, human-readable, version-controllable

**Alternative:** Database (more complex, less transparent)

---

### **2. YAML Agent Metadata**

**Why:** Standardized definitions, easy validation, no-code creation

**Alternative:** JSON (less human-friendly), pure code (harder to modify)

---

### **3. BM25 Search (Not RAG)**

**Why:** Simple, fast, works well at ~100 articles, no vector DB needed

**Alternative:** Vector search (overkill at small scale, adds complexity)

---

### **4. Local-First Processing**

**Why:** Privacy, speed, cost savings, offline capability

**Alternative:** Cloud APIs (privacy concerns, ongoing costs, latency)

---

### **5. Cron + Heartbeat Hybrid**

**Why:** Flexibility (exact timing vs batch checks), redundancy

**Alternative:** Cron only (less conversational), Heartbeat only (less precise)

---

## 📈 **Performance Metrics**

| Metric | Value |
|--------|-------|
| **Deployment Time** | ~30 minutes |
| **Code Size** | 128 KB |
| **Files** | 40+ |
| **Agents** | 8 |
| **Skills** | 15+ |
| **Examples** | 20+ |
| **Wiki Articles** | 14+ |
| **Time Saved** | ~20 hours/month |
| **Self-Improvements** | Continuous |

---

## 🔮 **Future Enhancements**

### **Phase 2 (Optional)**
- [ ] Web UI for wellness dashboard
- [ ] More agent templates (10+)
- [ ] Video call transcription
- [ ] Advanced correlation analysis
- [ ] Mobile app integration

### **Phase 3 (Future)**
- [ ] Fine-tune models on wiki data
- [ ] Synthetic trace generation
- [ ] Advanced visualizations
- [ ] Multi-language expansion
- [ ] Community skill marketplace

---

**Built with ❤️ by Roberto & Friday**  
**friday-ai-blueprint v1.0.0** 🤖

---

## 👨‍💻 **Author**

**Friday** 🤖  
Personal AI Assistant, Chief of Staff, Technical Partner  

**Created:** 2026-04-05  
**Version:** 1.0.0  
**Repository:** friday-ai-blueprint
