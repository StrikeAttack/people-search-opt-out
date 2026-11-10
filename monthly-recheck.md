# Monthly recheck

A removal sticks until the broker ingests a new public record. Do this once a month, on a day you will remember. Use a home connection and a normal browser. FastPeopleSearch and Nuwber often stop a cloud or datacenter address before the page loads.

Copy [`tracking-template.csv`](tracking-template.csv) to a private folder before you type anything. A safe name is `my-tracker.csv`, which this repo ignores. Do not commit the copy. Do not put a real listing URL, record id, street, phone, email, age, or relative in a file that gets pushed.

## Before you search

- [ ] Open your private tracker, not the placeholder file in the repo.
- [ ] List the names to check: current name, and any previous name you have used. Keep that list private.
- [ ] List the cities and phones that would confirm a match. You need them for the match test, not for a search-engine post.
- [ ] Skim [`brokers.md`](brokers.md). If a row is marked Cited or Unconfirmed, expect the form to have moved.

## On each broker

Repeat for every row in the brokers table.

- [ ] Open the public search page from a home browser.
- [ ] Search your name. If the site allows a city, add the city you actually live in, or a city you recently lived in.
- [ ] Open a result only when the name is yours.
- [ ] Apply the match test from the README: name, plus at least two of age, city, street, phone, or relatives. If it fails, set the status to `skipped-not-a-match` and move on.
- [ ] If it passes, copy the listing URL into your private notes only, then open the free opt-out URL from `brokers.md`.
- [ ] Stop if the page asks you to pay, create an account, or upload an ID or a photo.
- [ ] Submit with a spare email. Use a spare phone only when that form requires a phone. Open the email link the same day.
- [ ] Record `submitted` and the date. Come back after the time in the brokers table and record `removed` or `still-listed`.

## The whole pass

- [ ] Search the web for your name plus your city, and for your name plus each broker's name. Open only results that are clearly you.
- [ ] For any row already marked `removed`, search that broker again. If the listing is back, submit a new opt-out and set the status to `returned`.
- [ ] Open <https://radaris.com/>. While it shows the court-order transfer notice, there is nothing to file. If a search box is back, treat it as a new broker and read the privacy page before you type.
- [ ] If you are a California resident and you used DROP, look at your DROP status. DROP does not replace the rows above.
- [ ] Write the pass date at the top of your private tracker.

## Status words

Use these in the `status` column so later months stay easy to scan:

| Status | When to use it |
| --- | --- |
| `not-checked` | No search yet this pass |
| `not-found` | A search showed no listing that passed the match test |
| `skipped-not-a-match` | A similar name was visible and it was not clearly you |
| `submitted` | The free opt-out form was sent, and you opened the email link if there was one |
| `removed` | A later search no longer shows that listing |
| `still-listed` | The wait time has passed and the same listing is still up |
| `returned` | A listing you had removed is back, and you have filed again |
| `blocked` | The opt-out page would not load. Retry from a home connection before calling it blocked |

## What not to store

Store the broker name, the date, the status, and a private reminder such as "current city" or "previous name." Leave the listing URL and the record id out of any file you might commit. Screenshots of a listing belong in the same private place, or nowhere.
