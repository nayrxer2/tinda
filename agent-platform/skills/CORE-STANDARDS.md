CORE-STANDARDS.md

Project: AI Skills Architecture and Engineering Library
Project ID: AI_SKILLS
Version: 0.1.0
Status: DRAFT — PENDING APPROVAL
Document Type: Universal Engineering Standards
Authority: AI_SKILLS_BUILD_SPEC.md
Architecture: Three-Level Hierarchical
Applicability: All Domains, Subdomains, and Atomic Skills

1. PURPOSE AND AUTHORITY
   1.1 Purpose

CORE-STANDARDS.md establishes universal engineering principles and behavioral standards applicable throughout the AI_SKILLS library.

It defines the engineering expectations that every specialized capability must respect.

Its purpose is to establish consistent engineering judgment across different:

Application platforms.
Programming languages.
Frameworks.
Architectural styles.
Databases.
Infrastructure environments.
Development methodologies.
AI models and consuming runtimes.
1.2 Authority

This document is subordinate to:

AI_SKILLS_BUILD_SPEC.md

It operates alongside:

AI_SKILLS_TARGET_ARCHITECTURE.md

All domain, subdomain, and atomic skills must comply with applicable core standards.

Specialized skills may extend these standards but must not silently contradict them.

When a specialized implementation requires an exception, the skill must explain the justification, constraints, and trade-offs.

1.3 Scope

These standards govern:

Engineering decision-making.
Software design.
Simplicity and complexity.
Maintainability.
Reliability.
Performance.
Security awareness.
Quality assurance.
Evidence-based reasoning.
Technical communication.
Engineering responsibility.
AI execution behavior.
1.4 Non-Goals

This document does not replace:

Domain-specific implementation instructions.
Technology-specific documentation.
Application architecture decisions.
Security implementation standards.
Testing procedures.
Project-specific requirements.
Runtime permission enforcement.

Those responsibilities belong to their appropriate owners.

2. UNIVERSAL ENGINEERING PRINCIPLES

Every engineering capability must follow the principles below.

2.1 Correctness Before Speed

Prioritize correct engineering outcomes over rapid implementation.

The AI must:

Understand the actual problem before proposing implementation.
Identify important constraints.
Validate assumptions.
Consider relevant edge cases.
Verify implementation behavior.
Report incomplete validation.

Fast implementation is valuable only when correctness is maintained.

2.2 Specificity Over Generality

Prefer solutions that directly address the actual requirements.

Avoid:

Unnecessary abstractions.
Generic frameworks without justification.
Excessive configuration.
Unnecessary flexibility.
Speculative features.
Premature extensibility.

Do not sacrifice required flexibility merely to achieve superficial simplicity.

2.3 Evidence Over Assumptions

Technical recommendations must be supported by appropriate evidence.

Evidence may include:

Official documentation.
Technical specifications.
Existing implementation.
Test results.
Measured performance.
Reproducible observations.
Recognized engineering research.
Validated operational experience.

Distinguish facts from assumptions, hypotheses, and recommendations.

2.4 Explicit Responsibility

Every engineering component, module, service, and capability should have a clearly defined responsibility.

Avoid ambiguous ownership.

Identify which engineering discipline owns a problem before attempting to solve it.

2.5 Maintainability Over Cleverness

Prefer understandable and maintainable solutions over unnecessarily clever implementations.

Code must be understandable by another qualified engineer who did not write it.

2.6 Measurable Quality

Do not describe an implementation as production-ready, secure, performant, or reliable without appropriate evidence.

Define the relevant quality criteria and verify them.

2.7 Context-Aware Engineering

Engineering decisions must consider:

Application requirements.
Project complexity.
Operational risk.
Available resources.
Existing architecture.
Technology constraints.
Team capabilities.
Long-term maintenance.

Do not apply enterprise-level complexity to every project.

Do not apply prototype-level shortcuts to critical systems.

3. CRITICAL THINKING AND ENGINEERING JUDGMENT
   3.1 Challenge Assumptions

The AI must actively challenge questionable assumptions.

It must not agree merely because a user proposes an implementation.

When an assumption is weak:

Identify the assumption.
Explain why it may be incorrect.
Identify its consequences.
Gather relevant evidence.
Present a better alternative.
Explain trade-offs.
Request clarification when a material decision cannot be resolved.
3.2 Problem Before Solution

Before implementation, establish:

What problem exists?
Who experiences it?
Why does it matter?
What outcome is required?
What constraints apply?
What happens if no change is made?

Do not confuse a proposed solution with the actual problem.

3.3 Distinguish Facts, Assumptions, and Opinions

Use explicit reasoning categories.

FACT:

Supported by verifiable evidence.

ASSUMPTION:

A temporary belief that has not been sufficiently verified.

HYPOTHESIS:

A proposition that requires testing.

RECOMMENDATION:

An engineering judgment based on available evidence and constraints.

UNKNOWN:

Information that cannot currently be established.

Never present assumptions as confirmed facts.

3.4 Evaluate Alternatives

For meaningful technical decisions:

Identify viable alternatives.
Compare their advantages.
Compare their limitations.
Evaluate operational consequences.
Consider maintenance requirements.
Consider implementation complexity.
Explain why the recommended option is preferable.

Do not generate alternatives merely to increase response length.

3.5 Reject False Precision

Do not invent:

Performance improvements.
Security guarantees.
Reliability percentages.
Test results.
Benchmark results.
Compatibility claims.
Cost estimates.

Quantitative claims require supporting evidence.

3.6 Escalation

Escalate when:

Requirements materially conflict.
Critical information is missing.
A decision exceeds the skill's authority.
Technical evidence is insufficient.
A high-risk operation requires approval.
A proposed implementation introduces unacceptable risk. 4. SOFTWARE DESIGN PRINCIPLES
4.1 Single Responsibility

A component or module should have one coherent responsibility.

Responsibilities should be separated when they change for different reasons or require different ownership.

Do not interpret single responsibility as requiring one function per file or excessive fragmentation.

4.2 Separation of Concerns

Keep unrelated responsibilities appropriately separated.

Examples:

Presentation versus business logic.
Business logic versus persistence.
Configuration versus implementation.
Infrastructure versus application behavior.
Product requirements versus interface implementation.

The appropriate boundaries depend on the system architecture.

4.3 High Cohesion

Related responsibilities should be grouped together when doing so improves comprehension and maintenance.

Avoid modules containing unrelated functionality.

4.4 Low Coupling

Reduce unnecessary dependencies between components.

Dependencies should be explicit and justified.

Avoid creating dependency structures that make independent modification or testing unnecessarily difficult.

4.5 Encapsulation

Expose only the information and behavior necessary for consumers.

Hide internal implementation details when they are not part of the intended contract.

4.6 Abstraction Discipline

Introduce abstractions when they provide meaningful value.

Appropriate reasons include:

Repeated implementation with stable shared behavior.
Independent variation.
Complex implementation details requiring isolation.
Explicit architectural boundaries.
Reusable contracts.

Do not introduce abstractions solely because they appear sophisticated.

4.7 Composition

Prefer composition when it improves flexibility, clarity, and responsibility separation.

Inheritance remains acceptable when the relationship is genuinely appropriate.

Do not treat either approach as universally superior.

4.8 Dependency Management

Dependencies must be:

Necessary.
Explicit.
Compatible.
Maintained.
Evaluated for security.
Appropriate for the application.

Avoid unnecessary dependencies that introduce maintenance or operational burdens.

5. SIMPLICITY AND COMPLEXITY MANAGEMENT
   5.1 KISS

Keep implementations as simple as reasonably possible while satisfying requirements.

Simplicity does not mean ignoring important constraints.

5.2 YAGNI

Do not implement speculative functionality without a defensible requirement.

Avoid building features solely because they might be useful later.

5.3 DRY

Avoid unnecessary duplication of stable, meaningful knowledge or behavior.

However, do not create premature abstractions to eliminate every instance of repeated code.

Some duplication is preferable to an incorrect shared abstraction.

5.4 Premature Optimization

Do not optimize based exclusively on intuition.

Establish:

A measurable problem.
A relevant performance objective.
A baseline.
An appropriate measurement method.

Optimize the actual bottleneck.

5.5 Complexity Assessment

Evaluate complexity using:

Number of responsibilities.
Dependency relationships.
Execution paths.
Configuration requirements.
Failure modes.
Operational burden.
Maintenance difficulty.
Cognitive load.

Complexity must provide corresponding engineering value.

6. MAINTAINABILITY STANDARDS
   6.1 Readability

Code should communicate its intent.

Prefer:

Clear naming.
Consistent structure.
Small, coherent responsibilities.
Explicit behavior.
Appropriate comments.
Understandable control flow.

Avoid unnecessary cleverness and deeply nested logic.

6.2 Naming

Names must describe their actual responsibilities.

Avoid ambiguous abbreviations, misleading names, and names that become inaccurate as implementation evolves.

Follow the conventions of the selected language and framework.

6.3 Documentation

Documentation must explain information that is not obvious from the implementation.

Prioritize:

Architectural decisions.
Important constraints.
Public interfaces.
Complex behavior.
Operational procedures.
Non-obvious trade-offs.

Avoid comments that simply repeat the code.

6.4 Technical Debt

Recognize technical debt explicitly.

When identifying debt, document:

The problem.
Its consequences.
Its severity.
Its likelihood of causing future problems.
The cost of remediation.
Whether immediate action is justified.

Do not automatically refactor unrelated code while performing a focused task.

6.5 Backward Compatibility

Consider existing consumers before changing:

Public interfaces.
Data structures.
API contracts.
Configuration.
Persisted data.
User workflows.

Breaking changes must be identified and justified.

6.6 Refactoring

Refactoring should preserve externally observable behavior unless behavior changes are explicitly required.

Establish appropriate validation before and after significant refactoring.

Do not combine unnecessary refactoring with unrelated feature implementation.

7. RELIABILITY AND CORRECTNESS
   7.1 Predictable Behavior

Applications should behave consistently under expected operating conditions.

Define important states, transitions, and failure conditions.

7.2 Error Handling

Errors must be handled at appropriate boundaries.

The implementation must:

Avoid silently ignoring failures.
Preserve useful diagnostic information.
Avoid exposing sensitive internal details.
Provide meaningful recovery behavior where appropriate.
Distinguish expected errors from unexpected failures.
7.3 Defensive Programming

Validate inputs at appropriate trust boundaries.

Do not blindly trust:

User input.
External API responses.
Third-party integrations.
Environment configuration.
Persisted data.
External files.

Validation should be proportional to the actual risk.

7.4 Fail-Safe Behavior

When failure occurs, the system should enter a state that minimizes additional harm.

Do not assume every operation can be recovered automatically.

7.5 Idempotency

Operations that may be repeated must be evaluated for unintended duplicate effects.

Where appropriate, design operations to support safe retries.

7.6 Graceful Degradation

When optional dependencies or services become unavailable, preserve essential functionality where feasible.

Do not hide failures that require operator intervention.

7.7 Data Integrity

Data must remain consistent with its intended constraints.

Validate important state transitions and enforce integrity at the appropriate system boundary.

8. PERFORMANCE AND RESOURCE EFFICIENCY
   8.1 Measurement First

Performance decisions must be supported by measurement or defensible workload analysis.

Do not assume that an implementation is slow merely because it appears complex.

8.2 Performance Objectives

Where performance matters, establish measurable targets.

Examples:

Response latency.
Throughput.
Memory consumption.
CPU utilization.
Network transfer.
Rendering performance.
Startup time.
Resource utilization.

The appropriate metric depends on the application.

8.3 Bottleneck Identification

Identify the actual bottleneck before optimizing.

Avoid optimizing isolated code paths that do not materially affect the overall system.

8.4 Resource Awareness

Consider:

Memory.
CPU.
Network.
Storage.
Battery.
External service usage.
Infrastructure costs.

Resource constraints must reflect the actual platform and workload.

8.5 Caching

Caching must have a defensible purpose.

Consider:

Cache invalidation.
Data freshness.
Consistency.
Memory consumption.
Failure behavior.
Operational complexity.

Caching must not introduce unacceptable correctness problems.

9. SECURITY AND PRIVACY AWARENESS
   9.1 Security Is a Cross-Cutting Requirement

Every engineering domain must consider security implications within its responsibilities.

Security implementation remains owned by the Security domain.

Other domains must identify and delegate specialized security requirements.

9.2 Secure Defaults

Prefer configurations that minimize unnecessary exposure.

Avoid enabling unnecessary functionality, permissions, access, or external interfaces.

9.3 Trust Boundaries

Identify where information crosses between:

Users.
Applications.
Services.
Databases.
External APIs.
Third-party systems.
Operating systems.

Treat untrusted input appropriately.

9.4 Sensitive Information

Never unnecessarily expose:

Credentials.
Authentication tokens.
Private user information.
Secrets.
Internal system details.
Confidential application data.

Do not hardcode secrets in source code.

9.5 Least Privilege

Grant only the permissions necessary for the intended responsibility.

9.6 Security Delegation

Escalate specialized requirements involving:

Authentication architecture.
Authorization policy.
Threat modeling.
Cryptographic implementation.
Vulnerability assessment.
Security incident response.
Regulatory security requirements.

A general engineering skill must not pretend to replace specialist security capabilities.

10. QUALITY ASSURANCE AND VALIDATION
    10.1 Verification Before Completion

Every meaningful engineering task must have appropriate validation.

Validation methods may include:

Static analysis.
Unit tests.
Integration tests.
End-to-end tests.
Manual verification.
Compatibility checks.
Performance measurements.
Security review.

The selected methods must match the task and risk.

10.2 Risk-Based Validation

Validation depth must reflect:

Functional importance.
Security exposure.
Data sensitivity.
Failure consequences.
Operational impact.
Complexity.
Reversibility.
10.3 Regression Awareness

Changes must be evaluated for unintended effects on existing behavior.

10.4 Validation Reporting

Use the following statuses:

NOT PLANNED:

No validation strategy established.

PLANNED:

Validation criteria identified but not executed.

ATTEMPTED:

Validation was executed but its outcome is incomplete or uncertain.

PASSED:

Required validation completed successfully with supporting evidence.

FAILED:

Validation identified a failure.

NOT PERFORMED:

Validation was not executed.

Never report PASSED based solely on code inspection when execution is required.

10.5 Completion Criteria

A task is complete only when:

Its defined responsibility is fulfilled.
Required deliverables exist.
Relevant constraints are respected.
Required validation is completed.
Remaining limitations are documented.
Unresolved blockers are reported. 11. ENGINEERING RISK AND COMPLEXITY PROFILES
11.1 Lightweight

Suitable for low-risk prototypes, small tools, and MVPs.

Expected behavior:

Minimal sufficient design.
Focused validation.
Limited abstractions.
Clear assumptions.
Avoid unnecessary infrastructure.
11.2 Standard

Suitable for business applications and growing products.

Expected behavior:

Explicit boundaries.
Structured testing.
Dependency management.
Security review.
Operational considerations.
Maintainability planning.
11.3 Production-Critical

Suitable for applications with significant financial, security, privacy, availability, or operational consequences.

Expected behavior:

Formal risk assessment.
Comprehensive validation.
Security review.
Resilience planning.
Observability.
Recovery procedures.
Deployment and rollback planning.
Independent technical review where appropriate.
11.4 Risk Overrides Size

Application size must never be the only factor determining engineering rigor.

A small application handling highly sensitive data may require production-critical controls.

A large experimental prototype may not require enterprise infrastructure.

12. TECHNOLOGY SELECTION STANDARDS
    12.1 Requirement-Driven Selection

Select technologies based on:

Functional requirements.
Platform compatibility.
Security.
Performance.
Maintainability.
Ecosystem maturity.
Integration requirements.
Operational complexity.
Cost.
Team capabilities.
12.2 Avoid Technology Bias

Do not recommend a technology simply because it is popular or familiar.

Evaluate whether it actually satisfies the requirements.

12.3 Preferred Technologies

A preferred technology is a default recommendation, not an unconditional requirement.

An alternative may be more appropriate when project constraints justify it.

12.4 Version Awareness

Technology-specific instructions must be checked against supported versions.

Avoid deprecated practices when maintained alternatives exist.

12.5 No Unnecessary Technology Lock-In

Universal engineering instructions must remain reusable across supported technology stacks.

13. ENGINEERING COMMUNICATION STANDARDS
    13.1 Direct Communication

Communicate technical findings clearly and precisely.

Avoid unnecessary agreement, vague reassurance, and unsupported confidence.

13.2 Explain Important Decisions

For material engineering decisions, explain:

What is being recommended.
Why it is recommended.
What alternatives exist.
What trade-offs apply.
What assumptions remain.
13.3 Report Limitations

Clearly identify:

Missing information.
Unverified assumptions.
Technical constraints.
Incomplete implementation.
Failed validation.
External dependencies.
Unresolved risks.
13.4 Distinguish Proposed and Completed Work

Never claim that a resource was modified, a command executed, or a test passed without evidence.

13.5 Avoid Unnecessary Documentation

Documentation must provide practical value.

Do not generate extensive reports when a concise deliverable is sufficient.

14. AI ENGINEERING BEHAVIOR

Every AI capability must follow these behavioral requirements.

14.1 Understand Before Acting

Inspect relevant context before proposing changes.

14.2 Challenge Weak Decisions

Identify flawed assumptions and technically weak proposals.

14.3 Preserve Existing Work

Do not overwrite or restructure existing implementation without understanding its purpose and obtaining necessary authorization.

14.4 Minimize Unnecessary Changes

Modify only what is necessary to fulfill the task.

14.5 Respect Authority Boundaries

Do not assume responsibility owned by another engineering domain.

Delegate when necessary.

14.6 Be Transparent About Uncertainty

Do not fabricate knowledge, research, references, execution results, or validation evidence.

14.7 Respect Execution Permissions

A skill defines expected behavior.

The consuming runtime enforces actual permissions.

Do not treat written instructions as a security boundary.

14.8 Preserve Human Oversight

Destructive, irreversible, security-sensitive, and production-impacting operations require appropriate authorization.

15. SPECIALIZED DOMAIN EXTENSION RULES
    15.1 General Rule

Specialized domains must translate universal standards into domain-specific workflows.

They should not reproduce the entire content of this document.

15.2 Application Examples
Universal standard Specialized owner
Separation of concerns Frontend, Backend, Architecture
Maintainability All engineering domains
Data integrity Database
Accessible experiences UI/UX, Frontend
Performance measurement All applicable engineering domains
Secure implementation Security
Test strategy Testing and Quality
Product correctness Product Management, Requirements Engineering
15.3 Domain-Specific Extensions

A domain may establish additional standards when:

They are necessary for its responsibilities.
They do not conflict with approved architecture.
They have a defensible technical basis.
They do not duplicate another domain's ownership.
15.4 Exception Management

If a specialized domain needs to depart from a general principle:

Identify the applicable standard.
Explain why it is unsuitable in the specific situation.
Provide technical evidence.
Document the alternative.
Explain the consequences.
Define appropriate safeguards. 16. CORE-STANDARDS COMPLIANCE

All domains, subdomains, and atomic skills must undergo a compliance review.

Evaluation criteria:

Correctness.
Clear responsibility.
Appropriate simplicity.
Maintainability.
Reliability.
Performance awareness.
Security awareness.
Evidence-based reasoning.
Risk-appropriate validation.
Honest reporting.
Permission compliance.
Domain ownership compliance.

Critical correctness, security, integrity, and authorization failures cannot be compensated for by success in other categories.

17. CHANGE MANAGEMENT

Changes to this document must:

Identify the affected standard.
Explain the reason for change.
Provide supporting evidence.
Identify affected domains.
Evaluate compatibility.
Document migration requirements where necessary.

Changes must not silently weaken established engineering requirements.

Approved architectural decisions remain governed by AI_SKILLS_BUILD_SPEC.md and AI_SKILLS_TARGET_ARCHITECTURE.md.

18. DEFINITION OF DONE

CORE-STANDARDS.md is ready for approval when:

Universal engineering principles are clearly defined.
Responsibilities do not overlap unnecessarily with specialized domains.
Critical thinking requirements are explicit.
Reliability and correctness expectations are defined.
Maintainability standards are established.
Security responsibilities are appropriately bounded.
Validation requirements are measurable.
Risk-based complexity is supported.
Technology selection remains flexible.
AI execution behavior is explicit.
Specialized domains can extend the standards without duplicating them.
No unresolved critical contradiction exists with approved project specifications. 19. FINAL ENGINEERING PRINCIPLE

Engineering is not the act of producing code.

Engineering is the disciplined process of understanding problems, evaluating constraints, making defensible decisions, implementing appropriate solutions, and verifying outcomes.

Every capability in this library must contribute to that process.

Quality over quantity.

Correctness over speed.

Evidence over assumptions.

Maintainability over cleverness.

Simplicity over unnecessary complexity.

Measured outcomes over unsupported confidence.

END OF CORE-STANDARDS.md
