# Partnership OS

Status: MVP v1.0 on synthetic data. Public repository: [github.com/Lucumax/partnership-os](https://github.com/Lucumax/partnership-os).

## What it does

Partnership OS turns an inbound data or product partnership proposal into a structured term sheet, an assumption register, a normalized comparable set, a scenario valuation range (downside, base, upside), a negotiation brief, a human approved decision record and an audit history.

## Why it exists

Comparable deals are often sparse and structures are non standard. Several teams need one analytical view they can challenge.

## How it is built and verified

It is a local first Next.js 16 app in strict TypeScript, with Tailwind, Zod, Vitest and Playwright. A deterministic engine does the valuation math. A specification package in the repo served as the build contract, including acceptance criteria and a build prompt for a coding agent. Live AI is a deliberate boundary. The assistant is a typed interface with a deterministic fixture behind the "AI draft" labels. The live implementation is a stub that throws NOT_IMPLEMENTED, and no page calls it.

## Honest status

The data is synthetic. Six fictional cases appear in portfolio views, and one case is modeled end to end. It runs locally and is not a deployed product.

## What it taught

Write the contract before the code. Keep AI output labelled as a draft and keep the decision with a person.
