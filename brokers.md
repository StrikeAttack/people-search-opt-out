# Brokers

Free opt-out facts for the people-search sites this playbook covers. Read [`README.md`](README.md) before you use the table. Search URL patterns use `{first}`, `{last}`, `{city}`, and `{st}` so the repo does not point at a real lookup. Substitute your own name only in a private browser.

Verification date: November 10, 2026.

| Mark | Meaning |
| --- | --- |
| Read | The opt-out or notice page was retrieved and its text was read that day |
| Cited | A public page names this URL, and the form itself did not load here (usually HTTP 403) |
| Unconfirmed | Guides name this URL, and it did not load here. Open it and confirm before you type anything |

Field observations, not tied to any person:

- TruePeopleSearch and USPhonebook use an email-link flow plus a captcha, and the wait is about 72 hours. The USPhonebook form read for this playbook says "complete the captcha" and "allow 3 days," without naming the captcha vendor. Public readings of the TruePeopleSearch form describe the same email-link shape and a 3-day wait, and guides have called the widget hCaptcha or reCAPTCHA at different times. Complete whichever widget is on the page.
- FastPeopleSearch and Nuwber often Cloudflare-block cloud or datacenter IP addresses. Use a home connection. A curl from this environment received Cloudflare HTTP 403 for Nuwber's opt-out URL and for some FastPeopleSearch URLs, while a separate retrieval still returned FastPeopleSearch's opt-out text.

## Summary

| Broker | Public search URL pattern | Official free opt-out URL | Flow | Typical removal time | Check |
| --- | --- | --- | --- | --- | --- |
| TruePeopleSearch | `https://www.truepeoplesearch.com/results?name={first}-{last}` | `https://www.truepeoplesearch.com/removal` | Email link, captcha | About 72 hours | Cited |
| FastPeopleSearch | `https://www.fastpeoplesearch.com/name/{first}-{last}` | `https://www.fastpeoplesearch.com/optout` | Email link, captcha | 3 days | Read |
| USPhonebook | `https://www.usphonebook.com/{first}-{last}` | `https://www.usphonebook.com/removal` | Email link, captcha | 3 days | Read |
| ThatsThem | `https://thatsthem.com/name/{First}-{Last}` | `https://thatsthem.com/optout` | Web form, confirmation email | About 72 hours | Cited |
| Nuwber | `https://nuwber.com/` then a profile URL | `https://nuwber.com/removal/link` | Listing URL, email link, captcha | Up to 48 hours | Cited |
| Radaris | `https://radaris.com/` (notice only, as of this check) | None on the domain right now | Nothing to submit | n/a | Read |
| Spokeo | `https://www.spokeo.com/{First}-{Last}` | `https://www.spokeo.com/optout` | Listing URL, email link, captcha | 24–48 hours | Read |
| Whitepages | `https://www.whitepages.com/name/{First}-{Last}/{City}-{ST}/{id}` | `https://www.whitepages.com/suppression-requests` | Listing URL, then a phone call in the automated tool | Up to 15 days for a CCPA opt-out; listing-tool clock not stated | Read |
| BeenVerified | `https://www.beenverified.com/` people search | `https://www.beenverified.com/svc/optout/search/optouts` | Search, pick the record, email link | About 24 hours after the confirmation email | Cited |
| PeopleFinders | `https://www.peoplefinders.com/` | `https://www.peoplefinders.com/opt-out` | Email link and captcha, according to guides | About 3 days, according to guides | Unconfirmed |
| Intelius / PeopleConnect | Home pages of Intelius, TruthFinder, Instant Checkmate, USSearch | `https://suppression.peopleconnect.us/` | Email link, then identity fields. Steps not readable here | Not stated on a page we could read | Title only |
| MyLife | `https://www.mylife.com/` | `https://www.mylife.com/privacyrequest` | Web form with a human check | No day count on the form that was publicly described | Unconfirmed |

Details and the limits of each check are below. When a note says the form was not read, trust the live page over this file.

## TruePeopleSearch

- **Search.** Start at <https://www.truepeoplesearch.com/>. A commonly published results shape is `https://www.truepeoplesearch.com/results?name={first}-{last}`. Profile addresses are commonly under `/find/person/{id}`. Those result pages were not loaded for this check.
- **Opt-out.** <https://www.truepeoplesearch.com/removal>
- **Flow.** A public reading of that page on October 31, 2026 describes four steps: enter your name and email and complete the captcha; open the email link within 24 hours; fill the form so it matches the record; wait for a confirmation. The same reading quotes "Please allow 3 days for your record to be fully removed from our site."
- **Time.** About 72 hours.
- **Check.** Cited. A direct request on November 10, 2026 returned HTTP 403 from Cloudflare, so the live form was not re-read. Confirm the page before you submit. Do not call a support number from an old blog post unless it is printed on the page you are looking at.

## FastPeopleSearch

- **Search.** Start at <https://www.fastpeoplesearch.com/>. A commonly published name-results shape is `https://www.fastpeoplesearch.com/name/{first}-{last}`, and with a place `https://www.fastpeoplesearch.com/name/{first}-{last}_{city}-{st}`. Those result pages were not loaded for this check.
- **Opt-out.** <https://www.fastpeoplesearch.com/optout> and <https://www.fastpeoplesearch.com/removal>. Both addresses returned the same instructions when retrieved on November 10, 2026.
- **Flow.** The page says to enter your email and name, complete the captcha, and open the email link. The link must be used within 24 hours. The next form should match the record you want removed. Then a confirmation page and a confirmation email.
- **Time.** The page says to allow 3 days.
- **Check.** Read. The opt-out text was retrieved. A plain curl of `/removal` from this environment still returned Cloudflare HTTP 403, which matches the field note: if the human check will not clear, switch to a home connection and a normal browser. The page also refers to a phone option in third-party write-ups of the privacy notice. Use a number only if it is printed on the page in front of you, and prefer the form.

## USPhonebook

- **Search.** Start at <https://www.usphonebook.com/>. A commonly published name-results shape is `https://www.usphonebook.com/{first}-{last}`. That results page was not loaded for this check.
- **Opt-out.** <https://www.usphonebook.com/removal>. Older write-ups mention `/opt-out`; the form that loaded is `/removal`.
- **Flow.** The page says to enter your email and name, complete the captcha, and open the email link within 24 hours. The next form should match the record. The page says information from the request is used only to process the request. Treat that as their statement, and still use a spare email.
- **Time.** The page says to allow 3 days.
- **Check.** Read, November 10, 2026. A public copy of their do-not-sell page also points at an opt-out form and mentions a phone option. The form above is the one to use.

## ThatsThem

- **Search.** Start at <https://thatsthem.com/>. A commonly published name-results shape is `https://thatsthem.com/name/{First}-{Last}`. That results page was not loaded for this check.
- **Opt-out.** <https://thatsthem.com/optout>
- **Flow.** Spokeo's privacy policy (revision dated October 20, 2026, in the copy returned with search) sends ThatsThem listings to this URL and says the Spokeo opt-out does not cover ThatsThem. Indexed text of the ThatsThem page describes an opt-out form, a confirmation email, and processing in about 72 hours. Guides add required name, address, email, and phone fields plus a human check. Those field lists were not re-read on the live form.
- **Time.** About 72 hours, from the indexed page text.
- **Check.** Cited. A direct request on November 10, 2026 returned HTTP 403. Open the URL and follow the form that is actually there. Opt out of Spokeo separately.

## Nuwber

- **Search.** Start at <https://nuwber.com/> and search by name and state, which is what the opt-out instructions say to do. Profile addresses on the opt-out page use the shape `https://nuwber.com/person/{id}`. Do not copy a real `{id}` into this repo.
- **Opt-out.** <https://nuwber.com/removal/link>. Nuwber's privacy policy names that URL. Guides say the shorter `/removal` path is a 404. `/removal` was not requested for this check.
- **Flow.** Indexed text of the opt-out page says to paste the profile URL, enter an email, pass a reCAPTCHA, and follow the email link. The same text says the address is used to verify the request.
- **Time.** The indexed FAQ says the removal may take up to 48 hours, and that a removed profile URL can come back as HTTP 410.
- **Check.** Cited. The privacy-policy sentence and the opt-out page text were retrieved through search. A direct request for the opt-out URL on November 10, 2026 returned HTTP 403 from Cloudflare. Use a home connection.

## Radaris

- **Search.** <https://radaris.com/> did not offer a search box on November 10, 2026. It showed a court-order notice. Older profiles used a shape like `https://radaris.com/p/{First}/{Last}/`. Do not expect that path to open a listing while the notice is up.
- **Opt-out.** There is no opt-out form on the domain while that notice is what the site serves. <https://radaris.com/page/privacy> showed the same notice. Older guides mention `https://radaris.com/control/privacy`; that path was not requested separately.
- **What the notice says.** The domain radaris.com has been transferred to Atlas Data Privacy Corporation and is no longer under the control of its former operators. The notice titles the case Atlas Data Privacy Corporation, et al. v. Radaris.com, et al., in the Superior Court of New Jersey, and says a final judgment by default was entered on August 27, 2026, against Radaris.com, Rehold.com, and Trustoria.com. It describes the judgment as tied to New Jersey's Daniel's Law. This playbook did not read the court docket, so it does not say whether an appeal is pending. The notice is not a deletion receipt for every person who once had a Radaris page.
- **Flow.** Nothing to submit. If a web search engine still shows an old Radaris snippet, use that search engine's own outdated-result tool. Listings on other brokers are unaffected.
- **Time.** Not applicable while the notice is up. Look again on the monthly pass, in case the site returns.
- **Check.** Read, November 10, 2026, on the home page and on `/page/privacy`.

## Spokeo

- **Search.** Start at <https://www.spokeo.com/>. A commonly published name-results shape is `https://www.spokeo.com/{First}-{Last}`. Spokeo's help center describes a single listing URL that also includes a state, a city, and an id. Write that shape as `https://www.spokeo.com/{First}-{Last}/{ST}/{City}/{id}`. Each listing URL is opted out on its own.
- **Opt-out.** <https://www.spokeo.com/optout>
- **Flow.** The opt-out page, read November 10, 2026, says to enter the profile URL. It says opting out does not remove the data from the original source, that each listing URL is separate, and that a listing can reappear. Spokeo's help article "How do I remove my information from Spokeo?" (retrieved the same day) adds: paste the URL, enter an email used to verify the removal, complete the "I'm not a robot" check, and click the link in the confirmation email. The privacy policy says this tool does not cover ThatsThem.
- **Time.** The opt-out page says the request should be processed in 24–48 hours.
- **Check.** Read.

## Whitepages

- **Search.** Start at <https://www.whitepages.com/>. The consumer-rights page says to enter your name and city/state in People Search, open the matching listing, and copy that page's URL. Their own example uses a real city name; do not copy it. The shape is `https://www.whitepages.com/name/{First}-{Last}/{City}-{ST}/{id}`.
- **Opt-out.** <https://www.whitepages.com/suppression-requests>
- **Flow.** The suppression page is "Step 1 of 5" and asks for the profile URL. The consumer-rights page (last updated June 22, 2026, read November 10, 2026) says the automated tool both removes the listing and opts out of sale or sharing, and that the tool asks for a phone number used only to finish the request. Guides describe that step as an automated call and a short code shown on screen. If you do not want to give a phone number, the same page offers a customer-service form or the email address printed on that page, and it says a reply can take up to two business days. You do not have to create an account or buy anything.
- **Time.** The consumer-rights page says CCPA opt-out requests may take up to 15 days and are often faster. It does not state a separate clock for the automated listing tool. Search-engine copies of a removed page can linger after Whitepages has dropped it.
- **Check.** Read, for both the suppression page and the consumer-rights page.

## BeenVerified

- **Search.** Start at <https://www.beenverified.com/> and use the people search. A commonly published profile shape is `https://www.beenverified.com/people/{first}-{last}/`. That profile page was not loaded for this check.
- **Opt-out.** <https://www.beenverified.com/svc/optout/search/optouts> for the people-search opt-out. A second path, <https://www.beenverified.com/svc/optout/search/comprehensive_optouts>, is the privacy-rights form named in public readings of the privacy policy and in California registry write-ups. Use the people-search opt-out for a listing. On November 10, 2026, `https://www.beenverified.com/app/optout/search` returned HTTP 301 to `https://www.beenverified.com/svc/optout/search/`.
- **Flow.** Indexed text of the people-search opt-out page says to search, select the record, and confirm an email link. It says a further email confirms the opt-out, and that people-search results update on the next server refresh, in most cases within 24 hours. It also says the email is used to verify the request and that you do not need a membership.
- **Time.** About 24 hours after the confirmation email, according to that indexed page. Not re-read live.
- **Check.** Cited. Both form URLs returned HTTP 403 from Cloudflare on November 10, 2026. The redirect away from the older `/app/optout/search` path was observed directly.

## PeopleFinders

- **Search.** Start at <https://www.peoplefinders.com/>. A stable public results-URL pattern was not confirmed, because the site did not load here.
- **Opt-out.** Guides, including write-ups checked against the company's own pages in 2026, name <https://www.peoplefinders.com/opt-out>. The company's privacy notice (last updated date shown as January 1, 2025, in the copy returned with search) says to use "our Opt-Out Form" or a phone number printed in that notice. The notice text that was retrieved did not include the form's URL.
- **Flow.** Those guides describe an email link, a captcha, a record-suppression form, and about 3 days. That flow was not read on the live form for this playbook.
- **Time.** About 3 days, according to the guides. Unconfirmed here.
- **Check.** Unconfirmed. On November 10, 2026, `/opt-out`, `/optout`, and `/do-not-sell` all returned HTTP 403 from Cloudflare. Open `https://www.peoplefinders.com/opt-out` from a home connection. If it is not the company's form, use the opt-out link in the privacy notice footer instead of a third-party walkthrough.

## Intelius / PeopleConnect

PeopleConnect is the operator behind Intelius, TruthFinder, Instant Checkmate, and USSearch. One suppression request is described publicly as covering name-search background reports on those four sites. Confirm that sentence on the live page. Do not assume it covers every other brand in the corporate family. Public descriptions say Classmates.com is separate; that sentence was not on a page we could read.

- **Search.** Start at the home page of each site you want to check:
  - <https://www.intelius.com/>
  - <https://www.truthfinder.com/>
  - <https://www.instantcheckmate.com/>
  - <https://www.ussearch.com/>
- **Opt-out.** <https://suppression.peopleconnect.us/>
- **Brand paths guides tell you to open,** which are supposed to land on that same suppression center:
  - `https://www.intelius.com/opt-out`
  - `https://www.truthfinder.com/opt-out/`
  - `https://www.instantcheckmate.com/opt-out/`
  - `https://www.ussearch.com/opt-out/`
- **Flow.** The suppression center is a JavaScript application. On November 10, 2026 it returned HTTP 200 and the title "PeopleConnect - Suppression Center," and the static HTML contained no form fields. Public descriptions of the tool say you enter an email, open a link, then confirm identity details such as your name and a birth date plus a phone or email. Those steps were not visible here. There is a separate privacy-center path on the brand sites for account data; a listing suppression and an account-privacy request are not the same thing.
- **Time.** Not stated on a page we could read. Search each of the four sites after you submit.
- **Check.** Title only for the suppression center. The four brand `/opt-out` URLs returned HTTP 403 from Cloudflare, so the redirects were not reconfirmed on November 10, 2026. A public reading on October 17, 2026 reported that all four redirected to `suppression.peopleconnect.us`.

## MyLife

- **Search.** Start at <https://www.mylife.com/>. Copy a profile URL only if you are sure the profile is yours, and keep it in your private notes.
- **Opt-out.** <https://www.mylife.com/privacyrequest>
- **Flow.** A public reading of that form on October 31, 2026 describes the heading "DELETION AND OPT OUT OF SALE OF PERSONAL INFORMATION" and required fields for state, first and last name, city or postal code, email, birth year, and a human check. Middle initial, a previous name, and the profile URL were optional in that reading. The form said a matching profile listing would be removed. Give the birth year only because that form requires it to pick the right record, and use a spare email.
- **Time.** That reading found no number of days on the form, only a reference to legally required time frames. Recheck on the monthly pass rather than assuming a short clock.
- **Check.** Unconfirmed on November 10, 2026. A direct request returned HTTP 403 from Cloudflare, and another fetch returned HTTP 500. Confirm the form is still MyLife's before you submit. The company's help text also points at a privacy-request form.

## After you submit

- One listing per submission when the form is built that way. A second name, a previous address, or a second phone often means a second request.
- Clearing the broker's page does not clear a search-engine snippet on the same day. Give the search engine time, then use its own outdated-result tool if the broker page is already gone.
- Write the date and the status in your private copy of the tracker. Do not save the listing page.
