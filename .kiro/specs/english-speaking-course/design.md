# Design — English Speaking Course for Hindi Speakers

## Overview

The course is delivered as a collection of Markdown files in the repository.
This keeps it readable on GitHub today, printable, and easy to convert into a
web app or PDF later. The learning design follows a simple principle:
**input → practice out loud → self-correct → repeat daily.**

The content is deliberately light on grammar theory and heavy on usable spoken
phrases, because the learner's goal is *fluency and confidence in speaking*, not
passing a grammar exam.

## Architecture

### Content structure (folder layout)

```
englishspeaking/
├── README.md                      # Entry point + table of contents
├── 00-start-here.md               # How to use this course + daily routine
├── levels/
│   ├── a2-foundation/             # Rebuild a solid base
│   │   ├── 01-greetings-introductions.md
│   │   ├── 02-daily-routine.md
│   │   └── self-check.md
│   ├── b1-conversation/           # Real everyday conversations
│   │   ├── 01-shopping.md
│   │   ├── 02-phone-calls.md
│   │   ├── 03-restaurant.md
│   │   ├── 04-travel.md
│   │   └── self-check.md
│   └── b2-fluency/                # Opinions, work, storytelling
│       ├── 01-workplace.md
│       ├── 02-giving-opinions.md
│       ├── 03-small-talk.md
│       └── self-check.md
├── reference/
│   ├── common-mistakes-hindi-speakers.md
│   ├── pronunciation-guide.md
│   └── useful-phrases-cheatsheet.md
├── practice/
│   ├── 30-day-tracker.md
│   └── daily-speaking-prompts.md
└── .kiro/specs/english-speaking-course/   # This spec
```

### Lesson template (consistent across all lessons)

Every lesson file uses the same sections so the learner always knows what to expect:

1. **🎯 Goal** — one line: what you will be able to say after this lesson.
2. **📖 Words & phrases** — a small vocabulary table (English | meaning/Hindi hint | example).
3. **💬 Dialogue** — a natural spoken conversation.
4. **🔑 Key phrases to reuse** — reusable chunks.
5. **🗣️ Say it out loud** — a drill: sentences to repeat / blanks to fill.
6. **⚠️ Watch out** — the specific Hindi-speaker mistake relevant to this lesson.
7. **➡️ Next** — link to the next lesson.

## Components and Interfaces

Since this is a content project (not software), the "components" are content modules
and how they link together.

| Component | Responsibility | Links to |
|-----------|----------------|----------|
| `README.md` | Front door; table of contents | all sections |
| `00-start-here.md` | Onboarding + daily routine | levels, tracker |
| Level folders | Progressive lessons | next lesson, reference, self-check |
| `reference/` | Lookup material (mistakes, pronunciation, cheatsheet) | linked from lessons |
| `practice/` | Daily habit tools (tracker, prompts) | start-here |

### Navigation flow

```
README → 00-start-here → A2 lessons → A2 self-check
       → B1 lessons → B1 self-check
       → B2 lessons → B2 self-check
Reference + Practice are available at any time (linked from each lesson).
```

## Data Models

The only structured "data" is the vocabulary/phrase table and the tracker.

**Vocabulary row**
```
| English phrase | Meaning (Hindi hint) | Example sentence |
```

**Mistake entry**
```
❌ Incorrect: <wrong form>
✅ Correct:   <right form>
Why: <one-line reason>
```

**Tracker row**
```
| Day | Date | Lesson done | Spoke out loud (min) | ✓ |
```

## Error Handling

Not applicable in the software sense. The content equivalent is **mistake handling**:
- Each lesson's "⚠️ Watch out" box catches the common error for that topic.
- `reference/common-mistakes-hindi-speakers.md` is the central correction list.
- The self-check pages tell the learner how to notice and fix their own errors
  (record → listen → compare → redo).

## Testing Strategy

Because this is learning content, "testing" means verifying usefulness and correctness:

1. **Link check** — every lesson's `Next` and `README` link resolves to a real file.
2. **Template check** — every lesson has all 7 template sections.
3. **Content accuracy** — English examples are natural and grammatically correct;
   Hindi hints are accurate transliterations/meanings.
4. **Self-check coverage** — each level has a `self-check.md`.
5. (Future) If converted to a web app, add automated link-checking in CI.

## Decisions & Rationale

- **Markdown over an app first:** fastest to read/review on GitHub, zero setup for
  the learner, easy to evolve. A web app can wrap this content later.
- **Speaking-first, grammar-light:** matches the learner's stated goal (fluent speaking),
  avoids the over-grammar trap common in Indian English education.
- **Hindi hints included:** lowers friction for a post-beginner Hindi speaker without
  turning the course into a translation exercise.
- **CEFR-style levels (A2/B1/B2):** gives a recognizable progression and a sense of achievement.
