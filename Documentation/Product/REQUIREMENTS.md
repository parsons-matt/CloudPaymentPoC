# Requirements

## Network security
NET-01 — No direct public access to the processing core  
The processing core must have no directly accessible public endpoint or public IP address and must accept inbound connections only through the explicitly authorised internal paths defined in the v0.1 connection matrix.

NET-02 — Restrict access to service ports  
Every inbound network rule protecting a project component must match an approved source, destination, protocol and port in the connection matrix. The assessor must flag every tested rule that permits traffic outside this policy.

NET-03 — Enforce documented communication paths  
All network connections between in-scope payment components must correspond to a documented connection in the approved v0.1 architecture and connection matrix. The assessor must identify any in-scope network rule that permits an undocumented connection.

NET-04 — Read-only assessor permissions  
The assessor must use a dedicated AWS identity with only the read permissions required for the defined configuration checks, and must have no permission to modify payment infrastructure, security configuration or processing rules.

NET-05 — Configuration checks independent of the payment application  
All v0.1 infrastructure-configuration checks must execute using AWS control-plane APIs and the assessor's authorised read-only identity, without calling payment-processing application endpoints.

## Identity Access Management
IAM-01 — Least-privilege administrative roles  
Before the demonstrator is accepted, each implemented administrative role must have a documented permission matrix identifying its permitted and prohibited actions. Access tests must verify the defined boundaries for every implemented role.

IAM-02 — Controlled and auditable changes  
All changes to assessor code must be committed to version control and reviewed before merging. All in-scope changes to AWS security configuration must be attributable to an authorised identity and recorded through the applicable audit mechanism.

## Assessment Platform
ASS-01 — Complete, evidence-backed assessment results  
Every assessment result produced by the v0.1 assessor must include a rule identifier, outcome, evidence examined, assessment timestamp, explanation, recommended remediation where applicable, and limitations.

## APIs
API-01 - Authenticate external endpoints  
The merchant-facing and bank-facing interfaces must authenticate external counterparties using the mechanism selected for each interface. IP allowlisting alone must not be treated as sufficient proof of identity.

API-02 - JSON messages  
Both external-facing flows must reject malformed JSON, schema violations, missing mandatory fields and values outside defined constraints before the message reaches the processing core.

API-03 - Protect transport and message integrity  
All external API communication must use HTTPS with certificate and hostname verification at the relevant client endpoint. Where message-level signatures or MACs are part of the selected protocol, invalid or altered messages must be rejected.

API-04 - Enforce transaction correlation  
Every simulated bank response must be checked against the outstanding request using a unique transaction reference before the processing core accepts it.

## General Security

SEC-01 Control access to internal APIs  
The application-validation service and processing core must accept API calls only from explicitly authorised internal identities or components, over the documented connections.

##Logs
LOG-01 - Record security-relevant events  
The demonstrator must record authentication failures, message-validation rejections, assessor findings and relevant security-configuration changes without logging secrets or unnecessary sensitive transaction data.
