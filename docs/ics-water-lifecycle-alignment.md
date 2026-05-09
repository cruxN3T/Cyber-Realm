# ICS-WATER Lifecycle Alignment

ICS-WATER intentionally maps Red Team cards to the Cyber Kill Chain and Blue Team cards to the Operational Defense Lifecycle.

The physical card designs may use lifecycle symbols/icons instead of printed lifecycle words. That is preferred because it keeps the card face clean while still making the tabletop training structure visible.

## Red Team: Cyber Kill Chain

Red Team attacker cards should map to one or more of these stages:

1. Recon
2. Weaponize
3. Delivery
4. Exploit
5. Install
6. Command and Control
7. Actions on Objectives

## Blue Team: Operational Defense Lifecycle

Blue Team defender cards should map to one or more of these stages:

1. Detect
2. Respond
3. Recover
4. Reinforce

## Symbol rule

Cards should use lifecycle symbols consistently.

- Red Team symbols represent the Cyber Kill Chain stage.
- Blue Team symbols represent the Operational Defense Lifecycle stage.
- The public card database may describe lifecycle stages in text, but art prompts, Canva files, and production details stay outside the public repository.

## Design rule

Each card should have a gameplay purpose and a training purpose.

A good card should answer:

- What stage of the attack or defense lifecycle does this represent?
- What real-world lesson does the player learn?
- Does the mechanic make the player feel that lesson during play?

## Small Utility vs Script Kiddie alignment

### Red Team examples

| Card | Category | Lifecycle stage |
|---|---|---|
| Internet Exposure Search | Attack | Recon |
| Port Scan | Attack | Recon |
| Default Login Attempt | Attack | Exploit |
| Password Spray | Attack | Delivery / Exploit |
| Phishing the Operator | Attack | Delivery |
| Public Exploit | Attack | Weaponize / Exploit |
| Noisy Malware Drop | Attack | Install |
| Misconfigured Remote Access | Attack | Exploit / Command and Control |
| Flat Network Pivot | Attack | Command and Control / Actions on Objectives |
| Old Protocol Abuse | Attack | Exploit / Actions on Objectives |
| Simple Defacement | Attack | Actions on Objectives |

### Blue Team examples

| Card | Category | Lifecycle stage |
|---|---|---|
| Port Scanner | Tool | Detect |
| Deep Packet ICS Monitor | Tool | Detect |
| Basic Firewall | Asset | Reinforce |
| Port Closure | Defense | Respond / Reinforce |
| Basic MFA | Defense | Reinforce |
| Password Reset | Defense | Respond / Recover |
| Vendor Support Contract | Defense | Recover |
| Antivirus | Tool | Respond / Recover |
| Field Technician | Operator | Recover |
| Infrastructure Engineer | Operator | Recover / Reinforce |
| Operations Budget | Realm | Reinforce |
| Capital Funding | Realm | Reinforce |
| Federal Assistance | Realm | Recover / Reinforce |

## Current coverage

The first prototype has strong Recon, Exploit, Response, Recovery, and Reinforcement coverage.

It still needs deliberate playtest attention for:

- Weaponize
- Delivery
- Install
- Command and Control
- Actions on Objectives
- Detect
- Reinforce

## Next design step

Add lifecycle_stage as a column to future card files or maintain a lifecycle mapping file for each deck.

This keeps the game useful for tabletop exercises and makes it easier to explain to water-sector and security audiences without crowding the card face.
