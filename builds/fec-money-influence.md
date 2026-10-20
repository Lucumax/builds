# Congressional Funding Brief

Repository name: fec-money-influence. Status: incomplete local draft, pending human review. Private repository.

## What it does

A source linked briefing for a journalist. It compares campaign contributions from selected PACs, current committee roles and published funding requests for five House members. The records share a member. They do not show that a donor benefited or that anyone was influenced, and the product copy has to say so.

## Why it exists

The question is simple: what is documented, and where can a reader verify it?

## How it is built and verified

Python and DuckDB compute from saved inputs, and a static page displays the frozen draft. Acquisition saves immutable, hashed source bodies. A partial failure stays visible and never becomes a zero. The five members were frozen before anyone looked at the money. Dollar totals are withheld until source, completeness, reconciliation and review gates pass. The validate command checks evidence hashes and links, and its publication mode is built to fail while human review and rights gates are open. Adversarial tests and a CI check run on the committed exports.

## Honest status

It is a draft. A machine pass is not human verification, and the repo says the draft must not be called a validated release. A private preview exists. Nothing is published.

## What it taught

Gates that fail on purpose protect a claim better than a confident summary does.
