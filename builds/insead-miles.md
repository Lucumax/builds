# INSEAD Miles

Status: prototype. Not published yet, so there is no link.

## What it does

A points and miles optimizer for INSEAD alumni. The user picks the cards they hold and enters monthly spend by category. The page compares their best card in each category with the best card in its market list and shows the annual gap. It reports annual points or cash back and a net value after perks and fees. It also suggests a card to add. Two modes cover the two goals: transferable points, and plain cash back.

## Why it exists

Card rewards depend on categories and on which cards a person already holds. A spreadsheet answers one profile at a time.

## How it is built

The whole tool is one HTML file with inline JavaScript. The card list, point valuations and spend categories are data inside the file, and I found no network calls in it. The user's numbers stay in the browser.

## Honest status

It is a prototype. The card data and valuations are assumptions that I have to keep current and check, and the page itself asks for reports of discrepancies. I have not verified it against live issuer terms.

## What it taught

A small, single file build can still carry the discipline: keep the data separate from the logic so a wrong number is easy to find and fix.
