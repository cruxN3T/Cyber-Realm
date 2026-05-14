# Hacktivist Chains: Medium Organization vs Hacktivist

These chains define what should connect together in the ICS-WATER Hacktivist deck. The goal is to make the attacker disruptive but not overpowered.

## Core Chain 1: Phishing to Remote Access

```text
Phishing Campaign
  -> Credential Harvesting / Fake Login Page / Social Engineer
  -> RDP or Unsecured Remote Access
  -> External Access
  -> Network Position
```

**Purpose:** gives Hacktivist a realistic path from public/user targeting into limited internal access.

**Allowed finishers:**

- Website Defacement
- DDoS on HMI
- System Reset
- Valve Malfunction Trigger

## Core Chain 2: DDoS Pressure

```text
DDoS Botnet Setup
  -> LOIC / HOIC / HULK
  -> DDoS on HMI
```

**Purpose:** creates noisy availability impact without requiring deep ICS compromise.

**Rule:** DDoS on HMI should require one DDoS setup or tool card. Do not let it be played as a standalone event.

## Core Chain 3: Misconfiguration to Pivot

```text
Aux Scanner / Shodan / Nmap
  -> Firewall Misconfiguration
  -> RDP / External Access
  -> Network Position
```

**Purpose:** models opportunistic Hacktivist exploitation of exposed services.

**Defender counters:**

- Firewall Rule Update
- Security Audit
- MFA
- Secure Remote Access Gateway

## Core Chain 4: Public Embarrassment

```text
Application Access
  -> Credential Harvesting / Exploit / C2 Communication
  -> Website Defacement
```

**Purpose:** gives Hacktivist a non-ICS win path focused on reputation and public pressure.

**Rule:** Website Defacement should affect public-facing assets only. It should not disable PLCs, pumps, or treatment controls.

## Conditional Chain 5: ICS Disruption

```text
Network Position / Unsecured Remote Access / Rogue Workstation
  -> PLC Hijacker
  -> Valve Malfunction Trigger / System Reset / Circuit Breaker Shutdown
```

**Purpose:** gives Hacktivist a scary but conditional ICS path.

**Balance restriction:** PLC Hijacker should be rare/legendary or scenario-limited. Do not pair it with PLC Injector or Malicious Firmware Loader in the baseline Hacktivist deck.

## Defensive counter chains for Medium Organization

Medium Organization needs enough answers to prevent Hacktivist from feeling unstoppable.

```text
MFA
  -> blocks RDP / Unsecured Remote Access
```

```text
Secure Remote Access Gateway
  -> blocks RDP / Remote Access
  -> enables System Reset as a defender tool only
```

```text
Network Monitor / EDR Alert
  -> removes C2 Communication
  -> weakens Network Position
```

```text
Firewall Rule Update / Security Audit
  -> removes Firewall Misconfiguration
  -> reduces DDoS setup effectiveness
```

```text
Incident Responder / Playbook
  -> cancels one active Impact effect
  -> restores one inactive Asset next turn
```

## Recommended Hacktivist win condition pressure

Hacktivist should win by stacking SCP loss and temporary disruption, not by permanently destroying water systems.

Suggested SCP effects:

- Website Defacement: defender loses 1 SCP, or 2 if Cloud Presence is active.
- DDoS on HMI: defender loses 1 SCP, or 2 on a d20 roll of 10+.
- System Reset: defender loses 1 SCP only if remote/internal access is already active.
- Circuit Breaker Shutdown: defender loses 1 SCP and one Asset is inactive for 1 turn.
- Valve Malfunction Trigger: defender loses 1 SCP only when paired with PLC Hijacker.
