# events-aggregator-it

A published events feed: a list of IT conferences, community days, hackathons and online events in Europe,
checked against the organisers' official pages, as a web page and a calendar feed.

- Web page: https://georgii-web.github.io/events-aggregator-it/
- Calendar feed: https://georgii-web.github.io/events-aggregator-it/events.ics

## How to use

**Browse:** open the web page. Each event shows date, description, place with its Maps rating, hours, price, size
and status. The tag buttons filter the list (for example only PHP or only AWS events).

**Add one event to your calendar:** click "Add" in the Calendar column. It opens Google Calendar with the event
filled in; check it and save.

**Subscribe to all events:** add the calendar feed URL once, and new or changed events show up by themselves.
- Google Calendar: Other calendars → **+** → From URL → paste the feed URL → Add calendar.
- Apple Calendar: File → New Calendar Subscription → paste the feed URL.
- Outlook: Add calendar → Subscribe from web → paste the feed URL.

Calendar apps refresh subscribed feeds on their own schedule (Google: every few hours), so updates can take a while.

## Status of an event

- `ok (official)`: date and details confirmed on the organizer's, venue's or ticket seller's page.
- `unconfirmed (<site>)`: seen only on an event aggregator; check the event link before going.
- `sold out`, `few tickets`, `postponed`, `cancelled`, `no dates yet`: as announced by the organizer.

Facts are as of the "Checked" date on the page; always confirm on the event link before you go.

## How it is made

The site files (`index.html`, `event.html`, `events.ics`, `e/`) are generated, committed and pushed by
[events-aggregator](https://github.com/GeorgII-web/events-aggregator), an agent skill with scripts that searches,
verifies and stores the events. Every push to `main` runs the workflow `.github/workflows/pages.yml`, which deploys
them to GitHub Pages. Do not edit them here; changes are overwritten by the next update.
To build a feed for your own region and taste, clone events-aggregator and follow its README.
