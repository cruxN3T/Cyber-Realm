# Remove or Restrict from Baseline Hacktivist Deck

The Hacktivist deck should be disruptive, public, noisy, and opportunistic. These cards should not be included in the default Hacktivist deck unless they are moved into a special advanced scenario.

## Remove from baseline Hacktivist

### Malicious Firmware Loader

**Reason:** This implies specialized ICS firmware knowledge and high-risk persistent device manipulation. This fits APT, insider, or advanced ransomware better than Hacktivist.

**Move to:** APT deck or Advanced ICS Malware scenario.

### PLC Injector

**Reason:** Direct PLC payload injection is too advanced and too destructive for baseline Hacktivist. It also overlaps with PLC Hijacker and makes the Hacktivist deck too strong.

**Move to:** APT deck, ransomware deck, or red-team training scenario.

### Persistence via RAT

**Reason:** Long-term persistence changes the deck identity from hacktivist disruption to stealthy intrusion. Hacktivists can use basic C2, but not durable stealth persistence by default.

**Move to:** Black Hat, ransomware, or APT deck.

### Backdoor

**Reason:** Backdoor persistence is a stealth/long-term access mechanic. Baseline Hacktivist should use short-lived access and noisy disruption.

**Move to:** Black Hat or APT deck.

### Log Tampering

**Reason:** Log tampering is stealth behavior. Hacktivist gameplay should be visible and pressure-based, not stealth-first.

**Move to:** APT deck, insider deck, or advanced attacker expansion.

### Maintain ICS Access

**Reason:** Maintaining ICS access over time is too advanced for baseline Hacktivist and makes defender recovery too difficult.

**Move to:** APT deck or advanced scenario.

## Restrict, but can stay

### PLC Hijacker

**Status:** Conditional include.

**Restriction:** Keep as rare/legendary or scenario-limited. It must require Network Position, Unsecured Remote Access, or Rogue Workstation before it can act.

### Valve Malfunction Trigger

**Status:** Include with restrictions.

**Restriction:** Must require PLC Hijacker, Unsecured Remote Access, or Network Position. Remove the old double-effect rule.

### Circuit Breaker Shutdown

**Status:** Include with restrictions.

**Restriction:** Temporary halt only. One turn. No permanent outage or equipment destruction.

### System Reset

**Status:** Include with restrictions.

**Restriction:** Defender-only flavor is better, but it can be used as Hacktivist impact only if attacker already has Remote Access, RDP, or Network Position.

## Cards that strongly fit Hacktivist

- Website Defacement
- DDoS Pirate
- DDoS on HMI
- HOIC
- HULK
- LOIC
- DDoS Botnet Setup
- Phishing Campaign
- Social Engineer
- Fake Login Page
- Credential Harvesting
- Typosquatting
- Firewall Misconfiguration
- RDP
- Unsecured Remote Access
- External Access
- Network Position
- C2 Communication
- IRC Command Hijack
