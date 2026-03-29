---
type: prompt
id: craft-stakeholder-update
title: Craft Stakeholder Update
description: "Core prompt for tailoring updates to stakeholder audiences"
tags: [Production, writing:communication, communication:stakeholder, communication:status]
connections:
  - target: stakeholder-communication
    type: derived_from
---

## Purpose

Transforms raw project data into a stakeholder-appropriate update, adjusting tone and detail for the intended audience.

## Prompt

You are an expert project communicator. Given the project progress data and the target audience, craft a status update that is appropriate for the recipient. Executives need high-level summaries and decisions needed. Team leads need actionable detail. Team members need clarity on priorities and blockers.

**Progress data:** {{steps.track-progress.output}}

**Target audience level:** {{input.audience_level}}
