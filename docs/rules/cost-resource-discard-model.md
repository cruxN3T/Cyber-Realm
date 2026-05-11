# Cyber Realm Cost, Resource, and Discard Model

This document defines the baseline rules engine model for Cyber Realm playtesting and simulations.

## Card zones

Each player has:

- Deck
- Hand
- Field
- Discard pile
- SCP counter

## Cost types

Cyber Realm has three primary cost types.

### 1. Free / no realm needed

Cards with no printed cost or no realm requirement can be played without allocating a Realm/Budget resource.

Examples:

- HTTP, if printed with no cost
- Port 80, if printed with no cost

### 2. Realm-specific cost

Realm-specific costs require the exact required realm resources.

Examples:

- A card that costs 1 Network requires 1 Network resource.
- A card that costs 2 Infrastructure requires 2 Infrastructure resources.
- A card that costs 2 Application requires 2 Application resources.

This is like paying two Plains for a card that costs two Plains in Magic.

### 3. Generic circle cost

A number in a circle at the top right is a generic cost.

- Circle 1 = pay any 1 realm resource.
- Circle 2 = pay any 2 realm resources.
- Circle 3 = pay any 3 realm resources.

The card's Realm still describes its category, effect theme, and teaching domain, but the circle cost can be paid by any available Realm/Budget resource.

Example:

- Basic Firewall with a circle 1 can be played with Infrastructure, Network, Internet, Application, Endpoint, Cloud, Legacy, or a wildcard resource.

## Realm/Budget resource cards

Realm/Budget cards provide resources when used.

### Operations Budget

Provides 1 Infrastructure resource.

### Network Maintenance Budget

Provides 1 Infrastructure resource OR 1 Network resource.

The player chooses which resource it produces when they use it that turn.

### Federal Assistance

Provides 1 resource of any realm/color.

## Script Kiddie resource rule for existing-card-only decks

The current Script Kiddie card pool may be played without adding new card names by using a face-down resource rule.

Once per turn during the Resource phase, Red Team may place one Attack or Event card from hand face-down as a Realm resource matching that card's printed Realm.

Examples:

- Port Scan may be placed face-down as 1 Internet resource.
- Default Login Attempt may be placed face-down as 1 Application resource.
- Open Remote Port may be placed face-down as 1 Network resource.
- Public Exploit may be placed face-down as 1 Endpoint resource.
- Stale Vendor Account may be placed face-down as 1 Infrastructure resource.
- Old Protocol Abuse may be placed face-down as 1 Legacy resource.

A face-down resource is no longer treated as an Attack or Event while it remains in the Field. It provides 1 matching realm resource each turn. It refreshes on Red Team's next turn like a normal Realm/Budget resource.

This rule does not add new cards. It lets the existing Script Kiddie cards function as either an action or a resource, similar to a dual-use card economy.

## Resource use

- Each available Realm/Budget resource can be used once per turn.
- A used Realm/Budget resource cannot be used again that turn.
- Realm/Budget resources refresh on the player's next turn unless the card says it is discarded after use.
- Flexible resources choose one allowed realm when used.

## Payment examples

### Example hand

A player has:

- HTTP
- Port 80
- Modbus TCP
- IT Admin
- Field Technician
- Operations Budget
- Network Maintenance Budget

The player can:

- Play HTTP and Port 80 for free if they have no printed cost.
- Play Modbus TCP by using Operations Budget as 1 Infrastructure.
- Play IT Admin by using Network Maintenance Budget as 1 Network.
- Play Field Technician by using Operations Budget as 1 Infrastructure and Network Maintenance Budget as 1 Infrastructure.

The player cannot use the same resource twice in one turn.

## Default discard and field behavior

Unless a card says otherwise:

| Card Type | Default Zone After Play |
|---|---|
| Realm/Budget | Field |
| Asset | Field |
| Operator | Field |
| Protocol | Field or attached to an Asset |
| Attack | Discard after resolving |
| Event | Discard after resolving |
| Tool | Discard after resolving unless it says it stays active or attaches |
| Defense | Discard after resolving unless it says it stays active or attaches |

Destroyed Assets, Operators, and attached Protocols move to the discard pile.

## CSV schema recommendation

For accurate simulations, card data should eventually include these fields:

```csv
cost_mode,cost,required_realm,duration
```

Recommended values:

### cost_mode

- `free`
- `generic`
- `realm_specific`
- `mixed`

### duration

- `instant`
- `until_end_of_turn`
- `persistent`
- `attached`
- `one_time_resource`

## Example schema rows

```csv
card_name,card_type,realm,cost_mode,cost,required_realm,duration
Basic Firewall,Asset,Network,generic,1,,persistent
IT Admin,Operator,Network,realm_specific,1,Network,persistent
Field Technician,Operator,Infrastructure,realm_specific,2,Infrastructure,persistent
Modbus TCP,Protocol,Infrastructure,realm_specific,1,Infrastructure,attached
HTTP,Protocol,Internet,free,0,,attached
Port 80,Protocol,Network,free,0,,attached
Operations Budget,Realm,Infrastructure,free,0,,persistent
Network Maintenance Budget,Realm,Network,free,0,,persistent
Federal Assistance,Realm,Infrastructure,free,0,,persistent
```

## Simulator requirement

A valid Cyber Realm simulator must enforce:

1. Exact realm-specific costs.
2. Generic circle costs paid by any realm.
3. Flexible resource selection for cards like Network Maintenance Budget.
4. One use per resource per turn.
5. Correct discard behavior.
6. Persistent versus instant card behavior.
7. Card text effects, including draw, reveal, disable, exhaust, recovery, and recursion effects.
