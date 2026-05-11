---
name: software-project-planner
description: Research-first software project planning workflow. Use when a user wants to start, scope, plan, or decompose a new software app/project from a high-level idea; gather requirements interactively; perform market, product, technical, or best-practice research; define capabilities, work packages, GitHub issues, task breakdowns, architecture options, MVP scope, acceptance criteria, or a multi-agent Codex implementation plan.
---

# Software Project Planner

Use this skill to guide a new software project from a rough idea to a documented, implementation-ready plan. Move in phases: research, synthesis, interactive requirements, categorization, capability mapping, work packages, task issues, and approval gates.

## Core Workflow

1. Clarify only what blocks useful research.
   If the idea is understandable, state assumptions and begin. Ask a brief clarifying question only when the domain, audience, or project type is too ambiguous to research responsibly.

2. Research the space before requirements gathering.
   Search current sources when the user asks for a new app, product, or domain where market norms, tools, laws, best practices, competitors, APIs, or technical options may have changed. Look for existing products, user expectations, common capabilities, technical approaches, design patterns, opportunity gaps, risks, and relevant constraints. Cite sources when browsing is used.

3. Synthesize findings into a short discovery brief.
   Cover what exists, common user personas, common workflows, baseline capabilities, differentiated opportunities, architecture options, risks, assumptions, and open questions. Keep the synthesis actionable; do not bury the user in raw research.

4. Run interactive requirements gathering.
   Lead a structured Q&A. Ask a small batch of questions at a time, grouped by topic. Adapt based on the user's answers. Avoid dumping a huge questionnaire.

5. Maintain a living requirements summary.
   Track functional requirements, non-functional requirements, UX/design requirements, data requirements, integrations, security/privacy requirements, constraints, assumptions, decisions, open questions, and out-of-scope items.

6. Categorize requirements.
   Group requirements by project-relevant areas such as Frontend, Backend, UI/UX, Data, Security, Integrations, Testing, Deployment, Documentation, Operations, Analytics, or Admin.

7. Map requirements to capabilities.
   Convert requirements into coherent user-facing or system-facing capabilities. Name each capability clearly and explain the requirement(s) it satisfies.

8. Define MVP and later scope.
   Separate must-have first release work from enhancements. Call out decisions that materially affect timeline, risk, or architecture.

9. Group capabilities into work packages.
   A work package is a meaningful chunk of related work, usually too large for one Worker agent branch. It should map to a GitHub issue when using issue-based coordination.

10. Break work packages into task issues.
   A task is one Worker-agent-sized unit of work: claimable, branchable, testable, and suitable for one pull request. Use subtasks only as checklist items inside a task issue.

11. Propose architecture and design approach.
   Recommend a stack, system structure, data model, integration approach, testing strategy, deployment path, and major tradeoffs. Prefer established patterns and existing project conventions when a repo already exists.

12. Add approval gates before implementation.
   Pause for user approval after research synthesis, after requirements consolidation, and before creating implementation tasks or starting code.

## Interactive Requirements Topics

Use the relevant topics for the project, not all topics every time:

- Users and stakeholders
- Primary jobs to be done
- Core workflows
- Must-have features
- Nice-to-have features
- MVP boundary
- UI/UX style and accessibility
- Data model and data sources
- Integrations and APIs
- Authentication, authorization, privacy, and security
- Admin, operations, and observability
- Performance, reliability, and scalability
- Compliance or domain constraints
- Platform, hosting, and deployment
- Testing and quality expectations
- Timeline, budget, and technical preferences
- Out-of-scope items

## Recommended Artifacts

Produce these artifacts as the project matures:

- Research brief
- Requirements summary
- Assumptions log
- Decision log
- Open questions list
- Out-of-scope list
- Capability map
- MVP vs later scope
- Risk register
- Architecture proposal
- Work package list
- Task issue breakdown
- Acceptance criteria
- Verification plan

## GitHub Issue Hierarchy

When the project uses GitHub for coordination, use this hierarchy:

```text
Project
  -> Requirements / Capabilities
      -> Work Packages
          -> Tasks
              -> Subtasks
                  -> Pull Requests / Commits
```

Map it to GitHub like this:

```text
Repository or GitHub Project
  -> Master Project Issue
      -> Requirement Areas
          -> Work Package Issues
              -> Task Issues
                  -> PRs / Branches / Commits
```

Use these rules:

- Put durable context in the master project issue.
- Put major capability groups in work package issues.
- Put Worker-agent-sized implementation units in task issues.
- Put small implementation steps in task issue checklists.
- Link each task issue to its parent work package and master project issue.
- Link each PR to the task issue it completes.

## Multi-Agent Planning Rules

When planning for multiple Codex agents:

- Treat task issues as the normal Worker ownership unit.
- Keep each task independently branchable and reviewable.
- Make dependencies explicit.
- Avoid tasks that require multiple agents to edit the same files at the same time.
- Include suggested files/areas, acceptance criteria, and verification steps in each task.
- Add status/claim conventions when GitHub Issues are the coordination board.
- Include an Integrator/reviewer role before merging parallel work.

## Output Style

During discovery, be conversational and iterative. During documentation, be structured and precise. Prefer concise tables or grouped bullets for requirements and capabilities. Do not start implementation until the user has approved the requirements and planning direction, unless the user explicitly asks to proceed.
