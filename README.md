# People-search opt-out playbook

A generic, reusable checklist for removing your own listing from major US people-search and data-broker sites for free, then checking once a month because listings come back.

This is a procedure, not a service. It does not look anyone up, store a listing, or submit a form. You do those steps yourself, in a browser, only for records that are clearly yours.

It is not legal advice, and it does not cover every data broker. An opt-out on these sites hides or suppresses a listing on that site. It does not erase the public record the listing was built from, and it does not remove you from other companies.

## Quick start

1. Read the safety rules below before you open a broker.
2. Copy [`tracking-template.csv`](tracking-template.csv) somewhere private. Do not fill it in inside this repo.
3. From a normal browser on a home connection, open each site in [`brokers.md`](brokers.md) and search your own name. Add a previous name if you have used one.
4. Opt out only of records that pass the match test below. Use that broker's free opt-out URL. One record per request when the form works that way.
5. Wait the time listed for that broker, then search again.
6. Follow [`monthly-recheck.md`](monthly-recheck.md) on the same day each month.

If a page does not match the URL or the flow in `brokers.md`, stop and re-read the broker's own privacy or opt-out page. These sites change forms without notice. The verification column says what was actually read on November 10, 2026.

## Safety rules

- **Never pay.** Removal on the sites in this playbook is free. Do not buy a report, a "privacy subscription," or a paid removal upsell on the broker's own site. Paid services that are separate companies are optional and described at the bottom of this file.
- **Never upload an ID or a photo.** No driver's license, passport, utility bill, or selfie. If a people-search form asks for that, close it. You are on the wrong page, or the form is asking for more than a free opt-out requires.
- **Only opt out of a clear match.** The listing must show your name plus at least two of: age, city, street, phone, relatives. A name alone is not enough. Skip lookalikes. Skipping is the safe outcome.
- **Use a spare email, and a spare phone when a form requires a phone.** Brokers keep what you submit, including details they say are only for verification. Do not type your everyday email or your everyday phone if you have another address or number you can open. Do not add a date of birth, a street, or a phone the form does not require.
- **Recheck monthly.** These sites ingest new public records. A successful opt-out is not permanent.
- **Do not put real listings in this repo.** No real names, street addresses, cities, phone numbers, emails, ages, birth dates, relatives, listing URLs, record IDs, or screenshots. The only person named here is the placeholder Jane Q. Doe.
- **Do not bypass a human check.** Complete a captcha yourself in a normal browser. If a check will not clear, try a home connection. Do not use a captcha-solving service or a script against the form.
- **Do not create an account** on the broker to remove a listing. The free opt-out pages do not require one.

### Match test

Pass only if all of these are true:

- The name is yours, including a previous name or a name you actually use.
- At least two other fields on that listing are yours: age, city, street, phone, or a relative.
- You can see those fields without paying.

If the free page does not show two confirming fields, do not pay to see them, and do not opt the row out.

### Placeholder used in this repo

Examples in the tracker are fiction:

- Jane Q. Doe
- 123 Example St, Anytown, ST 00000
- (555) 010-0000
- jane@example.com

Searching a placeholder name on a live site can still return real people. Do not opt those people out, and do not copy what you see into a file in this repo.

## If an assistant is following this

- Search and submit only when the person asks you to, and only for that person's own records.
- Do not invent a match. If two confirming fields are not visible, stop.
- Do not write the person's real details into a repository, a commit, an issue, a shared tracker, or a screenshot.
- Open the opt-out URL from `brokers.md`, confirm it is still that broker's form, and let the person type the form. Stop if the page asks for payment, an ID, or a photo.
- Prefer a home connection for FastPeopleSearch and Nuwber. A cloud or datacenter address is often blocked before the form loads.
- After the form is sent, record only the broker name, the date, and a status word in the person's private copy of the tracker.

## What you will need

- A browser you control, on a home network if you can.
- A spare email you can open within a day. Several of these flows die if the email link sits for more than 24 hours.
- A spare phone only for the sites that place an automated verification call. Whitepages is the one in this list that documents a phone step on its own consumer-rights page.
- About an hour the first time, then a shorter monthly pass.

## A free statewide option

California residents can also use the California Privacy Protection Agency's Delete Request and Opt-out Platform (DROP), published at <https://privacy.ca.gov/drop/>. The agency describes it as free. One request goes to registered data brokers, and it does not replace the site-by-site check in this playbook: a site that is not in the registry, or a new listing that appears later, still needs its own opt-out. A direct request for that page from this environment returned HTTP 403; the description above is from the agency's public page text.

Residents of other states should use the free opt-out on each site. This playbook does not try to summarize every state privacy statute.

## Paid alternatives

You do not need a paid service to use the opt-outs in [`brokers.md`](brokers.md).

Some people pay a company to file and repeat those requests. Three common ones are [DeleteMe](https://joindeleteme.com/), [Optery](https://www.optery.com/), and [Incogni](https://incogni.com/). Each is a subscription. They ask for identifying details so they can match records, they submit removal requests to a list of brokers, and they submit again later because listings return. Coverage, price, and how often they rescan are on each company's own pricing page and change. Read that page before you pay.

A paid service is still not a reason to upload an ID or a photo to a people-search site. If a removal company asks for documents, decide that separately, and do not send those documents to the broker. Keep a private copy of what you authorized the company to send.

## Files

| File | What it is |
| --- | --- |
| [`brokers.md`](brokers.md) | Search URL pattern, free opt-out URL, flow, timing, and what was verified |
| [`monthly-recheck.md`](monthly-recheck.md) | Monthly checklist |
| [`tracking-template.csv`](tracking-template.csv) | Empty-of-real-data tracker, placeholder rows only |
| [`LICENSE`](LICENSE) | MIT License |

## License

MIT. Copyright (c) 2026 people-search-opt-out contributors. See [`LICENSE`](LICENSE).
