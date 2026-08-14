---
title: Project Contacts
created: 2026-08-14
---

# Contacts

One [vCard](https://en.wikipedia.org/wiki/VCard) per person, in a
fenced `vcard` code block (RFC 6350, version 4.0) — human-readable on
GitHub as-is, and directly extractable into a `.vcf` file for import
into any contacts app (each block is already valid standalone vCard
text; concatenating them is a valid multi-contact `.vcf`).

Two sections: the confirmed program team, and prospective/stakeholder
contacts that already have real dial-in info recorded. For
stakeholders, [`Stakeholder-Notes.md`](./Stakeholder-Notes.md) stays
the source of truth for research and outreach status — this file only
centralizes the actual email/phone/address, kept in sync with it, and
only includes a stakeholder once real contact info exists (not every
named-but-uncontacted lead belongs here).

## Confirmed program team

Source of truth: [`Admin-Business-Legal.md` §4](./Admin-Business-Legal.md#4-team-roster-vsu-contacts--regional-focus)
— update there first if a role/entity changes, then mirror it here.

```vcard
BEGIN:VCARD
VERSION:4.0
FN:Javon Guerrier
ORG:Builder Tech LLC
TITLE:Program Director; Operations; Business Intelligence & Design Instruction & Curriculum
EMAIL:main@buildertech.com
NOTE:Instructor. Presence: In-Person/Online.
END:VCARD
```

```vcard
BEGIN:VCARD
VERSION:4.0
FN:Dr. Shawn Nicholson
ORG:Dr. Shawn M. Nicholson LLC
TITLE:Operations Director & Institutional Liaison (to VSU)
EMAIL:drshawnmnicholson@gmail.com
NOTE:Not an instructor. Engaged via his own LLC, not VSU employment.
END:VCARD
```

```vcard
BEGIN:VCARD
VERSION:4.0
FN:Emanuel Perez
ORG:Explay
TITLE:Program Design; Entrepreneurship & Innovation Instruction & Curriculum
EMAIL:emanuel.perez.va@gmail.com
NOTE:Instructor. Presence: Online Only.
END:VCARD
```

```vcard
BEGIN:VCARD
VERSION:4.0
FN:Andrew Foulks
ORG:VoltPop LLC
TITLE:Computer Science SME; Engineering & Computer Science Instruction & Curriculum
EMAIL:dfoulks@voltpop.com
NOTE:Instructor. Presence: In-Person/Online.
END:VCARD
```

## Stakeholder contacts (prospective — not yet engaged as team members)

```vcard
BEGIN:VCARD
VERSION:4.0
FN:Dr. Joon-Suk Lee
ORG:Virginia State University;Computer Science Department
TITLE:Department Chair
EMAIL:jlee@vsu.edu
NOTE:Potential champion contact on the CoET/CS side — not yet engaged (Stakeholder-Notes.md, 2026-08-13).
END:VCARD
```

```vcard
BEGIN:VCARD
VERSION:4.0
KIND:org
FN:Siemens — Newport News Office
ORG:Siemens
TEL:+1-757-591-6600
NOTE:Ask for the Academic Programs Coordinator (name not yet known). Fallback/parallel path to Gail Norris (Sitrain US Lead) via VSU's Engineering Industry Advisory Council (Stakeholder-Notes.md).
END:VCARD
```

```vcard
BEGIN:VCARD
VERSION:4.0
KIND:org
FN:Siemens Foundation
ORG:Siemens
EMAIL:foundation.us@siemens.com
TEL:+1-732-906-3809
ADR:;;200 Wood Ave. South;Iselin;NJ;08830;USA
NOTE:National Foundation contact — lower-priority path; relationship-first funder, not a cold-submit target (Stakeholder-Notes.md).
END:VCARD
```

```vcard
BEGIN:VCARD
VERSION:4.0
KIND:org
FN:Jabil Cares Foundation
ORG:Jabil
TEL:+1-727-803-5988
ADR:;;10800 Roosevelt Boulevard North;St. Petersburg;FL;33716;USA
NOTE:Invitation-only — does not accept unsolicited proposals. Local Petersburg, VA site leadership is the stronger path (Stakeholder-Notes.md).
END:VCARD
```
