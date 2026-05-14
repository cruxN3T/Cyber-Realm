# Cyber Realm: ICS-WATER Edition

This edition models a tabletop matchup of **Medium Organization vs. Hacktivist** in the water sector.

The Hacktivist deck should feel disruptive, noisy, opportunistic, and message-driven. It should pressure availability, public trust, operator confidence, and weak remote access. It should not feel like a disciplined APT campaign with long-term stealth, firmware tradecraft, or bespoke ICS malware unless those cards are explicitly marked as advanced scenario variants.

## Matchup

- **Defender:** Medium Organization
- **Attacker:** Hacktivist
- **Primary defender concern:** keep water operations stable while handling limited staff, limited budget, and public pressure.
- **Primary attacker goal:** disrupt HMI/operator workflows, cause visible operational confusion, or force emergency response.

## Hacktivist deck design rule

Keep Hacktivist cards in these themes:

1. Public-facing pressure: DDoS, fake login pages, typosquatting, phishing, credential harvesting.
2. Opportunistic access: exposed RDP, unsecured remote access, reused credentials, firewall mistakes.
3. Noisy operational disruption: DDoS on HMI, system reset, valve malfunction trigger, circuit breaker shutdown.
4. Basic command-and-control: lightweight C2 or IRC-style command coordination.

Do **not** add these to the baseline Hacktivist deck:

- Malicious Firmware Loader
- PLC Injector
- Custom ICS malware
- Long-term stealth backdoors
- Log tampering as a stealth objective
- Nation-state/APT operators
- Destructive actions that imply permanent equipment damage

Those belong in an APT, ransomware, or advanced scenario expansion, not the default Hacktivist deck.

## Chain philosophy

Most Hacktivist cards should not win alone. They should become dangerous when chained:

- Recon or public weakness -> credential attack -> remote access -> network position -> ICS action
- Botnet setup -> DDoS tool -> DDoS on HMI
- Firewall misconfiguration -> RDP -> external access -> network position

## Files

- `cards/hacktivist-cards.yaml` contains the uploaded Hacktivist card definitions and recommended game text.
- `chains/hacktivist-chains.md` defines required and optional card chains.
- `balance/remove-from-hacktivist.md` lists cards that should be removed from the Hacktivist deck or moved to another expansion.
