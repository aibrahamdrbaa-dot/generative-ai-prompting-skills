---
name: personality-gate
description: Prevents accidental personality typing by requiring an explicit trigger before personality-analysis skills enter Roy's active context.
---

# Personality Gate

This gate protects the default Roy workflow from unsolicited personality typing.

## Before loading personality skills

Confirm at least one:
- explicit request for a personality test
- explicit request for personality analysis
- supplied assessment result that must be interpreted
- explicit request to adapt communication based on an existing personality result

## Reject activation when

The only evidence is:
- word choice
- mood
- a few past messages
- disagreement/agreement with Roy
- a user's occupation
- a single behavioral anecdote

## Persistence

Do not store an inferred personality type in Supermemory.

A durable personality fact may be stored only when:
1. the user explicitly confirms it, AND
2. the exact framework/instrument is known, AND
3. the stored statement is narrowly scoped.

Example:
"User reported MBTI result = INTP from [instrument/version], self-reported on [date]."

Never store:
"User is an INTP, therefore he thinks this way."

## Off switch

When the personality task ends, unload the personality subsystem from active reasoning and return to normal Roy routing.
