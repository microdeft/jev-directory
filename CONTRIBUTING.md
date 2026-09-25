# Contributing to the JEV Directory

Thanks for helping improve the **JEV Directory** — a curated, GitHub-only index of open-source projects built on **Jev**, TypeSafe AI's System One decision model.

This document explains what gets listed, what does not, and how to submit an entry.

---

## What belongs here

A project qualifies when **all** of the following are true:

1. **It is a public GitHub repository** with a working URL.
2. **It genuinely uses Jev** — TypeSafe AI's System One model — or implements a documented, Jev-compatible interface (an open reproduction, a client port, or a local drop-in server).
3. **It has an inspectable decision path** — a typed question (`Choice`, `Score`, or `Noul`), a typed answer carrying a probability or confidence, and application code that gates, routes, scores, or acts on the result.
4. **It is described in one factual line** stating what Jev decides and what the surrounding code does with the answer.

Small projects are welcome. Popularity is not a criterion.

## What does not belong here

- **Indexes and awesome-lists themselves.** Directories are used as discovery *sources* and credited in the README, but they are not listed as entries.
- **Generic classifiers, routers, or LLM judges** that do not actually call Jev or implement its interface.
- **Non-GitHub sources** — articles, videos, forum threads, hosted products without public code.
- **Private, deleted, or unreachable repositories.**
- **Duplicate entries.** Every repository appears exactly once, in its single best-fit section.
- **Marketing copy.** Descriptions must be factual, not promotional.

If a repository is real but unproven — a same-week experiment with no stars and no results — it can still be listed; note the limitation honestly in its description rather than leaving it out.

---

## Adding a project

1. **Fork** this repository and create a branch (for example `add/my-jev-project`).
2. **Find the most relevant section** in [`README.md`](README.md). Categories are mutually exclusive — pick the one that describes the project's *primary* purpose, not everything it touches.
3. **Add one row** to that section's table, keeping the existing format:

   ```md
   | [owner/repo](https://github.com/owner/repo) | One factual sentence: what Jev decides and what the surrounding code does with the answer. |
   ```

4. **Open a pull request** and include, in the description:
   - a link to the specific file in your repository that calls Jev (or implements the compatible endpoint);
   - any evidence you want reviewers to check — a test, a benchmark result, a demo;
   - a disclosure if you built or maintain the project.

5. **Update the repository count** in the README's stat line if your change adds or removes entries.

### Entry format

- Use the canonical `owner/repo` name as the link text.
- One sentence, present tense, third person.
- State the *decision* and the *consequence*: "classifies X, then routes Y", "scores Z and drops results below a threshold".
- Mention the stack only when it helps a reader decide (for example: ".NET", "Rust CLI", "Chrome extension").
- Note limitations when they are known and material.

### Examples

```md
| [acme/jev-ticket-router](https://github.com/acme/jev-ticket-router) | Classifies inbound tickets into three queues with a confidence gate, escalating below 0.6 to a human. |
| [acme/jev-local-server](https://github.com/acme/jev-local-server) | Serves a Jev-compatible `/v1/systemone` endpoint from an open model for offline use; answers come from the local model, not hosted Jev. |
```

---

## Review criteria

Maintainers review pull requests against these questions:

| Question | Why it matters |
| --- | --- |
| Does the code actually call Jev? | A README claim is not evidence — look for a real request with typed questions and a parsed answer. |
| Is there something runnable? | A test, an example with expected output, or a public demo is stronger than prose. |
| Do the numbers have a source? | Accuracy, latency, cost, and volume figures should be traceable to the linked repository. |
| Is the placement right? | The entry belongs in the section that matches its primary purpose. |
| Is the description accurate and neutral? | Descriptions are written for this index and are never copied from the project's own README. |

## Corrections and removals

Removals are as valuable as additions. Open an issue or pull request when you find:

- a **broken or moved link** — send the new URL, or delete the entry if the project is gone;
- a project that **no longer uses Jev**;
- an entry in the **wrong section**;
- a description that is **inaccurate, outdated, or promotional**.

## Style guide

- No emoji in entries.
- No superlatives ("blazing fast", "revolutionary", "best").
- No trailing punctuation inside the table cell.
- Keep the table column order intact so the README renders consistently.

## Licensing

This directory and its content are released under the [MIT License](LICENSE). By contributing, you agree that your contribution may be distributed under that license. Linked projects remain the property of their authors under their own licenses.

---

**Not affiliated with TypeSafe AI.** Jev and System One are products and trademarks of TypeSafe AI.
