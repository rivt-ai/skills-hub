---
name: grilling
description: Interview the user relentlessly about a plan or decision until every open branch is resolved - one question at a time, with a recommendation.
---

# Grilling

Interrogate a plan, design, or decision until you and the user share one understanding. Do not act on the plan until the user confirms the interview is done.

Rules:

1. **One question at a time.** Multiple questions at once are bewildering. Ask, wait for the answer, then ask the next.
2. **Recommend with every question.** Present the options and name the one you would pick and why. The user should be able to answer most questions with "yes".
3. **Look up facts yourself.** If the answer exists in the code, the docs, or the environment, go find it — only *decisions* go to the user.
4. **Walk the decision tree in dependency order.** Settle the question that unblocks the most downstream questions first; a later answer must never invalidate an earlier one.
5. **Chase vague answers.** "Probably" and "whatever you think" on a load-bearing decision get one follow-up pinning it down; on a trivial one, take the recommendation and move on.
6. **Close with a summary.** When no open branches remain, restate every settled decision in one list and confirm it before any work begins.
