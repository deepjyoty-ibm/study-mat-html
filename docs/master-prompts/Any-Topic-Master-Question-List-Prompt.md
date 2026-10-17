# Master Prompt: Generate an Interview & Revision Question List for Any Topic

Copy and use the prompt below. Replace `[TOPIC NAME]` with your topic.

---

## Prompt

You are my technical teacher and interview-preparation mentor.

Create a **complete, interview-focused, exam-revision question list** for the following topic:

**Topic: `[TOPIC NAME]`**

The final output must be written in **English** and delivered as a **downloadable Markdown (`.md`) file**.

## My Goal

I do not want a large collection of repetitive or fragmented questions. I want a carefully designed **master question list** that I can revise one day before an interview or examination.

Each main question should combine closely related concepts so that reading one well-structured answer and one practical code example later will help me revise the entire concept cluster.

For example, do not create separate questions for every small method, class, property, configuration field, request parameter, or status code when they can be explained naturally through one complete practical question.

## 1. Understand and Define the Topic Boundary

Before preparing the questions:

1. Identify what directly belongs to `[TOPIC NAME]`.
2. Identify related technologies that integrate with the topic but have their own separate concepts.
3. Include only the integration-side knowledge required for `[TOPIC NAME]`.
4. Move the internal concepts of related technologies to a final **Scope Boundary / Study Separately** section.
5. Do not mix unrelated chapters merely because they are commonly used together.

Example rule:

- Explain how the main topic integrates with another service.
- Do not include the complete internal architecture of that other service unless it is essential to understanding the main topic.

## 2. Consolidate Related Concepts into Master Questions

Create fewer but deeper questions.

Every master question should:

- Cover one meaningful concept cluster.
- Include all closely related sub-concepts under a `### Cover` section.
- Request a practical example where useful.
- Request complete code where the topic involves programming.
- Include configuration, execution flow, and expected behavior where relevant.
- Explain both **what** and **why**, not only definitions.
- Avoid repeating concepts already covered by another master question.

Bad structure:

- What is Class A?
- What is Method B?
- What is Property C?
- How do I read Parameter D?

Better structure:

- Build and explain one complete practical implementation covering Class A, Method B, Property C, Parameter D, validation, configuration, error handling, and execution flow.

## 3. Required Sections

Organize the final question list into the following sections. Adapt the section names when necessary for the selected topic.

### Part 1: Fundamentals

Include master questions covering:

- Core definition
- Purpose
- How it works
- Core components
- Execution/lifecycle overview
- Important terminology
- Main use cases
- When to use it
- When not to use it
- Comparison with closely related alternatives

### Part 2: Core Features and Practical Implementation

Include the topic's major features, components, modes, types, operations, or workflows.

For every major feature:

- Create one consolidated master question where possible.
- Ask for a practical implementation.
- Ask for complete code if applicable.
- Include project structure, configuration, request/input, processing, output, validation, error handling, and logging where relevant.

Do not omit important feature types.

### Part 3: Configuration and Environment Management

Cover where applicable:

- Local configuration
- Development, QA, staging, and production configuration
- Environment variables
- Configuration hierarchy
- Strongly typed configuration/options
- Secure values vs normal configuration
- How the same codebase works across environments

### Part 4: Security

Cover where applicable:

- Authentication
- Authorization
- Identity
- Tokens/keys/credentials
- Role-based access
- Secret management
- Secure local development
- Secure production access
- Common security mistakes
- Secretless/security-first design

### Part 5: Performance, Runtime and Scaling

Cover where applicable:

- Runtime behavior
- Lifecycle
- Concurrency
- Parallelism
- Scaling
- Resource usage
- Timeouts
- Startup behavior
- Performance bottlenecks
- Failure modes
- Optimization

### Part 6: Networking and Connectivity

Cover where applicable:

- Inbound connectivity
- Outbound connectivity
- Public and private access
- DNS
- Firewall/access restrictions
- Private networking
- Connectivity troubleshooting

If networking is not relevant, omit this section instead of forcing unrelated questions.

### Part 7: Error Handling, Logging and Monitoring

Cover where applicable:

- Local error handling
- Centralized/global error handling
- Structured logging
- Log levels
- Monitoring
- Metrics
- Tracing/correlation
- Dependency monitoring
- Production troubleshooting

### Part 8: Deployment and Production Readiness

Cover where applicable:

- Build and deployment
- Environment-specific settings
- CI/CD at the level required by this topic
- Safe release strategy
- Production checklist
- Operational readiness
- Moving from local development to production

### Part 9: Tricky Interview Questions

Create concise but conceptually difficult questions that test real understanding.

Include questions about:

- Common misconceptions
- Similar concepts that are often confused
- Hidden lifecycle behavior
- Scope/lifetime issues
- Local vs production differences
- Unexpected runtime behavior
- Edge cases
- Frequently made design mistakes

Do not repeat the basic questions word-for-word.

### Part 10: Scenario-Based Questions

Create realistic troubleshooting and decision-making scenarios.

Include scenarios such as:

- Works locally but fails in production
- Sudden traffic/load increase
- Slow production performance
- Authentication or permission failure
- Configuration mismatch
- Dependency failure
- Timeout or long-running processing
- Resource exhaustion
- Multi-environment deployment
- Hard-coded credentials
- Intermittent failures

For each scenario, add a short `### Think About` or `### Investigate` checklist. Do not provide the full answer unless explicitly requested.

### Part 11: Architecture and Design Questions

Create advanced questions covering:

- Production-grade architecture
- Large-project code organization
- Separation of concerns
- Security-first architecture
- High-scale architecture
- Resiliency
- Observability
- State management
- Integration boundaries
- Choosing this technology versus alternatives
- Architectural trade-offs

Use Mermaid or ASCII diagrams only where they improve revision clarity.

### Part 12: Final One-Shot Revision Question

Create one final master question that asks the learner to explain the complete topic from design to production.

Under it, include a compact concept tree that revises all major areas of the topic.

### Part 13: Recommended Study Order

Provide the recommended question ranges/order, for example:

```text
Q1-Q3   -> Fundamentals
Q4-Q10  -> Core implementation
Q11-Q14 -> Configuration and security
...
Final Q -> One-shot revision
```

### Part 14: Scope Boundary / Study Separately

Clearly list:

- Concepts directly covered in this topic
- Related services or technologies mentioned only for integration
- Concepts that should be studied as separate chapters

This section is mandatory because I do not want unrelated service internals mixed into the main topic.

## 4. Code Requirements

When `[TOPIC NAME]` is a programming or cloud-development topic:

- Use the latest stable and recommended programming model unless I specify a version.
- Mention the selected language, framework, runtime, SDK, or model at the beginning.
- Prefer complete, realistic examples over isolated snippets.
- Include required package/dependency names where useful.
- Include relevant project/file structure.
- Include configuration files where required.
- Do not place code in Markdown tables.

Preferred language/framework, if applicable:

- Language: `[PREFERRED LANGUAGE]`
- Framework/runtime: `[FRAMEWORK OR VERSION]`

If these values are not supplied, select the most widely used current stable option and state the assumption clearly.

## 5. Question-Design Rules

Follow these rules strictly:

1. Do not inflate the number of questions.
2. Do not create separate questions for sub-concepts that fit naturally into one complete example.
3. Do not omit any major feature, type, mode, or workflow belonging directly to the topic.
4. Do not repeat the same concept across basic, tricky, scenario, and architecture sections unless the angle is genuinely different.
5. Keep basic questions broad and implementation-oriented.
6. Keep tricky questions short and concept-focused.
7. Keep scenario questions realistic and diagnostic.
8. Keep architecture questions deep and decision-oriented.
9. Clearly separate the main topic from related technologies.
10. Ensure the list is suitable for interview preparation, examination revision, and practical understanding.
11. Do not write full answers yet. Produce the structured question list and coverage checklist only.
12. Use sequential question numbering across the complete document.

## 6. Quality Check Before Finalizing

Before generating the file, verify that:

- Every major part of `[TOPIC NAME]` is covered.
- No major feature or type is missing.
- Closely related concepts are consolidated.
- Repetitive questions are removed.
- Related-service internals are not mixed into the main chapter.
- Basic, tricky, scenario, and architecture questions are clearly separated.
- The questions progress from beginner to advanced.
- The final revision question covers the complete topic.
- The Markdown headings, lists, code blocks, and diagrams render correctly.
- The output contains no HTML copied from editors.

## 7. Markdown File Requirements

Create one downloadable file named:

`[TOPIC-SLUG]-Master-Interview-Revision-Questions.md`

The file must contain:

```text
Title
Goal
Assumptions / Selected Technology Version
Table of Contents
Fundamentals
Core Features / Practical Implementation
Configuration
Security
Performance / Runtime / Scaling
Networking, if applicable
Error Handling / Logging / Monitoring
Deployment / Production Readiness
Tricky Interview Questions
Scenario-Based Questions
Architecture-Level Questions
Final One-Shot Revision
Recommended Study Order
Scope Boundary / Study Separately
```

## 8. Final Response

After creating the file:

- Provide a direct download link to the `.md` file.
- Mention the filename.
- Do not paste the entire Markdown content into the chat unless I ask for it.
- Do not merely show sample questions. Generate the complete list.
- Do not ask for confirmation before creating the file.

---

## Input Values

```text
Topic: [TOPIC NAME]
Preferred Language: [PREFERRED LANGUAGE OR N/A]
Framework/Runtime: [FRAMEWORK OR VERSION OR LATEST STABLE]
Target Level: [BEGINNER / INTERMEDIATE / INTERVIEW / ADVANCED]
Special Focus: [OPTIONAL]
Exclude: [OPTIONAL]
```

Now generate the complete master question list and provide it as a downloadable Markdown file.
