# What you don't know CAN hurt you.

*A map of one GoHighLevel account, for the person who inherits it.*

---

## What this is

You have just taken over Safe Harbor's Parent Intake account in GoHighLevel.
Somebody has asked you to change something — the timing on some texts, a
booking link, what happens when a new lead comes in. You open the account and
there are more names on the screen than you expected. Several of them look
almost the same. The person who knew which was which is not here to ask.

This folder is a map of that account. It tells you what is in there, where to
find it, what happens when it runs, and — this is the part that matters — what
is sitting next to it that you might grab by mistake. Somebody walked the
account and wrote down what they saw. The map has no login. It cannot open
anything for you and it cannot change anything. It points at a screen. You go
and look at that screen yourself.

---

## How to use it

**Open `catalog.md`. It sends you to ONE card. Open that card. Then stop.**

Two hops. That is the whole thing.

Do not open a second card. Do not read the other cards for background. Do not
ask for a summary of the folder.

Here is why. When you read all of it, every name starts to feel equally close.
Feeling equally close to all of them is exactly how somebody changes the
workflow *next to* the one they meant. That mistake is the reason this folder
exists. Reading everything puts the mistake right back.

After the card, close the folder. Open the real thing in the account.

---

## What's inside

```
map/
├── README.md                  Start here once you are inside the folder.
├── identity.md                What this map is, and what it refuses to do. ~2 min
├── rules.md                   What the marks mean. What VERIFY means. ~3 min
├── catalog.md                 The front door. Find your sentence. It names one card.
├── objects/                   One card per object somebody walked. Eight of them.
│                              The catalog tells you which single one to open.
└── reference/
    └── collisions.md          Every lookalike pair in one table. Off the path.
                               Your lane in the catalog already covers your object.
```

**`receipts/` is not part of the map.** It sits at the top of this repository,
outside `map/`. It holds the dated record of who checked what, and when, and
what turned out to be wrong. You do not need it to use the map. If you were
handed the map, you were not handed the receipts.

---

## What this map does not do

- **It does not tell you how to build anything.** There are no build steps in it.
- **It does not tell you how to fix anything.** There are no repair steps either.
- **It does not say anything is broken, messy, or badly named.** It has no opinion.
- **It is a snapshot, not a live mirror.** It was drawn on August 17–18, 2026, and
  checked against the live account on August 21, 2026, using a walk done on
  August 19, 2026 by Sadie, the VA who works inside the account. Every card
  carries its own date. That date is the last day somebody looked at that
  particular thing.
- **It is not finished.** Two workflows are switched on in the account and have no
  card yet: `SH - Fit Call Nurture Trigger (24hr Check)` and
  `VAPI Transcript to Apollo`. Both are named in `catalog.md`, so you know they
  are there. Nobody has walked either one.
- **Some lines say `VERIFY`.** That means nobody could confirm that line. It does
  not mean something is wrong. `rules.md` explains it in about three minutes, and
  it is worth the three minutes before you change anything.

**When the map and the account disagree, the account is right. Every time.** The
map can be out of date. The account cannot.

---

## How a card is read

Somebody says: **"Change the timing on the Fit Call nurture texts."**

**Hop 1 — open `catalog.md`.** Look down the page for the sentence closest to
the one you were handed. It is there, in Lane B. Lane B names one object and
points at one card.

**Hop 2 — open `objects/sh-fit-call-nurture-alt-days.md`.** That card tells you:

- the full name is `SH - Fit Call Nurture (Alt Days)` — brackets included
- it sends 15 texts, 2 days apart
- what else moves if you change the spacing
- and a warning: **don't search `nurture`.** Five things come back. Three of them
  send texts.

**Stop there.** Close the folder. Open `Automation → Workflows` in the account
and read the name at the top of the screen before you touch anything.

That is two hops. You did not open a second card. You did not need to.

---

## Setup

Before you drop `map/` into a Claude project:

1. **Add the `map/` folder. Only that folder.**
2. **Leave `receipts/` out.** It is not part of the map.
3. **When you ask your first question, say this:** *read `catalog.md` first, then
   open the one card it names.* Do not ask it to read every file. Do not ask it
   to summarise the folder.

---

## How to check this map is true

Every correction to this map is written down in `receipts/`, with the date and
the name of whoever settled it. The method for testing it — `TEST_METHOD.md`, at
the top of this repository — was written and locked on August 17, 2026, before
anybody ran a single test. Sadie walked the account on August 19 and found nine
things the map had wrong. All nine are still in the receipts, along with
everything found since, because a map that shows you where it was wrong is worth
more than one that only shows you where it was right.

---

# What you don't know CAN hurt you.
