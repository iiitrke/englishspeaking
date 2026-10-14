# B2 · Lesson 1 — Explaining Your Code in a Review

## 🎯 Goal
Explain your code, design decisions, and trade-offs clearly in a code review or
design discussion — using your real Java / Spring Boot strengths.

---

## 📖 Phrases for explaining code

| English | When to use | Example |
|---------|-------------|---------|
| The idea here is… | Explaining purpose | "The idea here is to decouple the service from the controller." |
| I decided to… because… | Justifying a choice | "I decided to use a DTO because it keeps the entity hidden." |
| This handles… | Describing responsibility | "This class handles the retry logic." |
| The trade-off is… | Being honest about costs | "The trade-off is a bit more memory, but it's much faster." |
| We could also… but… | Comparing options | "We could also cache it, but it's not worth it yet." |
| Let me walk you through it | Starting a walkthrough | "Let me walk you through the flow." |

---

## 💬 Dialogue — Explaining a Spring Boot design

> **Reviewer:** Can you walk me through this service class?
> **You:** Sure. The idea here is to keep the business logic separate from the controller.
> So the controller just receives the request and delegates to this service.
> **Reviewer:** Why did you add this interface?
> **You:** I decided to use an interface because it makes the code easier to test — I can
> mock it in the unit tests. It also lets us swap the implementation later if we need to.
> **Reviewer:** Makes sense. What about performance?
> **You:** Good question. Right now it hits the database on every call. The trade-off is
> simplicity versus speed. We could add caching, but I'd suggest we do that only if we see
> a real bottleneck.
> **Reviewer:** Agreed. Nice work.

---

## 🔑 Key phrases to reuse

- "Let me walk you through it."
- "The idea here is to **[purpose]**."
- "I decided to **[choice]** because **[reason]**."
- "The trade-off is **[A]** versus **[B]**."
- "We could also **[option]**, but **[why not now]**."
- "That's a fair point." / "Good question."

---

## 🗣️ Say it out loud (drill)

Pick a **real class or method** you wrote recently. Out loud, in English:
1. "Let me walk you through this. The idea here is to __________."
2. "I decided to __________ because __________."
3. "The trade-off is __________."

Do this every time you finish a feature. It's free daily practice using your own code.

---

## ⚠️ Watch out (common Hindi-speaker mistake)

- ❌ "This code is doing the handling of the request."
- ✅ "This code **handles** the request."
- **Why:** Avoid heavy "doing the X-ing of" structures (translated from Hindi). Use the
  simple verb: handles, processes, validates.

- ❌ "I have did the changes."
- ✅ "I **made** the changes." / "I **have made** the changes."
- **Why:** We "**make** changes" (not "do changes"), and the past participle of "do" is "**done**", not "did".

---

➡️ Next: [Lesson 2 — Giving opinions & disagreeing politely](02-giving-opinions.md)
