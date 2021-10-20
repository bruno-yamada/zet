# Cloud readiness checks

- Production and non-production are separated (isolated accounts)
- Users login by assuming IAM roles through the master account
- Strong password policy
- Prefer using permission boundaries on the users/roles when possible
- Differentiate between user accounts and service accounts
- Restrict and audit who can change roles related to VPC, egress rules, white
  lists, etc
- If applicable, isolate projects on VPC or account level
- Require tagging on resources
- Configure billing alerts
- Configure weekly billing reports
- Make sure billing can be filtered by the necessary scope according to how
  projects are isolated
- Configure CloudTrail alerts for not-allowed or suspicious activity
- Make the root account email be a group e-mail to avoid loss of control and
  facilitate sharing when needed
- roo user has MFA, is audited and rarely used (emergency only)
- Properly make the distinction between Production and non-production and treat
  access in the same way
- If using some WAF (Akamai, Cloudflare), make sure to only allow ingress from
  the WAF and have a centralized way to update the ip whitelist as they are sure
  to change from time to time

- Make sure both in-transit and at-rest encryption are in place on as many
  layers as possible (eg. WAF > LB > Application)
- Avoid single-point-of-failure, use availability zones and scale the
  application horizontally
- Must be automatically scalable
- Make period backups and save them encrypted
- Collect application logs
- Collect server logs
- Implement a `request_id` or similar approach to be able to trace requests across
  the logs
- Implement monitoring of HTTPS endpoints and alerts for "soon-to-expire"
  certificates
- If applicable, monitor for out-of-date OS, and security patches that need to
  be applied

- Implement all security tests recommended for a secure product lifecycle (TODO add link to study notes)
- Require pentests if applicable
- Implement a go/nogo process for releases to production (can be automated or not)
- Release management process must exist
- Rollback process must exist
- Deployments are automated
- Identify stakeholders for releases
- Identify support group responsible for the project
- Have a runbook for oncall ops team to act on incidents


> tags: cloud; public-cloud; aws; azure; gcp;

> uid: 20211020083346Z

> links: 

