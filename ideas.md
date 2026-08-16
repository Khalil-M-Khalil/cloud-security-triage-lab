# Cloud Security Triage Lab — Design Brief

## Three directions considered

### Theme Name: Cloud Cartography
Very Brief Intro: A visual cloud estate map where identity, logging, and encryption signals form a navigable operational landscape.
Probability: 0.082

### Theme Name: Triage Desk
Very Brief Intro: A focused security operations desk built around queues, severity, and crisp remediation decisions.
Probability: 0.071

### Theme Name: Misconfiguration Field Notes
Very Brief Intro: An editorial casebook that turns cloud configuration evidence into concise, defensible findings.
Probability: 0.064

## Chosen approach: Triage Desk

### Design Movement
Editorial security operations: a tactile command desk inspired by incident triage boards, field notebooks, and high-signal enterprise observability tools.

### Core Principles
1. Severity must be explainable through asset exposure, control weakness, and business impact.
2. Every finding has a next action; the lab is not complete when a red badge appears.
3. Keep the asset, evidence, and remediation decision visible together so context is never lost.
4. Synthetic telemetry should feel plausible but remain obviously safe and non-operational.

### Color Philosophy
Warm parchment and graphite establish a calm analyst environment. Cobalt marks cloud-provider context and navigation. Oxide orange marks the active triage decision. Clay red is reserved for exploitable exposure; moss green is reserved for verified remediation or healthy controls.

### Layout Paradigm
A persistent asset rail on the left, a central finding queue, and a right-side remediation docket. The structure resembles a real triage desk and avoids a generic centered dashboard. On mobile, the rail becomes a filter drawer and the docket becomes an expandable decision sheet.

### Signature Elements
1. Severity strips that visually connect a finding to its affected asset.
2. “Why this matters” callouts that translate configuration weakness into business risk.
3. Remediation docket with a closure test instead of a generic “fix” button.

### Interaction Philosophy
The learner triages one finding at a time, chooses a severity, selects a disposition, and writes or accepts a closure test. The system provides a reference rationale after commit, exposing the difference between an overreaction, an underreaction, and a defensible decision.

### Animation
Use 160–240ms transitions for queue selection, severity changes, and docket expansion. Keep the queue stable while detail content changes. Use a small status pulse only for the active finding. Respect reduced motion.

### Typography System
Use `DM Sans` for labels and controls, `Space Grotesk` for section titles and severity numbers, and a monospace face for asset IDs, regions, and finding IDs. Headlines are compact and operational rather than promotional.

### Brand Essence
A practical cloud-security triage simulation for GRC and security analysts who need to turn misconfiguration signals into accountable remediation. Personality: **decisive, evidence-led, operational**.

### Brand Voice
Use direct, calm language that asks the learner to defend a decision.

Example lines:
- “The exposure is real. Now prove the priority.”
- “Close the finding only when the closure test can pass.”

### Wordmark & Logo
A small split-cloud mark made from two offset brackets and a single orange triage dot. It suggests cloud topology without using a generic shield.

### Signature Brand Color
Oxide Orange `#C85B3A`, reused as the active triage action color to connect the two Evidence Atlas labs while keeping the second lab more operational.

## Lab scope

The first release uses a fictional multi-cloud estate with six assets and six findings: public storage exposure, broad IAM policy, missing centralized logging, unencrypted snapshot, stale security group ingress, and an over-permissive service principal. The learner reviews synthetic configuration evidence, sets severity and disposition, then chooses a remediation closure test.

## Safety boundaries

No API calls, cloud credentials, external URLs, or real account names are used. Every asset, region, account identifier, and evidence line is synthetic and clearly labeled as simulation data.
