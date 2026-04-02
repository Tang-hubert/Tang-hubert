# Work-in-Midnight 自動化研究系統

## Definition
An automated research system that runs at 4:00 AM Taiwan time (UTC 20:00), pulling Trello Pending cards, conducting research, and delivering results to Discord.

## Key Components

| Component | Purpose |
|-----------|---------|
| Python Script | `work_in_midnight_research.py` - Core automation |
| Trello API | Board `openclaw-cowork` → Pending List |
| Cron Job | Isolated session, 30-min timeout |
| Discord | Delivery to `#openclaw-work-in-midnight` |

## Relay Mechanism (接力機制)

Critical for long-running research across multiple sessions:

1. Each Phase completion → immediate disk write (append mode)
2. "待續..." (To be continued) marker → next session pickup point
3. `research_progress.md` → central progress tracking
4. Future session flow: read progress → find card `.md` → continue from marker

## Trello Card Flow

```
Pending → on-work (research starts) → complete (research finishes)
```

## Card Categories

- A. GitHub Repo
- B. System Package Audit
- C. Topic Research
- D. Technical Implementation

## Research Report Structure

- Phase 1: 理解問題（核心問題 / 關鍵術語表 / 研究策略）
- Phase 2: 深度研究
- Phase 3: 寫入研究報告（Step 1-4 / 時間線 / 建議方向 / 待續接力章節）
- Phase 4: 更新 `research_progress.md`
- Phase 5: Discord 通知

## Key Learnings

- **Timeout Buffer**: Research tasks need 30+ minutes, not 10 minutes
- **Phase-based Write**: Write after each Phase to prevent context overflow
- **Incremental Append**: Never overwrite existing research, only append

## Related Daily Entries
- [2026-04-02](../daily-learnings/2026/04/2026-04-02.md)
