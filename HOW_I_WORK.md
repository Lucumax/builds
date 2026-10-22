# How I work

A one minute read.

## The rule

I decide in advance what an agent may do alone and what only a person may approve. Everything else follows from that line.

- **An agent may:** read, draft, build to a spec, run checks and propose.
- **Only a person may:** accept a decision, spend money, publish, change a gate or act on anything irreversible.

## Roles

- **Me:** product owner and final reviewer. I write the spec, the acceptance tests and the release gates, and I approve what ships.
- **Claude Code:** the conductor. It plans, splits the work and coordinates.
- **Codex and open weight models such as DeepSeek:** builders and independent reviewers.
- **Small checker models:** fact checkers. They check, they do not score.

## Gates

- Every build has a written spec before code.
- Agents build. A different agent then tries to break the work.
- Numbers and citations are checked by scripts wherever possible. A model proposes, a check disposes.
- Builder output is scanned before I accept it, because an agent's own report is not evidence.

## A passing check is not a finished review

Before I published the GPU cost model, a separate AI reviewer went through it and found two errors my own checks had passed. I had credited a 35 percent discount to a pricing page that states no percentage, and one cover ratio compared a year five scrap value with debt owed at the end of a one to three year contract. I relabeled the discount as an assumption and fixed the ratio before publishing. I read the output myself because the gates can only catch what they were built to see.
