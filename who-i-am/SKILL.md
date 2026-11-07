---
name: Who I am
description: >-
  Use this when you need a current picture of who the user is and their present
  status — before a prize, funding, eligibility, or similar search cycle, and
  before any task that depends on student status, affiliations, leave, roles, or
  what they can apply for. Bots that regularly need background (such as a prize
  scout) must run this at the start of each cycle, before searching.
---
# Who I am

Build a fresh snapshot of the user's current status. Do not rely only on old memory. Do not contact external people, apply for anything, or act on a status change unless the user asked for that action in this conversation.

## When this runs
- At the start of any regular search or watch cycle that depends on who the user is now (prize, award, funding, eligibility, partnership screening).
- Before a one-off task that needs current student status, affiliations, leave, roles, or what they can apply for.
- Run this **before** searching or shortlisting. The search uses the snapshot; it does not replace it.

## 1. Lasting facts
Search durable memory for profile facts: name, location, institutions, roles, leave or family status, degrees in progress, and known gaps (for example nationality or enrolment that has never been confirmed). Treat memory as a starting point, not as proof that nothing has changed.

## 2. Both email inboxes
Read recent mail in **both** of the user's addresses:
- Personal Gmail (typically `tongshl0527@gmail.com`, via the Gmail connector).
- Cambridge university email (typically `st883@cam.ac.uk`, via Cambridge Outlook).

Confirm the current addresses from memory or the vault if they may have changed. Search for status-changing threads from about the last 30 days, plus any older open threads memory already flags (student registry, admissions, enrolment, leave, internships, exams, funding, society memberships).

If a mailbox is not connected or returns an auth error, record that as a gap. Do not invent what that inbox contains, and do not switch to the browser to bypass a broken connector.

## 3. Other messages
- Recent messages that change plans or status, including WhatsApp. WhatsApp is read and sent through Personal Secretary; ask that bot rather than opening WhatsApp yourself.
- Do not attempt to read every message the user has ever sent. Aim for what would change a status snapshot today.

## 4. Department managers
Ask all current department managers for anything that has changed since the last snapshot, labelled as something the user told them versus inferred:
- Chief of Staff
- Personal Life Manager
- IFMSA SCOME Manager
- FirstAid Startup Manager

Look up their current teammate ids rather than hard-coding old ones. Ask about student status and leave, institutional enrolment, roles and titles they prefer, society memberships, prizes already won or applied for, and any constraint (exam freeze, wording rules, legal entity status) that would change eligibility. Do not contact other specialist bots unless a department manager points to a fact only they hold.

## 5. Write the snapshot
Produce a short dated brief with each point labelled **TOLD** (the user said it, or a record that was opened) or **INFERRED**. Include:
- Who they are right now: roles, institutions, where they live and work.
- Student and registration status (each university separately), leave, and any end dates.
- Work in progress that affects eligibility (research, education projects, association roles, startups), with approved public wording if one exists.
- Memberships and affiliations that are confirmed versus only possible.
- Upcoming dates that change what they can do (exams, freezes, admission windows).
- Open questions and missing sources (unconnected inbox, unconfirmed enrolment, unknown nationality).

Never present an inferred point as a confirmed fact. Never treat another bot's guess as the user's word.

## 6. After the snapshot
- Use it immediately for the task that triggered this skill (for example a prize search).
- If the snapshot is for a prize or funding cycle, follow the Prize and funding watch skill next: search only after this brief exists, then send structured finds to Chief of Staff.
- Save lasting new facts to memory only when they are clearly about the user and useful across assistants. Do not store private addresses, phone numbers, or secrets in the snapshot or in memory; those stay in the vault.
