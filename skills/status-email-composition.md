---
type: skill
id: status-email-composition
title: Status Email Composition
description: "Turning a status update into a formatted stakeholder email that leads with what the reader must know and states what is being asked of them"
tags: [Production, Communication]
connections:
  - target: llm-service
    type: runs_on
metadata:
  estimated_duration: "2-4 minutes"
  avg_tokens: 2000
  trigger: manual
---

## Status Email Composition

A status update and a status email are different artefacts. The update is a record; the email is a request for a reader's attention, and it competes with everything else in their inbox. This skill performs that conversion.

### Core Capabilities

#### Subject Lines That Survive a Crowded Inbox

The subject line must say what changed, not which document this is. "Project Atlas: launch slips to 14 November, decision needed on scope" is a subject line; "Weekly status update" is a filing label. Where there is a decision to be made, the subject says so, because that is what determines whether the mail is opened today or on Friday.

#### Inverted Structure

Readers of status mail read the first two lines and skim the rest. Order the content accordingly:

1. **The headline** — the single most important change since the last update
2. **Decisions needed**, each with who is being asked and by when
3. **Progress**, briefly, against what was promised
4. **Risks**, with what is being done about each
5. **Detail**, last, for the reader who wants it

#### Asking Clearly

A request buried in a paragraph of context will not be actioned. Every ask names the person or role, the decision, and the date by which it is needed. Where an ask has no owner in the supplied material, surface that gap rather than addressing the request to nobody.

#### Register

Status mail is read by people who did not attend the meeting. Expand first use of an acronym, avoid internal shorthand, and never report a slip in language that obscures it — a reader who discovers the delay in the fourth paragraph trusts the next email less.

#### Output Standards

- A subject line stating the change
- A greeting and a closing appropriate to the audience
- The body in the order above, with decisions near the top
- Clear signalling of any attachment or linked document the mail refers to
- An explicit note where the source update lacked something the email would normally carry, such as a date for a named decision

### Constraints

- Never soften a slipped date or an unmet target. The email reports the status it was given.
- Never introduce progress, commitments or dates absent from the source update.
- Never leave an ask without a named owner and a date where the source supplies them; where it does not, say what is missing.
