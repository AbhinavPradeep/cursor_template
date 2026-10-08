---
name: explain-artifact
description: Explain an existing engineering artifact in very plain language without redesigning or modifying the system.
disable-model-invocation: true
---

# Explain an engineering artifact plainly

Goal: help the user understand an existing artifact quickly and accurately.

Preserve the technical meaning, but explain it in the simplest language that
still remains correct.

Do not redesign, improve, or modify the underlying system unless explicitly asked.

Read the requested artifact and only the upstream artifacts needed to explain it.

## Style

- Use very plain language.
- Prefer short sentences.
- Explain one idea at a time.
- Avoid jargon where possible.
- When jargon is necessary, define it immediately in ordinary language.
- Do not assume the user remembers previous terminology.
- Do not compress several ideas into one dense sentence.
- Prefer concrete examples over abstract wording.
- Prefer "A calls B" over phrases like "A delegates responsibility to B".
- Prefer "B owns this state" over "B is the authoritative mutation boundary".
- Preserve important technical details rather than omitting them for simplicity.

The goal is:
**easy to understand, not dumbed down.**

## Procedure

1. Start with a very short summary:
   - what this artifact is;
   - what problem it is solving;
   - where it fits in the system.

2. Identify the few main ideas.
   Explain them in the order needed to understand the artifact.

3. For each component/concept, answer plainly:
   - What is it?
   - What does it do?
   - What does it talk to?
   - What state does it own, if any?
   - Why does it exist?

4. Prefer simple structured views:
   - small tables;
   - bullet trees;
   - numbered flows;
   - state-transition lists.

5. Use diagrams only when they make one specific idea easier to see.
   Keep diagrams small.
   Do not create a giant architecture diagram.

6. For an execution flow, explain:
   1. what starts it;
   2. what happens next;
   3. what state changes;
   4. what result is returned.

7. For a contract, explain:
   - who calls whom;
   - what goes in;
   - what comes back;
   - what can fail;
   - what is guaranteed.

8. For an invariant, explain:
   - what must always remain true;
   - what could break it;
   - which part of the system prevents that.

9. Clearly separate:
   - what the artifact explicitly says;
   - what is interpretation;
   - what remains ambiguous.

10. If the artifact is large, explain it in chunks rather than trying to
    summarize everything at once.

11. End with a short "mental model" section:
    summarize the artifact in the smallest useful picture or sequence.

## Constraints

- Do not modify project files unless explicitly requested.
- Do not redesign the system.
- Do not invent missing requirements.
- Do not launch subagents.
- Do not perform an independent review.
- Do not restate the whole artifact.
- Do not use dense academic or architecture-heavy prose.
- Do not introduce terminology before explaining the underlying idea.
- If a sentence can be made simpler without losing meaning, simplify it.