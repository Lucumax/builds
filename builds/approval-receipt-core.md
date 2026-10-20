# An approval layer for AI agents that spend money

Status: early prototype against a mock payment adapter. Private repository. Everything is simulation. Not production ready.

## The pattern

An agent should not hold a blank cheque. The core engine puts five controls between an agent's request and a payment.

1. **Mandate.** It states what the agent may spend, with limits and an expiry.
2. **Policy gate.** A pure function returns allow, escalate to a human, or deny, with a rule id and reason code.
3. **Human approval.** The approval binds to a digest of payee, amount, currency, purpose and mandate, plus a single use nonce. Hard blocks and expiry are rechecked right before execution.
4. **Signed receipt chain.** Every state change appends a record with a canonical JSON form, SHA 256 hash, HMAC signature and sequence number. A verify command names the first broken record. A saved checkpoint detects truncation.
5. **Safe recovery.** If a payment call times out, the state becomes UNKNOWN. The engine asks the provider using the same idempotency key. It retries only when the provider definitively has no record. An unclear answer stays UNKNOWN.

## Why it exists

The hard case is not a refused payment. It is not knowing whether money moved. The free text an agent gives as a reason is treated as untrusted and never reaches the policy checker.

## Built and verified

Python standard library only, with pytest. Version 2.0.0 followed independent model reviews. Prototype apps use the core, and a manifest check confirms a copy is unmodified.

## Not done

No real payment provider, no HTTP API or login, a local advisory file lock, no key rotation and no security review.

## What it taught

Design for the unknown state first.
