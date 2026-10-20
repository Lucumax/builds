# PetOS / PetSignal

Status: prototype. Private repository. The working brand is not cleared. The master spec (version 1.0) is marked proposed and gated.

## The idea

Your pet texts you. An owner adds a dog's photo and name and either enters a real event or uploads a short sound clip. The app writes a short message in the pet's voice, built only from facts the record supports. Each statement carries a label: Observed, Owner told us, Possible or Just for fun.

## How it is built

An immutable event ledger stores each event with its source and consent scope. The language model narrates. Measurable signals and owner statements supply the facts. A deterministic validator builds an allowlist of facts for each message, and a checker removes claims outside it. When the detector is unsure, the app says so: "Sound detected", "Not enough evidence" or "Needs your confirmation", never a made up percentage.

## What it refuses to do

The spec lists these as no go by default: literal pet speech translation, medical diagnosis, continuous home surveillance, scraping public video, automatic unsupervised posting, and invented performance numbers.

## What exists

The repository holds the spec, a browser sound check, a local Python engine that records experiment runs and checks pre registered criteria, a local analysis lab and a benchmark.

## Honest status

One experiment tested a detector rule on independent dog recordings. The criteria were written and dated before any of that audio was scored. The rule did not hold up, and the repo records it as not demonstrated, exploratory, with the labels not yet listened to.

## What it taught

A written no go list sharpens a product. A negative result recorded honestly is still a result.
