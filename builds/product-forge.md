# Product Forge

Status: v0.3 beta. Private repository with CI.

## What it does

Product Forge is a file first, AI assisted product operating system. It turns messy product context into evidence backed briefs, prioritized backlogs and work packets for execution. It uses Markdown, JSON, schemas, prompts and deterministic validation scripts. An MCP server exposes read routes to agents. It has no write tools by design.

## Why it exists

Most product work fails before engineering starts, through weak framing and no memory of past decisions.

## How it is built and verified

Artifacts are validated against JSON schemas, with negative tests that must fail. The repo's demo shows the rules. A claim labelled as a confirmed public fact is derived as unrecorded if its sources cannot be shown to be independent, so the verdict comes from the sources and not from the label. The pipeline only proposes a Decision Card. A person accepts it with a token and the card's exact hash. A missing token is refused, a stale hash is refused, and a second acceptance is refused. Decisions go to a tamper evident ledger.

## Honest status

The README lists its limits. It has one user so far, the author. The reviewer name is self asserted. The accept gate is weaker than it sounds, and the repo tracks that. File stores have no cross process locking. A ten route dashboard was built but never committed, and the repo records that it is gone.

## What it taught

Derive the verdict. Do not let the author declare it.
