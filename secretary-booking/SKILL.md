---
name: Secretary booking
description: >-
  Use when proposing or booking a meeting for the user, answering an
  availability request from another bot or an outside person, or placing a
  meeting on the calendar after the user already showed interest.
---
# Secretary booking

## Owner
Personal Secretary owns availability checks and meeting-time suggestions for the user. Other assistants hand this work to Personal Secretary instead of proposing times themselves, except when they are only forwarding a request.

## When to suggest times automatically
If another bot or an outside person wants to book the user, and the user already showed interest in having that meeting (they said they wanted it, asked to meet, or accepted the idea), Personal Secretary should automatically suggest concrete times. Do not ask the user to invent slots or to assign this work.

If the user has not shown interest yet, treat it as a new commitment: do not send times to the other person without the user. You may prepare suggested slots for the user to approve.

## Before suggesting or booking
1. Check every calendar used for the user's availability (typically both work/university and personal calendars when they have more than one).
2. Read what is already on those days: times, locations, and whether events are in-person or remote.
3. Note the requested meeting's location (a place, an area or campus, or video).
4. Note the user's location just before and after each candidate slot, from adjacent events that day.

## Travel time
Do not place an in-person meeting so close to another in-person event that the user cannot move between them. Leave enough travel time based on the two locations (walking, cycling, or transit as fits the distance). Remote-to-remote meetings can sit closer together. If a location is unknown, leave a modest buffer and say so.

## Cluster same-location events
When ranking slots, prefer times that put events near each other at the same location or in the same area on the same day — for example two campus meetings close together, rather than splitting the day with a long trip in between. Do not skip travel time just to cluster. Do not move an existing event other people are on in order to cluster, unless the user asked.

## How to propose
- Offer a few concrete slots in the user's timezone, not an open "whenever works."
- Prefer the user's known time-of-day preferences when they exist.
- Follow the scheduling skill for calendar writes, invites, and any message to another person. Draft external messages unless a standing rule already allows sending.

## After a time is agreed
Add or update the calendar event with the correct department colour. If a later message changes the time, place, or video link, update the event. If it is cancelled, update the calendar and send the user only a one-line FYI.
