# 05. Tooling playbook

Things I learned by running these tools every day. Useful to anyone building outbound on the same stack.

## Sourcing and enrichment

- Sourcing people inside Apollo gave about three times the verified-contact rate of finding names in ZoomInfo and matching them into Apollo afterwards.
- Lusha uses its own fixed list of industries. Free-text industry terms return nothing, so search with its taxonomy.
- Get the employer right before a Lusha lookup. Sometimes a person can only be found under their previous employer.
- Apollo's organisation keyword filter combines several terms with AND. Ask for several industries at once and you get zero results. One industry per query works every time.
- Apollo's waterfall enrichment finishes on the server in 3 to 10 minutes. Check the same request again and the result usually arrives on the second or third try.

## Managing sequences in Apollo

- A contact already enrolled cannot have its sending mailbox changed in place. Remove the contact and enrol again with the right mailbox.
- Deactivating a sequence is done in the Apollo interface. Reactivating can be done by approval.
- Apollo's campaign stats count unique contacts reached, not total messages. Keep both figures.
- Use one naming prefix for every sequence. A single search then brings up the whole set.

## Deliverability rules

- SPF, DKIM and DMARC set on the sending domain, with DMARC at quarantine.
- No more than 50 sends a day from one mailbox until it has ramped.
- Four steps per sequence, under 110 words, each opened on a real signal.
- Verify catch-all addresses before sending.
- Targets I work to: reply rate of 5% or better, bounce under 3%.
- Cold outreach never goes through the CRM's marketing email.

Result on this engagement: 0.8% bounce across 1,311 sends.

## The stack

| Tool | Job |
|---|---|
| Apollo.io (Professional) | Sequences, people sourcing, waterfall enrichment |
| HubSpot | CRM of record |
| ZoomInfo | Extra people sourcing |
| Lusha | Small companies, under 50 staff |
| LinkedIn Sales Navigator | Account research and personal outreach |
| Clay (free tier) | Enrichment workflows |
| Wappalyzer | What technology a prospect's site runs on |
| ZeroBounce | Email verification |
| Zapier | Connecting Apollo, HubSpot, Gmail and site forms |
| Google Workspace | Mailboxes, Sheets tracker, calendar |

## What I chose to leave out

Fully autonomous AI SDR tools, visitor-identification tools, and bought lookalike sending domains. The engine stays research-led, with a person behind every email, and sends only from domains the company already owns.
