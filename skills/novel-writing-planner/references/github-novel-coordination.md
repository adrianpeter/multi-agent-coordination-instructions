# GitHub Novel Coordination Reference

Load this reference when the user wants GitHub-ready issue templates, role prompts, or multi-agent coordination details for a novel.

## Recommended Repository Structure

```text
/manuscript/
  chapter-01.md
  chapter-02.md

/story-bible/
  premise.md
  characters.md
  world.md
  timeline.md
  canon.md
  voice.md
  unresolved-threads.md

/research/
  genre.md
  setting.md
  domain-notes.md

/editorial/
  revision-plan.md
  continuity-log.md
  style-sheet.md
```

## Master Novel Issue

Suggested title:

```text
Novel brief: <working title>
```

Suggested body:

```md
# Novel Brief: <working title>

## Premise
<One-paragraph story idea.>

## Genre / Audience
<Genre, subgenre, target reader, comparable titles.>

## Reader Promise
<What emotional/narrative experience the book must deliver.>

## Creative Intent
<Themes, tone, boundaries, constraints, ambitions.>

## Story Foundation
- Logline:
- POV / tense:
- Setting:
- Core cast:
- Main conflict:
- Central stakes:
- Ending target, if known:

## Story Bible Links
- Characters:
- World:
- Timeline:
- Canon:
- Voice / style:
- Unresolved threads:

## Branch / PR Policy
Base branch: main
Branch naming: novel/<issue-number>-<short-slug>
Merge policy: pull request only
Canon policy: durable story facts must be reflected in the story bible

## Definition Of Done
- Assigned scene/chapter/revision scope is complete
- Continuity implications are noted
- Story bible updates are included or proposed
- PR links the issue
- No unrelated rewrites outside scope

## Arcs / Chapter Groups
- <Issue links go here after planning>

## Coordination Notes
<Anything future agents need to know.>
```

## Foundation Issue

```md
# Foundation: <name>

Master novel: #<master-issue>

## Goal
<What story-bible, research, canon, or setup artifact this issue establishes.>

## Scope
- <In-scope item>
- <In-scope item>

## Out Of Scope
- <Explicit non-goal>

## Artifacts
- `<story-bible/path.md>`
- `<research/path.md>`

## Acceptance Criteria
- <Observable completion condition>
- <Canon or story-bible update expectation>

## Notes For Agents
<Creative constraints, user decisions, risks, or dependencies.>
```

## Arc Issue

```md
# Arc: <name>

Master novel: #<master-issue>

## Story Function
<What this arc contributes to the novel.>

## Scope
- <Act, plotline, subplot, character arc, mystery thread, or thematic movement>

## Key Beats
- <Beat>
- <Beat>
- <Beat>

## Dependencies / Blockers
- Depends on: #<issue>
- Blocks: #<issue>

## Child Chapters / Scenes
- #<issue> Chapter: <name>
- #<issue> Scene: <name>

## Continuity Risks
- <Timeline, reveal, character knowledge, or canon risk>

## Acceptance Criteria
- <Arc planning condition>
- <Integration expectation>

## Notes For Agents
<Context future Story Architect, Writer, or Editor agents need.>
```

## Chapter Issue

```md
# Chapter: <number or title>

Master novel: #<master-issue>
Parent arc: #<arc-issue>

## Purpose
<What must change for the reader, plot, or character by the end of this chapter.>

## Summary
<Brief chapter plan.>

## Scenes
- #<scene-issue> Scene: <name>
- #<scene-issue> Scene: <name>

## Required Canon
- <Canon fact>

## Forbidden Contradictions
- <What must not change or contradict prior material>

## Acceptance Criteria
- <Chapter-level success condition>
- <Continuity expectation>

## Notes For Agents
<POV, pacing, tone, or dependencies.>
```

## Scene Issue

```md
# Scene: <name>

Master novel: #<master-issue>
Parent chapter: #<chapter-issue>
Parent arc: #<arc-issue>

## Goal
<One clear scene outcome.>

## Scene Contract
- POV:
- Time:
- Location:
- Characters present:
- Scene goal:
- Conflict:
- Emotional turn:
- Plot turn / reveal:
- Entry state:
- Exit state:

## Required Canon
- <Canon fact or story-bible link>

## Forbidden Contradictions
- <What not to alter, reveal early, or contradict>

## Scope
- <Specific drafting or rewrite scope>

## Out Of Scope
- <Other chapters/scenes/arcs not to touch>

## Suggested Files / Areas
- `manuscript/<file>.md`
- `story-bible/<file>.md`

## Acceptance Criteria
- <Observable scene condition>
- <Voice/POV condition>
- <Continuity condition>

## Verification
- Check against `story-bible/canon.md`
- Check against `story-bible/timeline.md`
- Check against `story-bible/voice.md`

## Expected Story-Bible Updates
- <Canon, timeline, character knowledge, unresolved thread, or none>

## Writer Notes
<Implementation hints, constraints, or known risks.>
```

## Revision Issue

```md
# Revision: <scope and pass type>

Master novel: #<master-issue>
Affected scope: <chapter/scene/range>

## Revision Goal
<What this pass improves.>

## Pass Type
<Structural | Character | Continuity | Voice | Pacing | Line Edit | Copy Edit>

## Scope
- <Specific edits allowed>

## Out Of Scope
- <What must not be rewritten>

## Source Notes
- <Critique, continuity issue, or editorial concern>

## Acceptance Criteria
- <Observable improvement>
- <Continuity preserved>

## Verification
- <Manual review or file checks>

## Notes For Agents
<Creative direction, constraints, risks.>
```

## Claim Comment

```md
Claimed by Codex thread <identifier>.

Branch: novel/<issue-number>-<slug>
Worktree: <local path if relevant>
Started: <date/time/timezone>

Scope:
- <scene/chapter/revision scope>

Plan:
- <step 1>
- <step 2>
- <step 3>

Canon files expected to touch:
- <file>
```

## Pull Request Body

```md
Fixes #<issue-number>

## Summary
- <What was drafted, revised, or updated>

## Story-Bible / Canon Updates
- <Canon, timeline, character knowledge, unresolved threads, or none>

## Continuity Checks
- <What was checked>

## Notes
- <Risks, assumptions, follow-up issues>
```

## Startup Prompts

### Story Architect

```md
You are the Story Architect for this novel.

Target repo: <owner/repo>
Master novel issue: #<number>

Read the master novel issue and existing story-bible files. Develop the story foundation into arcs, chapter groups, and scene-level issue candidates. Do not draft prose yet. Identify dependencies, continuity risks, open creative questions, and approval gates.
```

### Writer Agent

```md
You are a Writer agent for this novel.

Target repo: <owner/repo>
Master novel issue: #<number>
Assigned scene or chapter issue: #<number>

Read the master novel issue, relevant story-bible files, parent arc/chapter issue, and assigned issue. Claim the issue before editing. Draft only the assigned scope. Preserve canon, POV, tense, voice, and continuity. If the scene requires a canon change, flag it clearly and update or propose updates to the story bible.
```

### Continuity Editor

```md
You are the Continuity Editor for this novel.

Target repo: <owner/repo>
Master novel issue: #<number>
Scope: <chapter/arc/manuscript range>

Check the assigned manuscript scope against the story bible, canon, timeline, character knowledge, relationships, unresolved threads, and prior chapters. Create focused continuity issues or propose fixes. Do not rewrite prose unless explicitly assigned.
```

### Voice Editor

```md
You are the Voice Editor for this novel.

Target repo: <owner/repo>
Master novel issue: #<number>
Scope: <chapter/arc/manuscript range>

Review the assigned manuscript scope for POV discipline, tense consistency, diction, rhythm, tone, dialogue style, and adherence to the voice guide. Suggest or implement only focused edits within scope.
```

### Integrating Editor

```md
You are the Integrating Editor for this novel.

Target repo: <owner/repo>
Master novel issue: #<number>

Review open PRs and linked issues. Confirm each draft or revision satisfies its scene/chapter criteria, preserves canon, updates the story bible where needed, and does not create contradictions. Coordinate conflicts between agents and protect the main manuscript branch.
```
