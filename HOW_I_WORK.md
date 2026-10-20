# How I work

A one minute read.

## Roles

- **Me:** product owner and final reviewer. I write the spec, the acceptance tests and the release gates, and I approve what ships.
- **Claude Code:** conductor. It plans, splits work and coordinates.
- **Codex and open weight models such as DeepSeek:** builders and independent reviewers.
- **Small checker models:** fact checkers. They check, they do not score.

## Gates

- Every build has a written spec before code.
- Agents build. A different agent then tries to break the work.
- Facts, numbers and citations are checked by deterministic scripts where possible. A model proposes, a check disposes.
- Builder output is scanned before I accept it. In one paper build, a builder agent twice slipped in text I had ruled out, so my process now scans builder output instead of trusting the agent's own report.

## Green is not good

A passing test or a PASS verdict is not the same as a good result. I read the output myself and look for what the gates cannot see. One example from my own work: a sound detector rule looked strong on one test set and did not hold up on independent recordings. I wrote down the test before scoring it and recorded the negative result in the repo.

## What an agent may do alone

- **Alone:** read, draft, build to spec, run checks, propose.
- **With a person:** accept a decision, spend money, publish, change a gate, or act on anything irreversible.

Two builds show the pattern. In the approval layer, an agent can only propose a payment and a human approves the exact terms. In Product Forge, the pipeline only proposes and a human accepts with a token and the exact hash of the card.
