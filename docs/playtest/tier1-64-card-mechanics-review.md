# ICS-WATER Tier 1: 64-Card Mechanics Review

## Review result

The Small Org Defense deck and Script Kiddie Attack deck make sense as a first AWWA tabletop prototype, but the cards need one rules framing decision to avoid confusion:

**Lifecycle symbols are training tags and combo tags, not strict play-order requirements.**

This keeps the game playable in a 2-hour workshop while still teaching the Cyber Kill Chain and Operational Defense Lifecycle.

## Recommended teaching rule

At the start of the game, tell players:

> The phase label shows where the card fits in the real-world story. You do not have to play cards in exact phase order, but cards become stronger when you chain them in a realistic order.

## Attack chain behavior

The Red Team deck should feel like this:

1. Recon: Network Scan / Public Info Gathering
2. Delivery: Phishing Campaign / Malicious Link / Malicious Attachment
3. Exploit: Vulnerability Exploit / Credential Attack / Password Spray
4. Install: Pre Built Malware Package / Remote Access Tool
5. Command and Control: Command Communication / Command Channel / Backup Command Channel
6. Actions on Objectives: System Outage

This is realistic and playable. Red Team has several ways to pressure Blue Team but still needs setup before System Outage.

## Defense lifecycle behavior

The Blue Team deck should feel like this:

1. Detect: Port Scanner / Deep Packet ICS Monitor / SCADA Web Interface visibility
2. Respond: Port Closure / Password Reset / Antivirus / IT Admin
3. Recover: Vendor Support Contract / Field Technician / Infrastructure Engineer
4. Reinforce: MFA / Basic Firewall / Capital Funding / Federal Assistance / Protocol hardening choices

This is a good tabletop learning flow because players see that defense is not only blocking attacks. They detect, contain, recover, and improve.

## Biggest mechanics issue found

Some defensive cards referenced broad terms like `Malware`, `Remote Access Attack`, or `Command card`, while the card names use specific public-safe titles.

For the first prototype, use exact card names or exact card categories whenever possible.

Good example:

- Bad: Remove one Malware effect.
- Better: Remove Pre Built Malware Package or Remote Access Tool from an Endpoint Asset.

Good example:

- Bad: Cancel one Remote Access Attack.
- Better: Reduce damage from Credential Attack or Password Spray. If Remote Access Tool is attached, detach it.

## Card-by-card review notes

### Blue Team: Small Org Defense

| Card | Review | Recommendation |
|---|---|---|
| Well | Works. Good economy + operational impact. | Keep. Use Asset role, not phase action. |
| Water Tower | Works as a scenario objective. | Keep. This gives Blue Team something visible to protect. |
| Pump Station | Works, but moving defense may confuse beginners. | Keep for prototype; explain as rerouting/operational resilience. |
| Chlorination Unit | Works and is strong educationally. | Keep. Great water-sector relevance. |
| RTU or PLC | Works. Good dependency card. | Keep. Pair with Modbus Protocol. |
| Gateway | Works. Good remote access boundary card. | Keep. Counters Internet pressure. |
| Operator Laptop | Works. Good endpoint target. | Keep. Important because many Red cards target it. |
| Basic Firewall | Works but could slow Red Team too much if played early. | Keep at cost 2. Fair. |
| SCADA Web Interface | Works but it currently helps Red if revealed. | Keep. It teaches exposed management interface risk. |
| Password Reset | Works. | Keep. Strong against Credential Attack. |
| MFA | Works, but wording should match exact attacks. | Update to mention Credential Attack and Password Spray. |
| Vendor Support Contract | Works. | Keep. Good recovery teaching. |
| Port Closure | Works. | Keep. Good response/reinforce card. |
| Port Scanner | Works. | Keep. Gives Blue active detection. |
| Deep Packet ICS Monitor | Works. Strong but fair at dual-resource cost. | Keep at 2 cost: 1 Network + 1 Infrastructure. |
| Antivirus | Works, but wording should match exact Red cards. | Update to mention Pre Built Malware Package and Remote Access Tool. |
| Modbus Protocol | Works but is intentionally double-edged. | Keep. This is educational and creates risk tradeoff. |
| Port 23 | Works as legacy exposure. | Keep. It should feel risky, not purely helpful. |
| Remote Terminal Protocol | Works as legacy risk. | Keep. |
| Port 80 | Works. | Keep. Good exposure lesson. |
| Plain Web Protocol | Works as a tradeoff. | Keep. |
| IT Admin | Works. | Keep. Good Network response operator. |
| Field Technician | Works. | Keep. Strong AWWA relevance. |
| Infrastructure Engineer | Works, but may be strong with multiple Protocol cards. | Keep at cost 3. |
| Operations Budget | Works. | Keep. Core resource. |
| Capital Funding | Works. | Keep. Good upgrade/reinforce resource. |
| Federal Assistance | Works. | Keep as burst resource. |

### Red Team: Script Kiddie Attack

| Card | Review | Recommendation |
|---|---|---|
| Network Scan | Works. Good Recon opener. | Keep. |
| Public Info Gathering | Works. | Keep. It teaches public exposure without trademark/tool issues. |
| Downloaded Exploit | Works, but should reward Recon setup. | Keep current +1 if Recon was played. |
| Pre Built Malware Package | Works, but should be clearly removable by Antivirus. | Keep with exact counter wording. |
| Phishing Campaign | Works. | Keep. Good human-factor card. |
| Malicious Link | Works. | Keep. Good delivery card. |
| Malicious Attachment | Works. | Keep. Combos into malware. |
| Vulnerability Exploit | Works. | Keep. Strong but countered by Port Closure. |
| Credential Attack | Works. | Keep. Countered by MFA/Password Reset. |
| Password Spray | Works. | Keep. Good low-sophistication attack. |
| Remote Access Tool | Works, but should attach only after damage. | Keep. This prevents it from being too strong early. |
| Command Communication | Works, but it is more of an attacker foothold than normal asset. | Keep. Deep Packet ICS Monitor should counter it. |
| Command Channel | Works. | Keep. Good cost-reduction engine. |
| Backup Command Channel | Works. | Keep. Nice persistence mechanic. |
| System Outage | Works as finisher. | Keep condition: only after 2 damaged Blue assets. |
| Operations Budget | Works. | Keep. |
| Network Position | Works. | Keep. Good C2/foothold resource. |
| External Access | Works. | Keep. Helps Recon/Delivery. |
| App Access | Works. | Keep. Helps Exploit. |

## Gameplay balance check

### Why Red Team can win

Red Team has enough pressure to damage assets through multiple routes:

- Network Scan / Public Info Gathering into Downloaded Exploit
- Phishing Campaign into Malicious Link or Malicious Attachment
- Credential Attack / Password Spray against weak identity controls
- Remote Access Tool after damage
- Command Channel to reduce future attack costs
- System Outage as a late-game objective

### Why Blue Team can win

Blue Team has enough tools to survive if players learn the lifecycle:

- Port Scanner and Deep Packet ICS Monitor find or remove threats
- Port Closure reduces exposure
- MFA and Password Reset blunt identity attacks
- Antivirus answers malware/remote access
- Vendor Support, Field Technician, and Infrastructure Engineer restore critical assets
- Basic Firewall and Capital Funding improve resilience

## Recommended simple playtest objective

Use this for the first 2-hour AWWA game:

- Play 6 turns.
- Blue Team wins if Water Tower or Chlorination Unit survives and Blue Team has at least 1 SCP.
- Red Team wins if System Outage resolves or Blue Team reaches 0 SCP.

## Recommended SCP starting values

For Tier 1 prototype:

- Blue Team starts with 5 SCP.
- Red Team does not track SCP.
- Blue Team loses SCP when critical assets are destroyed or System Outage resolves.

This makes the game easier to explain than tracking life totals for both sides.

## Recommended turn structure

Use a simple turn structure for the workshop:

1. Draw 1 card.
2. Gain resources from active Realm/Resource cards.
3. Play up to 1 Asset or Operator.
4. Play any number of cards you can afford.
5. Resolve damage, recovery, and destroyed cards.
6. Teach the phase: say what lifecycle step the card represented.

## Final verdict

The game does make sense when played. The strongest design is that Red Team cards naturally chain toward operational impact while Blue Team cards naturally teach detect, respond, recover, and reinforce.

The first prototype should avoid heavy phase-locking. Use phases as learning tags and combo language. That will make the game more fun and easier for AWWA participants to understand in a 2-hour window.
