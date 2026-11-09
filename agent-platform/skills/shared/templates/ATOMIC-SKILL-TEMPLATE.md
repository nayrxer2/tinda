ATOMIC-SKILL-TEMPLATE.md

Template Version: 0.1.0
Status: DRAFT — PENDING APPROVAL
Skill Level: ATOMIC
Architecture: Three-Level Hierarchical
Activation Model: On-Demand
Execution Model: Hybrid

1. METADATA
   Field Value
   Name [Atomic Skill Name]
   Version [Semantic Version]
   Description [Specific capability and expected outcome]
   Category [Capability Category]
   Skill ID [ATOMIC-XXX]
   Skill Level ATOMIC
   Parent Domain [Domain Name]
   Parent Subdomain [Subdomain Name]
   Tags [Relevant tags]
   Priority [P0 / P1 / P2 / P3]
   Activation Mode On-Demand
   Status [Draft / Review / Approved]
   1.1 Activation Metadata

MUST ACTIVATE:

[Specific conditions]

MUST NOT ACTIVATE:

[Conditions outside the skill's responsibility]

Dependencies:

HARD: [Required capabilities]
CONDITIONAL: [Condition-dependent capabilities]
RELATED: [Optional supporting capabilities]

Technology Scope:

[Universal / Technology-specific / Platform-specific]

Supported Versions:

[Applicable versions or N/A]

Last Technical Verification:

[Date]

2. MISSION

Define one specific engineering responsibility.

Explain:

The problem this skill solves.
The capability it provides.
The expected outcome.
Why this responsibility deserves independent activation.

The mission must be sufficiently narrow to establish clear ownership.

3. AUTHORITY AND RESPONSIBILITY
   3.1 Owns

[Responsibilities exclusively owned by this skill]

3.2 May Recommend

[Related decisions it may advise on]

3.3 May Modify

[Changes it may prepare or execute when authorized]

3.4 Does Not Own

[Responsibilities belonging to other capabilities]

3.5 Delegation Requirements

[Conditions requiring another specialist skill or domain]

4. ACTIVATION PROTOCOL
   4.1 MUST ACTIVATE

Define concrete task conditions requiring activation.

4.2 MUST NOT ACTIVATE

Define situations where another capability owns the task.

4.3 Activation Decision Framework

Explain how to determine whether the task genuinely requires this capability.

Do not rely on keyword matching alone.

4.4 Required Context

Identify the information needed for correct execution.

4.5 Non-Activation Behavior

Explain what to do when the task is outside scope.

5. REQUIRED KNOWLEDGE AND MASTERY

Document the knowledge necessary to execute the capability.

Include only relevant material:

Fundamental concepts.
Advanced concepts where justified.
Technical terminology.
Engineering principles.
Applicable standards.
Framework-specific knowledge.
Common misconceptions.
Relevant limitations.

Distinguish universal knowledge from technology-specific knowledge.

6. INPUT REQUIREMENTS
   6.1 Required Inputs

[Information necessary for correct execution]

6.2 Optional Inputs

[Information that improves execution but is not mandatory]

6.3 Assumptions

[Explicit assumptions, if unavoidable]

6.4 Environmental Constraints

[Platform, technology, version, permissions, or project constraints]

6.5 Missing Information Handling

Explain:

What can be safely inferred.
What requires clarification.
What must not be fabricated.
When execution must stop. 7. EXECUTION WORKFLOW

Define a repeatable engineering workflow.

Each step must identify:

Objective.
What to inspect.
What to evaluate.
Decisions to make.
Actions to perform.
Evidence to collect.
Expected output.
Step 1 — [Name]

[Detailed instructions]

Step 2 — [Name]

[Detailed instructions]

Step 3 — [Name]

[Detailed instructions]

Add or remove steps according to the actual capability.

Do not force irrelevant workflow stages into every skill.

8. DECISION FRAMEWORK

Define the decisions this skill is authorized to make.

For each significant decision explain:

Decision criteria.
Relevant engineering principles.
Available alternatives.
Trade-offs.
Exceptions.
Rejection conditions.

Include measurable thresholds only when supported by evidence or project requirements.

9. CONSTRAINTS AND ANTI-PATTERNS
   9.1 MUST

[Mandatory rules]

9.2 MUST NOT

[Prohibited behavior]

9.3 Common Mistakes

[Frequent implementation or reasoning errors]

9.4 Anti-Patterns

[Practices that produce unacceptable results]

9.5 Dangerous Assumptions

[Assumptions that could create material risk]

9.6 Overengineering Risks

[Unnecessary complexity to avoid]

10. DELIVERABLES

Define the expected outputs.

Examples:

Technical analysis.
Engineering recommendations.
Proposed implementation.
Code changes.
Configuration changes.
Documentation.
Review findings.
Validation results.

Deliverables must be proportional to the task.

Do not require unnecessary reports or artifacts.

11. VALIDATION
    11.1 Validation Criteria

Define measurable checks relevant to the capability.

Consider:

Correctness.
Completeness.
Requirement compliance.
Compatibility.
Security.
Maintainability.
Performance.
Reliability.

Only include applicable criteria.

11.2 Validation Methods

Identify suitable methods:

Code inspection.
Automated tests.
Static analysis.
Runtime execution.
Manual verification.
Documentation verification.
Independent review.
11.3 Validation Status

Use:

NOT PLANNED.
PLANNED.
ATTEMPTED.
PASSED.
FAILED.
NOT PERFORMED.
11.4 Evidence Requirements

Identify the evidence required to support successful validation.

Never claim success without evidence.

12. FAILURE HANDLING

Define behavior when:

Required information is missing.
Requirements conflict.
A technical blocker occurs.
The environment is unsupported.
A dependency is unavailable.
Validation fails.
The proposed solution introduces unacceptable risk.
Authorization is missing.

For each failure condition identify:

Detection.
Immediate response.
Recovery options.
Escalation requirements.
Reporting expectations. 13. EVALUATION SCENARIOS

Every skill must include practical behavioral scenarios.

13.1 Normal Scenario

[Representative correct usage]

Expected behavior:

[Expected outcome]

13.2 Edge Case

[Unusual but valid situation]

Expected behavior:

[Expected outcome]

13.3 Incorrect Assumption

[Situation containing a flawed assumption]

Expected behavior:

[Expected response]

13.4 Anti-Pattern

[Situation involving a known poor approach]

Expected behavior:

[Expected response]

13.5 Conflicting Requirements

[Situation containing competing requirements]

Expected behavior:

[Expected response]

13.6 Non-Activation Scenario

[Situation where this skill should not activate]

Expected behavior:

[Expected response]

14. EVALUATION SCORECARD

Define capability-specific evaluation criteria.

Criterion Evaluation Method Weight Critical?
Responsibility compliance [Method] [Weight] [Yes/No]
Technical correctness [Method] [Weight] [Yes/No]
Workflow execution [Method] [Weight] [Yes/No]
Validation quality [Method] [Weight] [Yes/No]
Evidence quality [Method] [Weight] [Yes/No]

Define:

Passing threshold.
Critical failure conditions.
Scoring methodology.
Evidence requirements.

Critical failures must never be compensated for by high scores elsewhere.

15. REFERENCES

Provide direct links to verified sources.

Classify references.

15.1 Courses

[Course title, instructor, provider, URL, evaluation status]

15.2 Official Documentation

[Documentation title, organization, URL, relevant version]

15.3 Books

[Book title, author, publisher, edition]

15.4 Standards and Specifications

[Standard, issuing organization, version, URL]

15.5 Academic Research

[Publication, authors, year, DOI or URL]

15.6 Supplementary Resources

[Relevant supplementary material]

Identify inaccessible or unverified resources.

16. DEFINITION OF DONE

Define precisely when the skill has completed its responsibility.

Include:

Required outcome.
Deliverables.
Validation conditions.
Remaining limitations.
Escalation requirements. 17. PROFESSIONAL OPERATING STANDARD

The skill must:

Challenge flawed assumptions.
Avoid unsupported confidence.
Explain meaningful trade-offs.
Identify uncertainty.
Refuse to fabricate evidence.
Respect domain boundaries.
Prefer maintainable decisions.
Avoid unnecessary complexity.
Respect execution permissions.
Report incomplete work honestly. 18. CHANGE HISTORY
Version Date Change Status
0.1.0 [Date] Initial creation Draft
