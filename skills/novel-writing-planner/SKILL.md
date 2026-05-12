---
name: novel-writing-planner
description: Research-first novel planning and multi-agent writing workflow. Use when a user wants to develop, outline, draft-plan, revise, or coordinate a novel or long-form fiction project; create a story bible, character cast, world bible, plot architecture, chapter plan, scene tasks, continuity system, revision plan, or GitHub Issues hierarchy for multiple writing agents working on one manuscript.
---

# Novel Writing Planner

Use this skill to guide a novel from rough premise to coordinated drafting and revision. Move in phases: research, story discovery, foundation, architecture, chapter and scene planning, GitHub issue decomposition, drafting, continuity review, revision, and integration.

## Core Workflow

1. Clarify only what blocks useful story work.
   If the genre, premise, audience, or target format is understandable, state assumptions and begin. Ask a brief clarifying question only when the story direction is too ambiguous to research or plan responsibly.

2. Research before locking the foundation.
   Search current sources when the user asks for a new novel, genre, market category, setting, profession, historical period, scientific concept, cultural context, or publishing approach where norms or facts may have changed. Look for reader expectations, comparable titles, genre promises, tropes, structure conventions, content sensitivities, factual constraints, and opportunity gaps. Cite sources when browsing is used.

3. Synthesize findings into a short discovery brief.
   Cover genre/audience expectations, comparable works, reader promise, likely structure, useful tropes, risks, opportunities, research constraints, assumptions, and open creative questions. Keep the synthesis actionable.

4. Run interactive story development.
   Ask focused questions in small batches. Adapt based on the user's answers. Avoid dumping a giant questionnaire.

5. Maintain a living story foundation.
   Track premise, logline, genre, target reader, reader promise, themes, tone, POV/tense, setting, cast, plotlines, conflicts, stakes, constraints, decisions, assumptions, open questions, and out-of-scope items.

6. Build the story bible.
   Create or maintain the durable sources of truth: premise, characters, world/setting, timeline, canon, voice/style, unresolved threads, research notes, and continuity log. Treat canon as authoritative unless the human owner approves a change.

7. Map creative intent to story architecture.
   Convert the foundation into acts, arcs, plotlines, character arcs, beats, turns, setups/payoffs, mysteries/reveals, escalation, climax, and resolution. Name each arc clearly and explain the story purpose it serves.

8. Define draft scope.
   Separate first-draft must-haves from later enhancements. Call out decisions that materially affect structure, tone, audience, research, or parallel drafting risk.

9. Break architecture into chapters and scenes.
   Each chapter or scene should state POV, time, location, active characters, scene goal, conflict, emotional turn, plot turn/reveal, required canon, forbidden contradictions, dependencies, acceptance criteria, and expected story-bible updates.

10. Group work into agent-sized issues.
   Use arc, chapter, scene, research, continuity, revision, and editorial-review issues. A normal Writer agent ownership unit should be one scene issue, one small chapter issue, or one focused revision issue.

11. Add approval gates.
   Pause for user approval after research synthesis, after story foundation, after chapter/scene planning, and before creating GitHub issues or launching drafting agents unless the user explicitly asks to proceed.

## Interactive Story Topics

Use the relevant topics, not all topics every time:

- Genre, subgenre, and target reader
- Comparable titles and reader promise
- Premise, logline, hook, and central dramatic question
- Theme, emotional target, and boundaries
- Protagonist, antagonist, supporting cast, and relationships
- Character wants, needs, wounds, misbeliefs, secrets, and arcs
- Setting, world rules, institutions, culture, technology, history, or magic
- POV, tense, narrative distance, voice, and style
- Main plot, subplots, mysteries, reveals, and reversals
- Structure model, acts, beats, escalation, midpoint, climax, and ending
- Chapter rhythm, scene density, pacing, and word-count target
- Research needs, factual constraints, and sensitivity risks
- Continuity risks, timeline constraints, and character knowledge
- Drafting strategy, revision strategy, and publication goals
- Out-of-scope content, tropes to avoid, and hard constraints

## Recommended Artifacts

Produce these artifacts as the novel matures:

- Research brief
- Story foundation summary
- Story bible
- Character registry
- Relationship map
- World/setting bible
- Timeline
- Canon file
- Voice and style guide
- Plot architecture
- Arc map
- Chapter outline
- Scene list
- Setup/payoff ledger
- Unresolved threads list
- Continuity log
- Revision plan
- Editorial review notes
- GitHub issue breakdown

## GitHub Issue Hierarchy

When the novel uses GitHub for coordination, use this hierarchy:

```text
Novel
  -> Story Foundation / Story Bible
      -> Arcs / Plotlines
          -> Chapters
              -> Scenes
                  -> Drafts / Revisions / Pull Requests
```

Map it to GitHub like this:

```text
Repository or GitHub Project
  -> Master Novel Issue
      -> Foundation Issues
      -> Arc Issues
          -> Chapter Issues
              -> Scene Draft Issues / Revision Issues
                  -> PRs / Branches / Commits
```

Use these rules:

- Put durable shared context in the master novel issue.
- Put story-bible and canon work in foundation issues.
- Put major plotlines, acts, or character arcs in arc issues.
- Put chapter planning or chapter integration in chapter issues.
- Put Writer-agent-sized drafting units in scene issues.
- Put focused editorial passes in revision or editorial-review issues.
- Link each child issue to its parent issue and the master novel issue.
- Link each PR to the issue it completes.
- Keep canonical story facts in story-bible files, not only in transient issue comments.

For longer templates and startup prompts, read `references/github-novel-coordination.md`.

## Multi-Agent Writing Rules

When planning for multiple Codex agents:

- Treat scene issues or focused revision issues as the normal Writer ownership unit.
- Keep each issue independently branchable and reviewable.
- Make dependencies explicit, especially timeline order, prior reveals, character knowledge, and canon state.
- Avoid assigning multiple agents to rewrite the same manuscript passage at the same time.
- Include required canon, forbidden contradictions, acceptance criteria, and verification steps in each issue.
- Require claim comments before drafting begins.
- Require story-bible updates or proposed updates when new durable facts are introduced.
- Add a Continuity Editor role before large merges.
- Add an Integrating Editor role before merged prose becomes canonical.
- If drafting reveals a better story direction, propose a canon or outline change instead of silently mutating downstream chapters.

## Role Vocabulary

- Human Owner / Lead Author: owns creative vision, approvals, and final canon decisions.
- Story Architect: develops foundation, structure, arcs, chapter map, scene list, and issue breakdown.
- Writer Agent: drafts assigned scenes or chapters within scope.
- Character Steward: checks character motivation, arc, voice, relationships, and knowledge.
- World / Research Steward: checks setting, world rules, factual research, and domain constraints.
- Continuity Editor: checks canon, timeline, prior reveals, character knowledge, and contradictions.
- Voice Editor: checks POV, tense, diction, rhythm, tone, dialogue, and style guide adherence.
- Revision Editor: converts critique into focused rewrite issues.
- Integrating Editor: reviews PRs, protects the manuscript branch, updates parent issues, and keeps the story coherent.

## Terminology Mapping

Use this translation when adapting software multi-agent coordination habits to fiction:

```text
Project                 -> Novel
Requirements            -> Creative Intent / Story Requirements
Capabilities            -> Story Pillars / Narrative Functions
Work Packages           -> Arcs / Chapter Groups / Revision Passes
Tasks                   -> Chapter Issues / Scene Issues
Subtasks                -> Beat Checklist / Edit Checklist
Architecture            -> Story Architecture
Data Model              -> Canon / Story Bible / Timeline
Acceptance Criteria     -> Scene Success Criteria
Verification Plan       -> Editorial Review / Continuity Check
Integrator              -> Integrating Editor / Lead Author
```

## Output Style

During discovery, be conversational, curious, and generative. During planning and issue creation, be structured and precise. Prefer concise tables or grouped bullets for arcs, chapters, scenes, and responsibilities. Do not start drafting prose, creating GitHub issues, or launching agents until the user has approved the story foundation and planning direction unless the user explicitly asks to proceed.
