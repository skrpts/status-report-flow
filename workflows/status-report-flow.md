---
type: workflow
id: status-report-flow
title: Status Report Flow
description: "Gathers data, analyses progress, and produces stakeholder updates"
tags: [Production, Customer-Facing]
connections:
  - target: progress-tracking
    type: uses
  - target: stakeholder-communication
    type: uses
  - target: track-progress
    type: uses
  - target: craft-stakeholder-update
    type: uses
  - target: stakeholder-update-email
    type: uses
---

## Overview

This workflow collects project data, analyses progress against milestones, and produces tailored status updates for different stakeholder audiences.

## Pipeline Stages

### Stage 1: Data Gathering

Invoke the **progress-tracking** skill to synthesise velocity, burndown, and milestone data from the project management tooling.

### Stage 2: Progress Analysis

Invoke the **track-progress** prompt to analyse gathered data and identify trends, risks, and highlights worth reporting.

### Stage 3: Stakeholder Update

Invoke the **stakeholder-communication** skill to tailor the update for different audience levels (executive, team lead, team member).

### Stage 4: Email Generation

Invoke the **stakeholder-update-email** prompt to produce a polished, ready-to-send status update email.

## Output

Stakeholder-appropriate status updates containing:

- Progress summary against sprint and project milestones
- Key achievements and blockers
- Risk flags with mitigation actions
- Next steps and upcoming milestones
