# Requirements — English Speaking Course for Hindi Speakers

## Introduction

This project is a self-paced English **speaking** course aimed at Hindi-native
learners who have already crossed the beginner level and now want to speak
English fluently and confidently. The focus is on *spoken* English — real
conversations, common mistakes Hindi speakers make, pronunciation, and daily
practice — rather than heavy grammar theory.

The deliverable is a structured, text-based course (Markdown) that can be read
on GitHub, printed, or later turned into a web app. It is organized so a learner
can practice a little every day.

## Glossary

- **Learner**: A Hindi-native speaker, post-beginner, wanting to improve spoken English.
- **Lesson**: A single focused unit (vocabulary, a conversation, a grammar point).
- **Drill**: A short repeat-after-me / fill-in practice exercise.
- **L1 interference**: Mistakes caused by translating directly from Hindi.

## Requirements

### Requirement 1 — Structured, progressive lessons
**User Story:** As a learner, I want lessons arranged from easier to harder, so that
I can build up my speaking skills step by step without feeling lost.

#### Acceptance Criteria
1. WHEN the learner opens the course THEN the system SHALL present a clear table of contents ordered from foundational to advanced topics.
2. WHEN the learner finishes a lesson THEN the system SHALL point to the next recommended lesson.
3. THE course SHALL group lessons into levels (e.g. A2 → B1 → B2).
4. EACH lesson SHALL state a clear learning goal at the top.

### Requirement 2 — Everyday conversation practice
**User Story:** As a learner, I want ready-made dialogues for real situations, so that
I can practise phrases I will actually use.

#### Acceptance Criteria
1. THE course SHALL include dialogues for at least these situations: introductions, shopping, phone calls, workplace/office, restaurants, and travel.
2. EACH dialogue SHALL use natural, spoken English (contractions like "I'm", "don't", "gonna" where appropriate).
3. EACH dialogue SHALL include a short list of key phrases the learner can reuse.
4. WHERE a phrase is commonly mistranslated from Hindi THE lesson SHALL show the natural English version.

### Requirement 3 — Common Hindi-speaker mistakes
**User Story:** As a learner, I want to see the specific mistakes Hindi speakers make, so that
I can stop making them.

#### Acceptance Criteria
1. THE course SHALL contain a dedicated section listing frequent L1-interference errors.
2. EACH error entry SHALL show the incorrect form, the correct form, and a one-line reason.
3. THE section SHALL cover at least: articles (a/an/the), tenses, prepositions, "since/for", direct translation, and word order.

### Requirement 4 — Pronunciation help
**User Story:** As a learner, I want simple pronunciation guidance, so that
people understand me clearly.

#### Acceptance Criteria
1. THE course SHALL explain sounds that are hard for Hindi speakers (e.g. v/w, th, silent letters, word stress).
2. PRONUNCIATION SHALL be written in a simple phonetic hint style (no requirement to read IPA), with IPA shown as optional extra.
3. EACH pronunciation point SHALL include example words.

### Requirement 5 — Daily practice routine
**User Story:** As a busy learner, I want a daily plan, so that
I can improve with a small, repeatable habit.

#### Acceptance Criteria
1. THE course SHALL provide a suggested daily routine that fits in about 20–30 minutes.
2. THE routine SHALL include speaking-out-loud activities, not only reading.
3. THE course SHALL provide a 30-day practice tracker the learner can tick off.

### Requirement 6 — Self-assessment and feedback
**User Story:** As a self-learner, I want to check my own progress, so that
I know I am improving.

#### Acceptance Criteria
1. EACH level SHALL end with a short self-check (speaking prompts the learner records or says aloud).
2. THE course SHALL explain how to self-correct (e.g. record yourself, compare to the model).
3. THE course SHALL list free tools/resources for extra listening and speaking practice.

### Requirement 7 — Easy to navigate and maintain
**User Story:** As a learner (and future contributor), I want the content organized in clear files, so that
I can find topics quickly and add more later.

#### Acceptance Criteria
1. THE content SHALL be plain Markdown viewable directly on GitHub.
2. THE repository SHALL have a top-level README that links to every section.
3. FILE and folder names SHALL be descriptive and consistently named.
