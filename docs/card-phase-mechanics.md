# Card Phase Mechanics

## Design decision

Lifecycle phases should describe a card's **primary training role**, not always a strict action timing rule.

This matters most for Asset cards.

## Assets

Assets can belong to a lifecycle phase, but they should usually be treated as **targets, footholds, or enablers** rather than actions.

Examples:

| Team | Asset | Phase | Why it fits |
|---|---|---|---|
| Blue Team | Water Tower | Reinforce | It is a protected operational asset tied to resilience and scenario survival. |
| Blue Team | Gateway | Detect/Reinforce | It represents a monitored access path and a hardened boundary. |
| Blue Team | SCADA Web Interface | Detect | It can reveal operational visibility but can also become an exposed target. |
| Red Team | Command Channel | Command and Control | It represents attacker control infrastructure. |
| Red Team | Command Communication | Command and Control | It represents attacker communication with a compromised system. |

## Attacks and Defenses

Attack and Defense cards should map more directly to lifecycle actions.

Examples:

- Network Scan = Recon
- Phishing Campaign = Delivery
- Vulnerability Exploit = Exploit
- Pre Built Malware Package = Install
- System Outage = Actions on Objectives
- Port Scanner = Detect
- Port Closure = Respond/Reinforce
- Password Reset = Respond/Recover
- MFA = Reinforce

## Rule of thumb

Use lifecycle phase this way:

- **Attack / Defense / Event cards** = what is happening right now
- **Tool / Operator cards** = capability that supports a phase
- **Protocol cards** = system condition or risk that affects a phase
- **Realm cards** = resource/funding/access that enables a phase
- **Asset cards** = protected target, operational dependency, or attacker foothold connected to a phase

## Card face recommendation

For Assets, the phase symbol should be smaller or treated as a training tag.

For Attack and Defense cards, the phase symbol should be more prominent because those cards represent direct lifecycle actions.

## Current recommendation for Tier 1

Keep phases on Assets for training clarity, but do not teach players that Assets are "played during" that phase.

Say this instead:

> The phase symbol tells you what part of the attack or defense story this card teaches.

This keeps the game educational without making the mechanics confusing.
