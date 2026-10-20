# Priming Risk Scanner

Status: v0.2.0. Private repository, runs locally.

## What it does

The scanner reads a credit agreement and flags covenant interactions that let some lenders move ahead of others, such as uptier and dropdown transactions. It also pulls figures from SEC 10-K and 10-Q filings and compares them with the financial covenant thresholds it extracts. The output is a nine section risk memo in Markdown, HTML and JSON, with an evidence table and a list of questions for the analyst. It is framed for insurance, pension, private credit and special situations teams.

## Why it exists

A structural read of a credit agreement takes an analyst days. The risk sits in how sections interact, so a quick summary misses it.

## How it is built and verified

The model is the smallest part. A parser splits the filing into sections and an indexer finds defined terms. A resolver follows definition chains through three levels. A router then sends only the relevant sections to the model for each risk topic, instead of the whole document. Every quotation the model returns is checked against the source text in three tiers: exact, normalized, then fuzzy. Unverified citations are gated. Live inputs come from SEC EDGAR and FRED (SOFR, the 10 year Treasury and a credit spread). A gatekeeper step writes a JSON audit record. Per the README, the repository has more than 120 tests.

## Honest status

The README lists its own limits: text native PDFs only, one document at a time, heuristic definition extraction, regex based financial extraction, and no legal advice. Findings need review by counsel.

## What it taught

Routing and citation checks decide whether a memo can be trusted. The model call is the easy step.
