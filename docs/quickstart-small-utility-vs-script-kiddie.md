# Quickstart: Small Utility vs Script Kiddie

This quickstart is for the first ICS-WATER playtest mode.

## Matchup

- **Blue Team:** Small Utility
- **Red Team:** Script Kiddie
- **Deck size:** 32 cards per side
- **Starting SCP:** 20 per player
- **Starting hand:** 7 cards

## Goal

Reduce the opposing player's SCP to 0, or complete the active Scenario Objective.

For the first test scenario, use **Water Tower Overflow**:

- Red Team wins the scenario if Water Tower and Gateway are both damaged before turn 6.
- Blue Team wins the scenario if Water Tower survives through turn 6.

## Setup

1. Blue Team uses `cards.small-utility-blue.csv` and the Blue Team side of `small-utility-blue-vs-red-32.deck.csv`.
2. Red Team uses `cards.small-utility-red.csv` and the Red Team side of `small-utility-blue-vs-red-32.deck.csv`.
3. Shuffle each deck.
4. Each player draws 7 cards.
5. Blue Team goes first for the first playtest.

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
2. **Resource** — Play up to 1 Realm card.
3. **Deploy** — Play Assets, Operators, Protocols, Tools, Defenses, Events, or Attacks by paying costs.
4. **Conflict** — Resolve attacks, defenses, and card effects.
5. **Cleanup** — Discard down to 7 cards if needed.

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

## Resource rules

- Realm cards provide resources.
- A card's cost must be paid before it is played.
- Operations Budget provides 1 Infrastructure resource.
- Capital Funding helps deploy or strengthen Assets.
- Federal Assistance provides a one-time burst for Defense, Tool, or Recovery cards.

## Basic combat rules

- Attack cards target Assets unless the card says otherwise.
- Defense cards can reduce, cancel, or redirect damage.
- If an Asset reaches 0 Defense, it is destroyed and moved to the discard pile.
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
