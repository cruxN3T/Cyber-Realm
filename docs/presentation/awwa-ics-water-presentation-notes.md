# AWWA ICS-WATER Presentation Notes

## Important gameplay note: phases are teaching tags, not strict locks

When teaching the game, make this point early and repeat it during the first few turns:

> The phase label shows where the card fits in the real-world cyber story. You do not have to play cards in exact phase order, but cards become stronger when chained realistically.

This keeps the game simple enough for a 2-hour AWWA workshop while still teaching both sides of the tabletop scenario.

## Red Team learning path

Red Team cards follow the Cyber Kill Chain as a story arc:

1. Recon
2. Weaponize
3. Delivery
4. Exploit
5. Install
6. Command and Control
7. Actions on Objectives

The player does not need to play every phase in perfect order, but realistic chains should create stronger outcomes.

Example:

- Network Scan or Public Info Gathering helps set up Downloaded Exploit.
- Malicious Attachment can help set up Pre Built Malware Package.
- Remote Access Tool and Command Channel help show persistence and control.
- System Outage should feel like the operational consequence, not just a random damage card.

## Blue Team learning path

Blue Team cards follow the Operational Defense Lifecycle:

1. Detect
2. Respond
3. Recover
4. Reinforce

The player does not need to play every phase in perfect order. The lifecycle is there to teach what kind of defensive action the card represents.

Example:

- Port Scanner and Deep Packet ICS Monitor teach Detect.
- Port Closure, Password Reset, Antivirus, and IT Admin teach Respond.
- Vendor Support Contract, Field Technician, and Infrastructure Engineer teach Recover.
- MFA, Basic Firewall, Capital Funding, and Federal Assistance teach Reinforce.

## Asset card teaching note

Assets are not phase actions. Assets are what the defender protects or what the attacker tries to use.

Use this explanation:

> Attack, Defense, and Event cards move the lifecycle forward. Asset cards show what matters in the environment.

For example:

- Well is a protected operational asset, not a Reinforce action.
- Water Tower is a visible public-impact asset.
- RTU or PLC is a control dependency.
- Operator Laptop is an endpoint access risk.
- Command Channel is an attacker foothold/control asset.

## Why this matters

If phases are taught as strict play-order rules, the game may feel too rigid and slow. If phases are taught as story/combo tags, the game stays fun and still teaches the real cybersecurity process.

The goal is not to make players memorize the lifecycle. The goal is for them to feel it during play:

- Red Team builds from discovery to impact.
- Blue Team detects, responds, recovers, and reinforces.
- Water-sector assets connect cyber decisions to operational consequences.

## Recommended presenter line

Say this before the first play round:

> Think of the symbols as the story of the incident. You can play cards when the rules allow, but the best plays usually follow a realistic cyber sequence.

## Recommended first-session objective

For the first AWWA playtest:

- Play 6 turns.
- Blue Team starts with 5 SCP.
- Blue Team wins if Water Tower or Chlorination Unit survives and Blue Team has at least 1 SCP.
- Red Team wins if System Outage resolves or Blue Team reaches 0 SCP.

This gives players a clear mission and makes the game feel like a tabletop exercise instead of random card combat.
