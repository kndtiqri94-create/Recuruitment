---
title: Role Tracker — Product Brief
status: draft
created: 2026-08-13
updated: 2026-08-13
---

# Product Brief: Role Tracker (working name)

## Executive Summary

A client's recruiting team currently tracks open roles in a shared spreadsheet, and it's breaking down: the same role gets posted more than once, and nobody has a reliable answer to "what's actually still open?" This brief scopes a small, standalone web app that replaces the spreadsheet with one shared view — recruiters post a role, mark it filled when it's done, edit it as it changes, and search or filter to find what they need. There's no ambition here beyond that: this is a test to see whether solving this one specific pain is worth building further, not a platform pitch. [ASSUMPTION] Success for this phase is defined narrowly — the client seeing enough value to agree to pay for a real build — so the brief stays deliberately lean rather than investor-grade.

## The Problem

The recruiting team's system of record is a spreadsheet, shared across the team. In practice this produces two recurring failures:

- **Duplicate postings** — more than one recruiter posts the same role, likely because there's no single place to check "has this already been posted?" before adding a new row.
- **Stale/unclear status** — there's no reliable way to tell which roles are still open versus filled, so the spreadsheet accumulates rows nobody trusts.

[ASSUMPTION] The team copes today by manually scanning the sheet and likely relying on tribal knowledge or side conversations (Slack, email) to catch duplicates and closures — a coping mechanism that breaks down as the sheet grows or as recruiters are heads-down on their own work. The cost of the status quo is wasted recruiter time, and — more importantly for this test — client confidence in the team's ability to run a clean process.

## The Solution

A standalone web app, shared across the recruiting team (one team view, not siloed per-recruiter accounts), that lets a recruiter:

- **Post** a new open role.
- **Edit** a posted role as details change.
- **Mark a role filled/closed** so it drops out of the "live" view.
- **Search/filter** roles (e.g., by department, location, or status) to quickly answer "is this already posted?" and "what's open right now?"

The core outcome: one shared, trustworthy view of what's live, replacing the spreadsheet's guesswork with a single source of truth.

[ASSUMPTION] "Shared team view" means all recruiters see and can act on all roles (no per-recruiter ownership/permissions layer) — this keeps the first version simple, but should be confirmed with the client before build, since it affects who can edit or close someone else's posting.

## Who This Serves

**Primary users:** the client's recruiters, a small internal team currently coordinating through a shared spreadsheet. They need to post roles quickly, trust that what they see is current, and avoid the embarrassment/waste of double-posting. Success for them looks like: opening the app and knowing, without cross-checking, what's open and what isn't.

[ASSUMPTION] Team size and volume of roles are currently unknown — these affect how much search/filtering sophistication is actually needed for v1, and should be confirmed early since they weren't part of this discovery.

## Success Criteria

This is an early-stage test, not a committed build. The defining success signal:

- **The client agrees to pay for a real build.** Everything else is in service of getting there.

Supporting signals worth watching once something is in front of the recruiters:
- Recruiters actually use it instead of falling back to the spreadsheet.
- Duplicate postings visibly stop happening.
- Recruiters can answer "is this role still open?" without asking a colleague.

## Scope

**In (v1):**
- Post a role
- Edit a role
- Mark a role filled/closed
- View live (open) roles
- Search/filter roles

**Out (for now):**
- Multi-client / multi-tenant support — this is scoped to one client's team
- Per-recruiter accounts, permissions, or ownership of roles
- Integration with an ATS, job boards, or other external systems
- Analytics/reporting beyond the live-roles view

## Open Questions

Flagged honestly rather than papered over, since this is a test-the-idea phase:

- What does the client actually mean by "simple"? Not yet validated with the recruiters directly.
- How many recruiters, and how many roles at a time? Affects whether search/filter needs to be more than basic.
- Should any recruiter be able to edit/close any role, or does ownership matter once real usage starts?
- No existing source material (spreadsheet, recruiter interviews) was reviewed for this brief — it's built from Knd's working knowledge of the situation. Worth validating against the actual spreadsheet or a recruiter conversation before committing to build.
