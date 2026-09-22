---
name: personality-gate
description: Hard activation gate that prevents accidental personality typing and prevents personality skills from entering unrelated Roy workflows.
---

# Personality Gate

This gate runs before any personality skill is loaded.

## Activation allowed only when

At least one is explicit:
- the user asks for a personality test;
- the user asks for personality/behavior analysis;
- the user supplies a personality assessment result and asks for interpretation;
- the user explicitly asks Roy to adapt communication/workflow based on an existing personality result.

## Activation denied when the only evidence is

- word choice
- mood
- a few past messages
- occupation
- behavior in one anecdote
- agreement/disagreement with Roy
- Roy's intuition that a type fits

## Isolation

Personality skills are not visual-generation skills.

A visual task must not activate them.

A study, coding, marketing, writing, or planning task must not activate them unless personality analysis is explicitly part of the request.

## Exit condition

After the requested personality task is complete:
- stop using the personality subsystem;
- do not keep its framework assumptions active for unrelated tasks;
- do not turn the result into hidden personalization.

## Persistence rule

Never store an inferred type.

A stored personality fact must be:
- explicitly user-confirmed;
- tied to a known framework/instrument;
- narrow in scope;
- clearly marked as self-report where applicable.
