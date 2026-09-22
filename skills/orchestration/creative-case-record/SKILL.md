---
name: creative-case-record
description: Records reusable lessons from an image or video generation case so successful workflows can be reproduced and failures can be diagnosed.
---

# Creative Case Record

Use for non-trivial jobs or experiments that are likely to be repeated.

## Record

- intent
- modality and operation
- selected model/variant
- skill stack
- references and their roles
- key prompt decisions
- output version
- observed failures
- corrections
- final result status
- reusable lesson

## Versioning

Use sequential output versions such as v1, v2, v3.

Do not replace the original case record merely because v2 is better. The comparison between attempts is part of the learning signal.

## Reusable lesson rule

Write a lesson in the form:
When [task pattern], use [skill/model decision] because [verified reason]. Avoid [failure mode].

Only promote the lesson to Supermemory after the Memory Router criteria are met.

## Stop condition

A case is complete when:
- the requested deliverable is accepted, or
- the provider/tool limitation is clearly identified and documented.
