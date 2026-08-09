# raw/ — source documents

**Immutable.** The agent reads from here and never modifies anything.

This is your source of truth. Meeting transcripts, notes, articles, reports, emails — whatever
you're accumulating knowledge from.

```
raw/
├── _inbox/       ← drop new sources here, then say "ingest this"
├── transcripts/  ← meeting recordings, calls
└── notes/        ← handwritten notes, summaries, forwarded email
```

---

## Why immutable matters

Two reasons, and the second is the one people miss:

1. **Provenance.** Every claim in the wiki traces back to a source you can re-read. If the wiki
   says something surprising, you can check whether it's a real finding or a bad inference.
2. **Re-ingestion.** As the wiki gets richer, re-reading an old source often surfaces things you
   missed the first time — because now you have somewhere to connect them to. That only works if
   the source is untouched.

---

## What's here

Six seeded sources spanning June to August 2026, plus one waiting in `_inbox/`.

| Date | Source | Account |
|---|---|---|
| 2026-06-02 | Renewal kickoff notes | Northwind |
| 2026-06-19 | Migration go-live call | Northwind |
| 2026-07-08 | Capacity planning session | Tailspin |
| 2026-07-16 | Data team workshop | Relecloud |
| 2026-07-28 | Quarterly business review | Northwind |
| 2026-08-04 | Infrastructure sync | Tailspin |
| **2026-08-07** | **CFO pre-brief — in `_inbox/`** | **Northwind** |

All fictional.
