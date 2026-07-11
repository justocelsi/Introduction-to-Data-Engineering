---
name: log-learning
description: Append newly learned concepts, tools, and takeaways to docs/knowledge.html, the course knowledge base. Use when the user finishes a lesson/module/exercise, says "/log-learning", "log this", "document what we learned", or mentions adding to the knowledge base.
---

# Log learning to knowledge base

**PRIVACY GUARDRAIL — this repo is PUBLIC and ALL work details are confidential.** When connecting concepts to the user's real work, NEVER mention: the employer's name, the business domain or what the data is about, internal file/script names, vendor or platform names (including infra providers), architecture, metrics, or ops details. Frame work connections only at the level of transferable skills, in this style: "Ways I applied this at my job as a jr data scientist: built chronological data-extraction pipelines that used LLM enrichment." Capability described, everything identifying omitted. If in doubt, leave it out.

Maintain `docs/knowledge.html` — a single self-contained HTML page that accumulates everything learned during the course. It must always open cleanly in a browser with no external dependencies.

## Steps

1. Read `docs/knowledge.html`.
2. Gather what to log. Sources, in order of preference:
   - What was just done in this conversation (an exercise, a module's videos, a reading)
   - If unclear, ask the user: "What did you cover, and what stood out?"
3. Write the entry in the user's voice of understanding — practical, not textbook. For each entry capture:
   - **Concept(s)** — plain-language explanation, and where it connects to their real work (per the privacy guardrail above: transferable-skill framing only) when a connection genuinely exists
   - **Tools** — any tool/technology learned; add it to the Tools index table (name, what it's for, one-line when-to-use)
   - **Gotchas / decisions** — anything non-obvious worth remembering
   - **Deeper reading** — check the two reference books in `docs/` (local only, gitignored): "Fundamentals of Data Engineering" (Reis & Housley) and "Designing Data-Intensive Applications" (Kleppmann). If a chapter covers the same topic, read the relevant section (use the Read tool with the `pages` parameter on the PDF) and weave 1-2 insights that go BEYOND the course material into the entry, citing book + chapter. Fundamentals maps closely to intro-course topics (lifecycle, ingestion, storage, orchestration); DDIA goes deeper on storage engines, replication, batch/stream processing.
4. Insert the entry:
   - New `<article class="entry">` at the TOP of `<section id="entries">` (newest first), with the date and module name in the header
   - Update the Tools index table (`#tools tbody`) — one row per tool, no duplicates; if a tool reappears, update its row instead
5. When adding the first entry or first tool, delete the matching placeholder (`#entries-empty` / `#tools-empty`).
6. Keep the HTML self-contained: inline CSS only, no CDN links, no JS frameworks.
6. Do not rewrite or summarize old entries — the page is append-only history.
7. ALWAYS also update the Progress table in README.md (add/update the module's row with status and date logged).
8. Commit and push (knowledge.html + README.md together).

## Entry markup

```html
<article class="entry">
  <header><h3>Module N — Title</h3><time>YYYY-MM-DD</time></header>
  <h4>Concepts</h4>
  <p>...</p>
  <h4>Tools</h4>
  <p>...</p>
  <h4>Gotchas &amp; decisions</h4>
  <p>...</p>
</article>
```
