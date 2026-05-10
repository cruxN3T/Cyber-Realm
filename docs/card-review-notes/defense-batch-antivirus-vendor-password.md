# Defense Batch Review: Antivirus, Vendor Support Contract, Password Reset

## Review date

Current Tier 1 ICS-WATER Small Org defense-card review.

## Global rule

Only Asset and Operator cards should have attack or defense values.

Defense, Tool, Protocol, Realm, and Event cards should not have attack/defense values unless a future advanced rule explicitly says otherwise.

## Antivirus

Current prototype text:

> Remove one Malware or Remote Access Tool effect from an Endpoint Asset or reduce Malware damage by 2.

Current prototype phase:

> Reinforce

### Issue

The text reads like an immediate cleanup/removal effect, which is more Recover or Respond than Reinforce.

### Best choice

Use one of these two patterns:

#### Option A: Keep Reinforce as a standing defense control

Card type: Defense
Realm: Endpoint
Phase: Reinforce

Text:

> Attach to one Endpoint Asset. The first time Malware or Remote Access Tool would damage that Asset each turn, reduce that damage by 2.

This is the best fit if Antivirus is meant to be installed ahead of time.

#### Option B: Keep the current removal text but change phase

Card type: Tool
Realm: Endpoint
Phase: Recover

Text:

> Remove one Malware or Remote Access Tool effect from an Endpoint Asset, or reduce Malware damage by 2.

This is the best fit if Antivirus is meant to be a one-time cleanup action.

### Recommendation

For Tier 1 training, use Option A:

> Defense — Endpoint / Reinforce

This teaches baseline endpoint protection better.

## Vendor Support Contract

Current prototype text:

> Restore 2 Defense to one damaged Infrastructure Asset. If Gateway is active, draw 1 card.

Current prototype phase:

> Recover

### Review

This works well. It teaches that vendor support helps recovery, but the Gateway condition reminds players that vendor access needs controlled connectivity.

### Recommended tweak

The card type line should not say Defense — Water unless Water is being used as a special edition tag. For the realm system, this should be:

> Defense — Infrastructure

Phase should stay:

> Recover

## Password Reset

Current prototype text:

> Cancel one Credential Attack or restore 2 Defense to one Operator or Endpoint Asset.

Current prototype phase:

> Recover

### Review

This works. It is understandable and useful during play.

### Optional phase label

Recover is fine. If you want to show dual use, Respond/Recover is also accurate because it can cancel a live Credential Attack.

For simplicity in the AWWA training deck, keep:

> Recover

## Final recommendations

- Antivirus: Defense — Endpoint / Reinforce, with standing attached-control wording.
- Vendor Support Contract: Defense — Infrastructure / Recover.
- Password Reset: Defense — Endpoint / Recover.
