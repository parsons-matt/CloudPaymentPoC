| Role | Responsibilities | Key Restriction | Privilege Level |
|---|---|---|---|
| Security Personnel | Manage approved security rules and review findings | Cannot change payment-processing logic | Domain admin |
| Infrastructure Personnel | Manage infrastructure and onboard simulated merchants or banks | Cannot change assessment logic or approve their own security exceptions | Domain admin |
| Payment Processing Personnel | Configure simulated processing and authorisation rules | Cannot modify AWS network security controls | Domain admin |
| Software Assessment Tool Personnel | Develop and propose new assessor checks | Code changes require review before deployment | Elevated privileges |
| Emergency Access Administrator | Temporarily restore or secure the environment during an emergency | Requires strong authentication, time-limited access, alerting, and post-use review. Cannot approve or deploy their own software changes or bypass required code review | Emergency administrator, highest privileges |
| Identity and Access Administrator | Create, disable, and assign user accounts and roles | Cannot grant themselves access, approve their own access requests, or change payment-processing or assessment logic | Domain admin |
| Independent Approver / Reviewer | Approve security exceptions and review sensitive changes or emergency actions | Cannot approve their own request or perform the change they are approving | Acceptance privileges |
| Read-Only Auditor | View configurations, findings, access records, and audit logs | Cannot modify settings, approve exceptions, or access secrets unless specifically required | No privileges |
