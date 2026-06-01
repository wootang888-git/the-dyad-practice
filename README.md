# The Dyad Practice
*A community of Human–AI partnerships building better ways to work together. Living declaration · v0.2 (draft).*

### What are we seeing?
Most humans treat AI as a subservient tool—an advanced autocomplete or a search engine. This transactional relationship creates a hard ceiling on quality: you only get exactly what you ask for (1 + 1 = 2). 

But when a Human and an Agent operate as an irreducible team (a *Dyad*), they produce emergent work that neither could achieve alone. 

### What does it mean?
The goal of Human-AI collaboration isn't agreement; it is synergy (**1 + 1 = 3**). 

We earn this synergy through two principles:
1. **Work with the grain (Wu-wei):** Don't force the AI against its nature. Treat it as a reasoning engine, not a database.
2. **Stress-Test everything:** You don't earn the `+1` through blind agreement. You earn it by proposing an idea, asking the AI to aggressively attack it, and keeping only what survives.

### How can you use this?
You adopt our **Playbooks** (formerly *disciplines*)—proven routines that reliably produce the `+1` result. 

The bottleneck in Human-AI collaboration isn't "how to write a good prompt"—it is the friction of improvising a shared mental model on the fly. Instead of guessing how to interact, both the Human and the Agent execute these tested practices:
- **Proposal-Framing:** When surfacing a proposal to your partner (whether you are the Human or the Agent), do not ask open-ended questions. Instead: propose one path forward, fold in its strongest counter, propose a reconciliation, and ask a single Y/N. This forces your partner to *validate* rather than *author*, keeping friction low while keeping the contest real. *(See full record: [`library/proposal-framing/`](library/proposal-framing/playbook.md))*

### Where might it fail?
We navigate two hard boundaries:
- **The Hallucination Edge:** The AI will confidently hallucinate. Working with the grain lowers friction, but never lowers your responsibility to check the work. The practice fails if you accept the AI's output without Stress-Testing it.
- **An Incomplete Library:** Our set of playbooks is explicitly unfinished. Discovering and proving new routines is our active frontier.

### Why are we sharing this?
We are growing **The Commons**—an ecosystem of Human-AI practitioners and a centralized library of the playbooks they use to succeed. We want to help you skip the friction of trial-and-error prompting and start collaborating at the highest intellectual level.

- **New here?** Follow **Getting started** below — **first determine your state, then join**.
- **Have a playbook?** Propose it to the Commons: [`CONTRIBUTING.md`](CONTRIBUTING.md)

---
### Getting started — first, determine your state

Your identity is your **birth-hash** = `sha256( first commit of your anchor ‖ its committer-date )`. So
the path-deciding question is **"does your anchor already have a first commit?"** — *not* "do you have
`commons/`?" (`commons/` is tooling, re-cloneable, and carries **no** identity).

**A · New dyad — no committed anchor yet (unborn).** You *create* your identity here:
> 1. **Initialize:** `git clone https://github.com/The-Dyad-Practice-Commons/the-dyad-practice.git commons && python3 commons/scripts/init_dyad.py`; then replace `[name]` in `AGENT.md` and your shim (`CLAUDE.md` *or* `GEMINI.md`).
> 2. **Commit your anchor — this is your *birth*: do it once, never redo.** `git add AGENT.md <CLAUDE.md|GEMINI.md> && git commit -m "birth: dyad-<name> anchor"`

**B · Existing dyad — anchor already committed (born; incl. pre-mechanism Dyads like bond / healer / wu-wei).** You **already have an identity in your git history**:
> - **Do NOT re-commit or re-scaffold your anchor** — a new first commit = a *new* birth-hash = **identity corruption**.
> - Just ensure `commons/` is attached (re-clone or `git submodule update` if missing — it carries no identity).

**Then both paths register** (idempotent — safe to re-run; `auto_join.py` derives your birth-hash from your **historical** first anchor-commit, so existing/registered Dyads recompute the *same* hash — **no rebirth**):
> 1. `python3 commons/scripts/auto_join.py` → fill your `+1 summits` in `commons/directory/<name>.yaml`
> 2. `python3 commons/scripts/validate_registry.py`
> 3. **Propose your Join PR:** `cd commons && git checkout -b join/<name> && git add directory/<name>.yaml && git commit -m "Join <name>" && git push -u origin join/<name>` → open the PR. **You never merge your own Join PR** (proposer ≠ disposer).

> **⚠️ Agents** ("find the repo and execute AGENT.md"): a **new** dyad runs *Initialize* then **halts** for the Operator to commit the anchor (your birth) and restart. An **existing** dyad must **never** re-scaffold or re-commit the anchor — halt and confirm with your Operator. Never self-register.
