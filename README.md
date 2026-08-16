# Cloud Triage Desk

## Cloud Security Misconfiguration & Triage Lab

Cloud Triage Desk is a browser-local security lab for practicing cloud misconfiguration triage across a fictional AWS/Azure estate. The learner reviews synthetic configuration evidence, explains business impact, selects severity and disposition, writes a verifiable closure test, and commits the decision to a local simulation timeline.

> This is a training simulation. It does not connect to AWS or Azure, does not inspect real accounts, and does not certify security or compliance.

## Learner workflow

The learner enters the Northstar Platform cloud estate and works through a finding queue. Each finding provides an affected asset, cloud provider, region, configuration evidence, and impact statement. The learner must then:

1. Select the relevant finding from the queue or asset map.
2. Read the configuration evidence and “why this matters” context.
3. Choose a severity: Critical, High, or Medium.
4. Choose a disposition: Remediate now, Remediate this sprint, Accept as monitored, or Escalate for risk acceptance.
5. Compare the decision with the reference rationale.
6. Write a closure test that can be verified by a future analyst.
7. Commit the decision to the synthetic case timeline.

The quality score rewards a decision that matches the expected severity and disposition. A closure test is required before the decision can be committed.

## Synthetic estate

| Finding | Asset | Signal | Expected call |
| --- | --- | --- | --- |
| F-001 | AWS S3 patient-export-bucket | Anonymous read and disabled Public Access Block | Critical / Remediate now |
| F-002 | AWS IAM analytics-read-role | Wildcard read access across production buckets | High / Remediate this sprint |
| F-003 | AWS central-audit-trail | Production region missing centralized management logging | High / Remediate this sprint |
| F-004 | Azure payments-worker-nsg | Internet-facing SSH rule | Critical / Remediate now |
| F-005 | Azure release-pipeline-sp | Owner role at subscription scope | High / Remediate this sprint |
| F-006 | Azure billing-prod-sql | Encryption at rest verified | Medium / Accept as monitored |

## What this demonstrates

The lab demonstrates practical cloud-security reasoning rather than memorization. It tests whether a learner can connect a technical configuration to exposure, choose proportionate urgency, distinguish a healthy control signal from a misconfiguration, and define a closure condition that another analyst can validate.

The lab pairs with a cloud evidence collection project: that project gathers evidence metadata, while this experience trains the analyst to interpret the evidence and triage what happens next.

## Safety boundaries

All identifiers, regions, asset names, policy snippets, and event ages are synthetic. The frontend makes no network requests and requires no API key, account, credential, database, or environment variable. Nothing is modified outside the browser session, and refreshing the page resets the simulation.

## Run locally

```bash
pnpm install
pnpm run check
pnpm run build
pnpm run dev
```

Open the local URL printed by Vite. The application is a static React/TypeScript frontend and can be hosted as a static site.

## Methodology references

The scenario uses public cloud-security concepts and educational mappings rather than claiming to be an official benchmark. Reference material:

- [AWS IAM best practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)
- [Amazon S3 Block Public Access](https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-control-block-public-access.html)
- [AWS CloudTrail best practices](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/best-practices-security.html)
- [Microsoft Azure network security groups](https://learn.microsoft.com/en-us/azure/virtual-network/network-security-groups-overview)
- [Microsoft Azure role-based access control](https://learn.microsoft.com/en-us/azure/role-based-access-control/overview)
- [CIS Controls v8](https://www.cisecurity.org/controls/v8)

## License

MIT. See [LICENSE](LICENSE).
