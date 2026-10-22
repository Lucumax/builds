# Builds

**Walter Guevara**, Washington, D.C. Finance and strategy operator who builds AI assisted systems.

This repository holds write ups of seven of them. It contains no source code. The code lives in private repositories, with one public exception linked below.

Contact: walter.guevara.us@gmail.com | [linkedin.com/in/walterguevara](https://linkedin.com/in/walterguevara)

## How I work

I work as a small team of one: product owner, analyst, builder and reviewer, directing AI agents. Claude Code is the conductor. Codex, open weight models such as DeepSeek, and small checker models act as builders, reviewers and fact checkers. I write the spec, the acceptance tests and the release gates. Agents build, and other agents try to break the work. Nothing ships without my approval, and a passing test is not the same as a good result, so I read the output myself. The hard design question in every build is what an agent may do alone and what must stay with a person.

More detail on one page: [HOW_I_WORK.md](HOW_I_WORK.md).

Scale: most of this work lives in private repositories, which is why this page describes them instead of linking code.

## Featured builds

| # | Build | What it is | Status |
|---|---|---|---|
| 1 | [Priming Risk Scanner](builds/priming-risk-scanner.md) | Finds covenant and structural risk in credit agreements, with verified citations, SEC EDGAR and FRED data | v0.2.0, private, local tool |
| 2 | [PetOS / PetSignal](builds/pet-os.md) | Your pet texts you, but only from facts a record can support | Prototype, private |
| 3 | [Approval layer for AI agents](builds/approval-receipt-core.md) | Mandate, policy gate, human approval and signed receipts for agents that spend money | Early prototype, all simulation |
| 4 | [Partnership OS](builds/partnership-os.md) | Valuation and negotiation brief when comparables are sparse | MVP on synthetic data, [public repo](https://github.com/Lucumax/partnership-os) |
| 5 | [Congressional Funding Brief](builds/fec-money-influence.md) | Source linked briefing on campaign money and funding requests, with completeness gates | Incomplete draft, private |
| 6 | [Product Forge](builds/product-forge.md) | File first product operating system with an MCP server | v0.3 beta, private, one user |
| 7 | [INSEAD Miles](builds/insead-miles.md) | Points and miles optimizer for alumni | Prototype, not published |

## What this is and is not

> These are internal systems built mostly for my own use. I am the primary and generally the only user. Prototypes and simulations are labelled as such. None of them is a deployed enterprise product or a client system.
