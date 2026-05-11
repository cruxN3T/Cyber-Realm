# Quickstart: Small Utility vs Script Kiddie

This quickstart is for the first ICS-WATER playtest mode.

## Matchup

- **Blue Team:** Small Utility
- **Red Team:** Script Kiddie
- **Deck size:** 32 cards per side for the first starter test, or use the 40-card existing-card-only deck for expanded balance testing
- **Starting SCP:** 20 per player
- **Starting hand:** 7 cards

## Goal

Reduce the opposing player's SCP to 0, or complete the active Scenario Objective.

For the first test scenario, use **Water Tower Overflow**:

- Red Team wins immediately if Red destroys any Blue Team Asset at any point.
- Red Team also wins the scenario if Water Tower and Gateway are both damaged by the end of turn 6.
- Blue Team wins the scenario if no Blue Team Asset has been destroyed and Water Tower is not damaged by the end of turn 6.

## Setup

1. Blue Team uses `cards.small-utility-blue.csv` and the Blue Team side of the selected deck file.
2. Red Team uses `cards.small-utility-red.csv` and the Red Team side of the selected deck file.
3. Shuffle each deck.
4. Each player draws 7 cards.
5. Blue Team goes first for the first playtest.
6. Both players must maintain a 7-card hand target. Each player draws 1 card at the start of their turn. If a player has more than 7 cards during Cleanup, they must discard down to 7.

## Card zones

Each player has:

- Deck
- Hand
- Field
- Discard pile
- SCP counter

## Turn structure

Each turn has five simple phases:

1. **Draw** — Draw 1 card.
2. **Resource** — Play up to 1 Realm/Budget card, or use the applicable resource rule for the deck.
3. **Deploy** — Play Assets, Operators, Protocols, Tools, Defenses, Events, or Attacks by paying the printed cost.
4. **Conflict** — Resolve attacks, defenses, and card effects.
5. **Cleanup** — Discard down to 7 cards if needed.

## First-turn timing

Blue Team goes first.

- On Blue Team's first turn, Blue may play/place a card, but that card's effect does not activate until Blue Team's second turn unless the card says otherwise.
- Red Team may attack on Red Team's first turn if Red can legally pay the cost and the card text allows the play.
- From turn 2 onward, cards resolve according to their printed text and normal timing.

## Hand size and draw rules

- Each player starts with 7 cards in hand.
- Each player draws 1 card at the start of their turn.
- If a player has more than 7 cards in hand during Cleanup, they must discard down to 7.
- Card text that draws cards still applies. Extra cards are kept until Cleanup, then the player discards down to 7.
- Discard decisions should follow strategy based on the player's current hand, board state, resource needs, and scenario objective.

## Cost and resource rules

Cyber Realm uses Realm/Budget cards like mana sources.

There are three basic cost types:

1. **Free / no realm needed** — Cards with no cost can be played without using a Realm/Budget card.
2. **Realm-specific cost** — If a card costs 2 Application, the player must use 2 Application resources. If it costs 1 Network, the player must use 1 Network resource.
3. **Generic circle cost** — If a card has a number in a circle at the top right, the player may pay that many resources from any realm. A circle 1 costs any 1 resource. A circle 2 costs any 2 resources. A circle 3 costs any 3 resources.

Realm/Budget cards provide resources:

- **Operations Budget** provides 1 Infrastructure resource.
- **Network Maintenance Budget** provides 1 Infrastructure resource OR 1 Network resource.
- **Federal Assistance** provides 1 resource of any realm/color.

Used Realm/Budget resources cannot be used again that turn. They refresh on the player's next turn unless the card says it is discarded after use.

### Existing-card-only Script Kiddie resource rule

For existing-card-only Red Team decks, Red may place one Attack or Event card from hand face-down as a Realm resource matching that card's printed Realm during the Resource phase.

- The face-down card is no longer treated as an Attack or Event while it is in the Field.
- It provides 1 matching realm resource each turn.
- It can be used the turn it is placed unless a scenario says otherwise.
- Red must choose whether a card is more valuable as a resource or as an effect based on the current hand and board state.

### Example hand

If Blue Team draws:

- HTTP
- Port 80
- Modbus TCP
- IT Admin
- Field Technician
- Operations Budget
- Network Maintenance Budget

Then:

- HTTP and Port 80 can be played for free if they have no realm cost.
- Modbus TCP can be played with Operations Budget as 1 Infrastructure.
- IT Admin can be played with Network Maintenance Budget as 1 Network.
- Field Technician can be played by using Operations Budget as 1 Infrastructure and Network Maintenance Budget as 1 Infrastructure.

The player cannot use the same budget resource twice in the same turn.

## Card text priority

Card text matters. If a card's printed rules text conflicts with these basic rules, the card text wins.

Simulation and playtesting should resolve the card text, including:

- Draw effects
- Reveal effects
- Disable effects
- Exhaust effects
- Recovery effects
- Damage modifiers
- Attack restrictions
- Recursion effects
- Hand reveal or discard effects

Strategy should be based on the player's current hand, current Field, revealed information, resource availability, and scenario objective.

## Default discard and field rules

Unless a card says otherwise:

- Realm/Budget cards stay in the Field.
- Assets stay in the Field until destroyed.
- Operators stay in the Field until destroyed, removed, or disabled by a card effect.
- Protocols stay in the Field or attach to an Asset.
- Attacks go to the discard pile after resolving.
- Events go to the discard pile after resolving.
- Tools go to the discard pile after resolving unless the card says it stays active or attaches.
- Defenses go to the discard pile after resolving unless the card says it stays active or attaches.
- Destroyed Assets, Operators, and attached Protocols move to the discard pile.

## Blue Team play pattern

Blue Team should try to:

- Keep critical Assets alive.
- Use Realms to afford Defenses and Tools.
- Protect Water Tower, Chlorination Unit, Gateway, and SCADA Web Interface.
- Use Operators to recover from attacks.
- Use Protocols to reduce repeated damage.

## Red Team play pattern

Red Team should try to:

- Use Recon cards to reveal targets.
- Chain simple attacks into bigger impact.
- Pressure weak protocols like Telnet, HTTP, Port 23, and Port 80.
- Disable Operators before damaging critical Assets.
- Punish missing MFA, segmentation, and patching.
- Destroy any Blue Team Asset when possible, because destroying any Blue Team Asset is an immediate Red Team win condition in this scenario.

## Basic combat rules

- Attack cards target Assets unless the card says otherwise.
- Defense cards can reduce, cancel, or redirect damage.
- If an Asset reaches 0 Defense, it is destroyed and moved to the discard pile.
- Red Team wins immediately if any Blue Team Asset is destroyed in the Water Tower Overflow scenario.
- Some Assets cause SCP loss when destroyed.
- Effects on cards override these basic rules.

## Keywords

### Recon

Reveals cards or information. Recon usually does low damage but sets up stronger attacks.

### Credential Attack

Represents default login attempts, password spraying, or credential reuse. MFA cards usually counter these.

### Remote Access Attack

Represents exposed remote pathways. MFA, firewall rules, and vendor review usually counter these.

### Malware Attack

Targets Endpoint or operational systems. Antivirus and cleanup tools usually counter these.

### Legacy Risk

Cards like Telnet, HTTP, Port 23, Port 80, and Modbus TCP may be useful but make assets easier to attack.

## First playtest questions

After playing, answer:

- Did Blue Team have enough recovery?
- Did Red Team feel threatening without being impossible to stop?
- Were the rules clear on first read?
- Which cards were confusing?
- Which cards felt too strong?
- Which cards felt useless?
- Did the game teach a real water-sector cybersecurity lesson?

## First balance targets

- Game length: 15-25 minutes
- Red Team should create pressure by turn 3
- Blue Team should have at least one comeback moment
- Scenario should matter by turn 5 or 6
- No single card should decide the whole game by itself
