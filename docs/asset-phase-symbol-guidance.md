# Asset Phase Symbol Guidance

## Recommendation

Asset cards should generally **not** use the same prominent lifecycle phase symbol treatment as active Attack, Defense, or Event cards.

Assets are usually the protected environment, operational target, dependency, or attacker foothold. They are not usually the action being taken in the lifecycle.

## Well example

A **Well** card should not be presented as if the well itself is a Reinforce action.

Better treatment:

- Card Category: Asset
- Realm: Infrastructure
- Color: Green
- Primary role: Critical operational asset
- Lifecycle tag: Optional secondary training tag, not a main phase symbol

## Recommended card-face layout

For Asset cards:

- Show the Realm symbol/color prominently.
- Show the Asset category clearly.
- Use the lifecycle symbol only as a small secondary training tag if needed.
- Do not make the lifecycle symbol look like the card is an action phase card.

For Attack, Defense, and Event cards:

- Show the lifecycle symbol more prominently because these cards represent actions in the attack or defense chain.

## Practical Tier 1 guidance

For Blue Team operational assets such as Well, Water Tower, Pump Station, Chlorination Unit, RTU or PLC, Gateway, Operator Laptop, Basic Firewall, and SCADA Web Interface:

- Keep the Asset category and Realm color as the main identifiers.
- Use lifecycle phase only as a backend spreadsheet field or small training icon.
- In the master spreadsheet, use `Operational Asset` or `Protected Asset` if the lifecycle label feels confusing.

## Teaching line

> Assets are what the defender protects or what the attacker tries to use. Attack, Defense, and Event cards are what move the lifecycle forward.
