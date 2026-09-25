<div align="center">

# JEV Directory

### A curated index of **Jev** projects, SDKs, examples & tools — the open-source ecosystem of TypeSafe AI's **System One** decision model.

[![Jev — TypeSafe AI System One decision model](https://img.shields.io/badge/model-Jev-000000?style=flat-square)](https://typesafe.ai)
[![TypeSafe System One model family](https://img.shields.io/badge/family-System%20One-6f42c1?style=flat-square)](https://docs.typesafe.ai/concepts/system-one)
[![Sources: GitHub repositories only](https://img.shields.io/badge/sources-GitHub%20only-181717?style=flat-square&logo=github)](#inclusion-criteria)
[![Pull requests welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat-square)](#contributing)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue?style=flat-square)](LICENSE)

**438 open-source repositories · 17 categories · GitHub-only sources**

**Jev** is TypeSafe AI's System One decision model. You send unstructured state plus **typed questions** — `Choice`, `Score`, `Noul` — and receive **typed, calibrated decisions with probabilities** instead of generated text.

This directory is a **curated index of Jev projects on GitHub**: official SDKs, community client libraries in Python, TypeScript, Go, Rust, Java, .NET, Ruby, PHP and more; LangChain, LiteLLM and Vercel AI Gateway integrations; MCP servers and coding-agent plugins; guardrails, benchmarks, cookbooks, and open-source alternatives that run locally.

> **Not to be confused with** Japanese encephalitis virus (JEV) or any other use of the acronym — this directory covers only **Jev**, the AI decision model by TypeSafe AI.

</div>

---

## Contents

| # | Category | # | Category |
| :-: | --- | :-: | --- |
| 1 | [Official TypeSafe AI Resources](#1-official-typesafe-ai-resources) | 10 | [Agent Memory & Context Engineering](#10-agent-memory--context-engineering) |
| 2 | [Language SDKs & Client Libraries](#2-language-sdks--client-libraries) | 11 | [Developer Utilities & CLIs](#11-developer-utilities--clis) |
| 3 | [Framework & Platform Integrations](#3-framework--platform-integrations) | 12 | [Applications & End-User Tools](#12-applications--end-user-tools) |
| 4 | [Agent Tooling, MCP Servers & Coding-Agent Integrations](#4-agent-tooling-mcp-servers--coding-agent-integrations) | 13 | [Games, Simulation & Robotics](#13-games-simulation--robotics) |
| 5 | [Model Routing & Gateway Infrastructure](#5-model-routing--gateway-infrastructure) | 14 | [Trading & Financial Applications](#14-trading--financial-applications) |
| 6 | [Safety, Guardrails & Verification](#6-safety-guardrails--verification) | 15 | [Open Models & Local Inference](#15-open-models--local-inference) |
| 7 | [Classification, Extraction & Scoring](#7-classification-extraction--scoring) | 16 | [Benchmarks, Evaluations & Research](#16-benchmarks-evaluations--research) |
| 8 | [Search, Retrieval & Data Infrastructure](#8-search-retrieval--data-infrastructure) | 17 | [Learning Resources, Cookbooks & Examples](#17-learning-resources-cookbooks--examples) |
| 9 | [Browser, Mobile & Computer Use](#9-browser-mobile--computer-use) | — | [FAQ](#frequently-asked-questions) · [Contributing](#contributing) |

---

## What is Jev? TypeSafe AI's System One decision model

**Jev** is the first **System One** model from TypeSafe AI: a fast, low-cost model built to return **decisions**, not dialogue. It handles the small, repeated judgments inside software — classify, route, score, verify, gate — where latency and cost matter more than prose.

| | |
| --- | --- |
| **Model** | TypeSafe AI's flagship System One model (`jev-latest`, currently the 1.13 line) |
| **Interface** | `POST /v1/systemone` — send `state` + typed `questions`, receive constrained `answers` with probabilities and confidence |
| **Primitives** | `Choice` (pick one of your options) · `Score` (ordered scale) · `Noul` (yes/no probability) |
| **Design goal** | Fast, low-cost, deterministic-shaped decisions for software: classification, routing, scoring, verification, gatekeeping |
| **Not** | Not a chat model. It does not generate prose and cannot hallucinate free text |

> A Jev integration is usually **a decision in the middle of an application loop**: your code owns the options, the thresholds, the side effects, and the fallbacks — Jev returns the judgment.

---

## Start here

**New to Jev?** Read [What is Jev?](#what-is-jev-typesafe-ais-system-one-decision-model) above, then try the [official playground](https://github.com/TypeSafeAI/typesafe-playground) with an API key from the [TypeSafe console](https://console.typesafe.ai).

**Looking for something specific?**

| If you want to… | Start with |
| --- | --- |
| Call Jev from code | [Official TypeSafe AI resources](#1-official-typesafe-ai-resources) · [Language SDKs & client libraries](#2-language-sdks--client-libraries) |
| Add Jev to an AI agent | [MCP servers & coding-agent plugins](#4-agent-tooling-mcp-servers--coding-agent-integrations) |
| Route models, tools, or skills | [Model routing & gateway infrastructure](#5-model-routing--gateway-infrastructure) |
| Gate risky actions safely | [Safety, guardrails & verification](#6-safety-guardrails--verification) |
| Run decisions locally or free | [Open models & local inference](#15-open-models--local-inference) |
| Follow a runnable recipe | [Cookbooks & examples](#17-learning-resources-cookbooks--examples) |
| Evaluate Jev on your own task | [Benchmarks & research](#16-benchmarks-evaluations--research) |

---

## How to use this directory

1. **Pick a category.** Categories are mutually exclusive — every project is listed **once**, in the section that best describes its primary purpose.
2. **Read the one-line summary.** Each entry states *what Jev decides* and *what the surrounding code does with it*.
3. **Check the source before adopting.** Many entries are same-week experiments. A listing here is **not** an endorsement, a security review, or a claim of production readiness.
4. **Prefer entries with evidence.** Repositories that publish runnable checks, raw results, or documented limitations are marked with a note in their description where known.

### Inclusion criteria

- The project is a **public GitHub repository**.
- It **uses Jev** (TypeSafe System One), or implements a **documented Jev-compatible/port/derivative** interface.
- It has an **inspectable decision path**: a typed question, a typed answer, and code that acts on it.
- One line describes it; no duplicates across sections.

Sources that are not GitHub repositories (articles, videos, forum posts, provider documentation) are **out of scope** and are not listed, though they are credited in [Sources & Acknowledgements](#sources--acknowledgements).

---

## 1. Official TypeSafe AI Resources

The official TypeSafe AI repositories on GitHub: the Python and TypeScript SDKs for the Jev / System One API, agent skills, a baseline LLM adapter for comparisons, and the reference playground, UI kit, and router.

| Project | What it provides |
| --- | --- |
| [typesafe-ai/typesafe-sdk-python](https://github.com/typesafe-ai/typesafe-sdk-python) | Official Python SDK. Typed questions, `Choice`/`Score`/`Noul` primitives, retries, Pydantic `response_model` support (v0.7+). |
| [typesafe-ai/typesafe-sdk-js](https://github.com/typesafe-ai/typesafe-sdk-js) | Official TypeScript/JavaScript SDK for the `/v1/systemone` endpoint. |
| [typesafe-ai/skills](https://github.com/typesafe-ai/skills) | Official agent skills covering the System One distinction, quick starts, and coding-agent patterns. |
| [typesafe-ai/system-one-adapter-python](https://github.com/typesafe-ai/system-one-adapter-python) | Drop-in `typesafe_sdk` replacement backed by OpenAI, Anthropic, or Gemini — for running the same typed questions against an LLM as a baseline. |
| [typesafe-ai/typesafe-ai.github.io](https://github.com/typesafe-ai/typesafe-ai.github.io) | Source repository for the official TypeSafe AI website. |
| [TypeSafeAI/typesafe-playground](https://github.com/TypeSafeAI/typesafe-playground) | Interactive playground: 110+ use cases, Jev Chat, a Jev-only browser agent, JevDoom, and a duck-driving demo. |
| [TypeSafeAI/typesafe-ui](https://github.com/TypeSafeAI/typesafe-ui) | Shared UI primitives (typed-response meters, decision contracts) and 169 interactive Jev Labs. |
| [TypeSafeAI/typesafe-router](https://github.com/TypeSafeAI/typesafe-router) | Reference model/tool router plus a Next.js lab: closed-set `choice`, confidence thresholds, and explicit fallback policies. |
| [TypeSafeAI/clarity-judge](https://github.com/TypeSafeAI/clarity-judge) | Writing-clarity judge built on `Noul`/`Choice` checks. |

---

## 2. Language SDKs & Client Libraries

Client libraries for calling the Jev / System One API (`POST /v1/systemone`) from Python, TypeScript & JavaScript, Go, Rust, Java, Kotlin, Scala, .NET, Ruby, PHP, Elixir, Haskell, Clojure, OCaml, Swift, and Dart.

### Python

| Project | Details |
| --- | --- |
| [AboveColin/jevclient](https://github.com/AboveColin/jevclient) | Async client for typed questions and probabilities. |
| [steven-shoemaker/hunch](https://github.com/steven-shoemaker/hunch) | Asks closed-set questions over every item in a list or DataFrame (`classify`, `score`, `rank`, `check`, `extract`), caches answers, joins them back. A [TypeScript port](https://github.com/steven-shoemaker/hunch-js) offers the same verbs. |
| [pithings/advocaat](https://github.com/pithings/advocaat) | Small type-safe client for asking Jev questions about a dataset. |
| [allebee/pytest-jev](https://github.com/allebee/pytest-jev) | pytest plugin: `jev.expect` turns plain-English claims about a test's text into assertions (pass ≥ 0.8, must-not-hold ≤ 0.2). |
| [chunxiaoxx/nautilus-compass](https://github.com/chunxiaoxx/nautilus-compass) | `jev-trust` middleware: logs every decision, measures domain calibration (accuracy, Brier, top-label ECE), and signs the evidence with ed25519. |
| [ma2saka/jevmock01](https://github.com/ma2saka/jevmock01) | Function-mocking decorator that delegates judgments to Jev's typed engine. |

### TypeScript & JavaScript

| Project | Details |
| --- | --- |
| [Mawfyy/jevflow](https://github.com/Mawfyy/jevflow) | Composes `Noul`/`Score`/`Choice` into deterministic threshold workflows that batch into one `systemOne` call and return explainable actions, with a mock provider for policy tests. |
| [pedro-pscunha/guideme-typescript](https://github.com/pedro-pscunha/guideme-typescript) | SDK where a Jev judgment *is* the control flow. |
| [ChristopherKotthoff/jif-js](https://github.com/ChristopherKotthoff/jif-js) | Replaces ordinary `if` statements with Jev-decided branches. A [Python counterpart](https://github.com/ChristopherKotthoff/jif-py) mirrors the API. |
| [jonaed1230/typesafe-ai](https://github.com/jonaed1230/typesafe-ai) | Lightweight wrapper that asks typed questions and returns unwrapped answers. |
| [juspay/neurolink](https://github.com/juspay/neurolink) | Unified TypeScript interface across 40+ providers, exposing Jev-backed calibrated `decide` alongside generate/stream, MCP, RAG, and memory. |

### Go

| Project | Details |
| --- | --- |
| [HomayoonAlimohammadi/jev-sdk-go](https://github.com/HomayoonAlimohammadi/jev-sdk-go) | Dependency-free Go 1.24+ client that reads `Choice`/`Score` answers back as the caller's own types, with retries and examples against an in-process fake. |
| [gamebox/typesafe-ai-go](https://github.com/gamebox/typesafe-ai-go) | Minimal Go SDK for integrating Jev. |
| [peach-zhang/typesafe-go](https://github.com/peach-zhang/typesafe-go) | Exposes typed judgments and probabilities for workflow control. |
| [kisshan13/typesafe-ai-go](https://github.com/kisshan13/typesafe-ai-go) | Go client with typed questions, fluent builders, retries, and examples. |
| [jmelahman/typesafe-sdk-go](https://github.com/jmelahman/typesafe-sdk-go) | Community Go library for the TypeSafe API. |
| [guchengod/typesafe-sdk-go](https://github.com/guchengod/typesafe-sdk-go) | Classification and rating primitives over text and JSON. |
| [captain-corgi/typesafe-sdk-go](https://github.com/captain-corgi/typesafe-sdk-go) | Community-maintained Go SDK for Jev. |
| [Stumble/jev-go](https://github.com/Stumble/jev-go) | Community Go SDK. |

### Rust

| Project | Details |
| --- | --- |
| [ariel-frischer/jevkit](https://github.com/ariel-frischer/jevkit) | CLI that lints `Choice`/`Score`/`Noul` question sets with 13 offline rules before spending a call, then prints parsed JSON answers with exit code 2 for billed-but-useless requests. |
| [luizribeiro/jevrs](https://github.com/luizribeiro/jevrs) | Sans-IO Rust core with typed questions and WASI transport support. |
| [zchee/typesafe-sdk-rust](https://github.com/zchee/typesafe-sdk-rust) | Async Rust client with derive-macro question sets, ported from the Python SDK. |
| [tanishqnalloju/typesafe-rust-sdk](https://github.com/tanishqnalloju/typesafe-rust-sdk) | Rust SDK for the System One typed-decision API. |
| [codeitlikemiley/typesafe-sdk-rust](https://github.com/codeitlikemiley/typesafe-sdk-rust) | Rust SDK for the TypeSafe AI API. |
| [community-ports/typesafeai-sdk-rust-community](https://github.com/community-ports/typesafeai-sdk-rust-community) | Community-built Rust port of the official Python SDK. |

### JVM — Java · Kotlin · Scala

| Project | Details |
| --- | --- |
| [spring-ai-community/spring-ai-typesafe](https://github.com/spring-ai-community/spring-ai-typesafe) | Java SDK plus Spring AI integrations for judge, guardrail, and RAG post-processing use cases. |
| [galitianu/jev4j](https://github.com/galitianu/jev4j) | Java 21 client library supporting typed questions and typed answers. |
| [jamilxt/typesafe-ai-java](https://github.com/jamilxt/typesafe-ai-java) | Community Java client for the System One API, explicitly not an official product. |
| [Olti1947/jev-java](https://github.com/Olti1947/jev-java) | Idiomatic Java SDK for the Jev decision engine. |
| [gudcks0305/jev-java](https://github.com/gudcks0305/jev-java) | Java SDK with Spring Boot and WebClient integrations, plus Vercel AI Gateway support. |
| [oskarscot/typesafe4j](https://github.com/oskarscot/typesafe4j) | Lightweight Java SDK for Jev models. |
| [Premo-Cloud/typesafe-sdk-java](https://github.com/Premo-Cloud/typesafe-sdk-java) | Unofficial Java client extending the community SDK ecosystem. |
| [early-effect/hexis](https://github.com/early-effect/hexis) | ZIO / Scala 3 SDK for System One. |
| [aoprisan/typesafe-ai-scala-sdk](https://github.com/aoprisan/typesafe-ai-scala-sdk) | Community Scala client for TypeSafe AI and Jev. |
| [snevadalabs/jev-kmp](https://github.com/snevadalabs/jev-kmp) | Kotlin Multiplatform client (JVM/Android/iOS) exposing typed answers and calibrated probabilities. |
| [ItisNoMatter/kojev](https://github.com/ItisNoMatter/kojev) | Kotlin Multiplatform client that answers `Choice`/`Score` questions as the caller's own enums; thresholds stay in caller code. |

### .NET

| Project | Details |
| --- | --- |
| [hardkoded/typesafe-sdk-dotnet](https://github.com/hardkoded/typesafe-sdk-dotnet) | Unofficial .NET port supporting typed questions and answers. |
| [tryAGI/TypeSafeAI](https://github.com/tryAGI/TypeSafeAI) | AutoSDK-generated, NativeAOT-ready .NET client with batching, DI, and Microsoft.Extensions.AI adapters. |
| [Hawxy/TypeSafeAI.Net](https://github.com/Hawxy/TypeSafeAI.Net) | .NET SDK with `HttpClientFactory`/DI wiring and Microsoft.Extensions.AI guardrail, routing, tool, and evaluator adapters. |
| [elbruno/ElBruno.AI.Jev](https://github.com/elbruno/ElBruno.AI.Jev) | .NET 10 SDK integrating Jev typed decisions with Microsoft.Extensions.AI. |
| [bariskisir/JevSharp](https://github.com/bariskisir/JevSharp) | .NET 10 SDK routing decisions through TypeSafe, OpenRouter, Vercel AI Gateway, or compatible endpoints. |
| [FYIsoft/FYIsoft.Extensions.AI.Providers](https://github.com/FYIsoft/FYIsoft.Extensions.AI.Providers) | Provider collection adding Jev alongside Anthropic Claude for Microsoft.Extensions.AI. |

### Ruby

| Project | Details |
| --- | --- |
| [afurm/typesafe-sdk-ruby](https://github.com/afurm/typesafe-sdk-ruby) | Ruby port of the JS SDK with typed questions, retries, and typed errors. |
| [dtheofr/typesafe-jev-ruby](https://github.com/dtheofr/typesafe-jev-ruby) | Dependency-free client returning probabilistic answers. |
| [joshmn/typesafe-sdk](https://github.com/joshmn/typesafe-sdk) | Ruby client for the typesafe.ai API. |
| [obie/ruby_decision_model](https://github.com/obie/ruby_decision_model) | Client for decision models such as Jev, so Ruby apps can ask typed questions directly. |
| [javiergradiche/ruby_llm-providers-typesafe](https://github.com/javiergradiche/ruby_llm-providers-typesafe) | RubyLLM provider integrating System One models for judgments, evaluations, and reranking. |

### PHP

| Project | Details |
| --- | --- |
| [sanmai/typesafe-ai-php](https://github.com/sanmai/typesafe-ai-php) | Unofficial PHP client for Jev and the TypeSafe API. |
| [valksor/typesafe-sdk-php](https://github.com/valksor/typesafe-sdk-php) | PHP client implementing 1:1 parity with the official JS and Python SDKs. |
| [binnash/typesafe-sdk](https://github.com/binnash/typesafe-sdk) | PHP/Laravel client with typed questions, retries, and tests for routing, thresholds, ranking, and side effects. |
| [Butochnikov/laravel-typesafe-jev](https://github.com/Butochnikov/laravel-typesafe-jev) | Laravel integration with typed responses, async requests, scoped DI, and testing fakes. |

### Elixir

| Project | Details |
| --- | --- |
| [Studio-Sasquatch/typesafe-sdk-elixir](https://github.com/Studio-Sasquatch/typesafe-sdk-elixir) | Community Elixir SDK for Jev typed decisions. |
| [nshkrdotcom/typesafe_sdk](https://github.com/nshkrdotcom/typesafe_sdk) | Idiomatic Elixir port with streaming, structured outputs, tool calling, and agent workflows; Jev as flagship model. |
| [dannote/jev](https://github.com/dannote/jev) | Elixir/OTP client designed around GenServer replies so callers pattern-match on the answer. |

### Haskell & Functional

| Project | Details |
| --- | --- |
| [realbogart/jev](https://github.com/realbogart/jev) | Haskell library for the Jev model. |
| [byteally/typesafe-sdk](https://github.com/byteally/typesafe-sdk) | Haskell SDK exposing typed judgments to Haskell applications. |
| [inanna-malick/jev-dsl](https://github.com/inanna-malick/jev-dsl) | Early-alpha Haskell DSL encoding typed question packets and decoding answers; transport left to the caller. |
| [jonesmelton/verdict](https://github.com/jonesmelton/verdict) | OCaml client interface for the Jev model. |

### Other Languages

| Project | Details |
| --- | --- |
| [IAmNo1Special/typesafe-sdk-godot](https://github.com/IAmNo1Special/typesafe-sdk-godot) | Godot 4.7 SDK with feature parity to the Python SDK and HTTP API. |
| [RomainFranceschini/typesafe_ai_sdk](https://github.com/RomainFranceschini/typesafe_ai_sdk) | Community Dart package for the TypeSafe AI API. |
| [peterfriese/jev-foundation-models](https://github.com/peterfriese/jev-foundation-models) | Native Swift 6 bridge integrating Jev with Apple's Foundation Models framework. |
| [tinystruct/tinystruct-typesafe-sdk](https://github.com/tinystruct/tinystruct-typesafe-sdk) | tinystruct-based SDK exposing Jev typed decisions. |
| [antlobach/clojev](https://github.com/antlobach/clojev) | Portable Clojure SDK for System One with no Java interop layer. |
| [simxnherrera/jevr](https://github.com/simxnherrera/jevr) | Native R client for typed questions via TypeSafe or OpenRouter. |

---

## 3. Framework & Platform Integrations

Jev wired into the frameworks and platforms you already use: LangChain, LangChain.js, Pydantic AI, LiteLLM, BAML, Composio, Effect, TanStack AI, AutoGPT, Home Assistant, n8n, and more.

| Project | What it integrates |
| --- | --- |
| [langchain-ai/langchain](https://github.com/langchain-ai/langchain) | Python `TypeSafeClassifier` Runnable with batched typed questions, model routing, and risky-tool middleware. |
| [langchain-ai/langchainjs](https://github.com/langchain-ai/langchainjs) | JavaScript/TypeScript classifier Runnable and middleware for bounded routing and tool-call checks. |
| [pydantic/pydantic-ai](https://github.com/pydantic/pydantic-ai) | First-class TypeSafe model provider deriving Jev questions from Pydantic output types. |
| [BerriAI/litellm](https://github.com/BerriAI/litellm) | Jev-backed complexity routing plus an optional relevance guardrail for compacting tool results. |
| [0xPlaygrounds/rig](https://github.com/0xPlaygrounds/rig) | Rust `rig-typesafeai` crate with typed `Choice`/`Score`/`Noul` queries, validation, and fixtures. |
| [ComposioHQ/composio](https://github.com/ComposioHQ/composio) | Tool shortlisting and selection from a bounded set, with confidence and destructive-action gates. |
| [Effect-TS/effect](https://github.com/Effect-TS/effect) | `@effect/ai-typesafe` decision model mapping classify, probability, and rating operations to Jev questions. |
| [BoundaryML/baml](https://github.com/BoundaryML/baml) | Maps typed function return values to Jev questions (v1 nightly line). |
| [ax-llm/ax](https://github.com/ax-llm/ax) | Native TypeSafe client and provider for Boolean, Choice, Score, and raw questions with answer validation. |
| [TanStack/ai](https://github.com/TanStack/ai) | `@tanstack/ai-typesafe` adapter exposing typed decisions through TanStack AI's `decide()` API. |
| [vercel/eve](https://github.com/vercel/eve) | Agent framework whose `auto` model router defaults to Jev via Vercel AI Gateway. |
| [vercel-labs/ai-cli](https://github.com/vercel-labs/ai-cli) | Vercel Labs CLI that can run Jev as the evaluation model for its `evaluate` command. |
| [vercel-labs/ai-python](https://github.com/vercel-labs/ai-python) | Official Python AI SDK carrying Jev through its evaluation operation and Gateway examples. |
| [vercel-labs/fx](https://github.com/vercel-labs/fx) | Experimental Zig coding agent with an optional Jev permission reviewer mapped to a `Choice`. |
| [cline/plugins](https://github.com/cline/plugins) | Cline's official plugin collection, including a Jev-driven browser plugin. |
| [Significant-Gravitas/AutoGPT](https://github.com/Significant-Gravitas/AutoGPT) | Autonomous agent platform with first-class TypeSafe Jev decision blocks for typed routing and next-action dispatch. |
| [agentscope-ai/agentscope](https://github.com/agentscope-ai/agentscope) | Multi-agent platform implementing native TypeSafe classification models (binary, choice, score). |
| [elie222/inbox-zero](https://github.com/elie222/inbox-zero) | Open-source email assistant where Jev is an optional classifier backend returning bounded categories. |
| [allenporter/home-assistant-typesafe](https://github.com/allenporter/home-assistant-typesafe) | Home Assistant integration for structured intent routing and device control. |
| [AboveColin/HA-Jev](https://github.com/AboveColin/HA-Jev) | Home Assistant integration exposing typed answers as sensors, automation actions, and an Assist conversation agent. |
| [Paca-AI/paca](https://github.com/Paca-AI/paca) | Self-hosted Jira alternative: Jev assigns tasks, fills blank fields, and routes automation at ≥ 0.6 confidence. |
| [usenotra/notra](https://github.com/usenotra/notra) | Production GEO platform routing brand-visibility classifiers off an LLM and onto Jev at a 0.5 threshold. |
| [milvus-io/milvus-model](https://github.com/milvus-io/milvus-model) | Python reranker adapter batching candidate-document `Noul` questions and preserving original indices. |
| [milvus-io/bootcamp](https://github.com/milvus-io/bootcamp) | `bootcamp/RAG/search_with_jev` — nine notebooks combining embeddings, Milvus retrieval, and typed Jev decisions for reranking, filtering, routing, and evaluation. |
| [itsmeyaw/n8n-nodes-typesafe](https://github.com/itsmeyaw/n8n-nodes-typesafe) | Community n8n nodes putting TypeSafe AI inside visual automation workflows. |
| [n3ndor/n8n-nodes-typesafe-jev](https://github.com/n3ndor/n8n-nodes-typesafe-jev) | Community n8n node for asking multiple typed questions over workflow state. |
| [FFatTiger/new-api-plugin-typesafe](https://github.com/FFatTiger/new-api-plugin-typesafe) | Adds a native `/v1/systemone` endpoint to the `new-api` LLM gateway. |

---

## 4. Agent Tooling, MCP Servers & Coding-Agent Integrations

MCP servers, agent skills, and plugins for Claude Code, Codex, Cursor, Cline, Pi, Hermes, and DeepSeek Harness that put typed Jev judgments behind standard tool interfaces.

### MCP Servers

| Project | What it exposes |
| --- | --- |
| [itsmostafa/typesafe-mcp](https://github.com/itsmostafa/typesafe-mcp) | MCP connector giving agents direct access to Jev for fast evaluations. |
| [Brainwires/jevwire](https://github.com/Brainwires/jevwire) | MCP server, embeddable `DecisionModel` library, and an escalate-only Claude Code plugin. |
| [sf-stav/mcp_typesafe](https://github.com/sf-stav/mcp_typesafe) | MCP server making System One models available inside agent workflows. |
| [CodeIA-Academy/jev-mcp](https://github.com/CodeIA-Academy/jev-mcp) | Dependency-free local MCP server exposing `ask_jev` and `list_jev_models` to Claude Code, Codex, and Hermes. |
| [blakestone-x/jev-mcp](https://github.com/blakestone-x/jev-mcp) | MCP server exposing classify, score, check, match, and screen tools with confidence on every answer. |
| [BYK/jev-mcp](https://github.com/BYK/jev-mcp) | Eval-first MCP server returning typed judgments with probabilities. |
| [jkudish/jev-mcp](https://github.com/jkudish/jev-mcp) | Node MCP server with ten bounded tools: claim verification, content screening, candidate ranking, extraction, and patch review. |
| [burnigtm/jev-mcp](https://github.com/burnigtm/jev-mcp) | MCP server putting Jev into the coding loop for Cursor, Codex, and any MCP client. |
| [clouatre-labs/decisions-judge-mcp](https://github.com/clouatre-labs/decisions-judge-mcp) | Exposes yes/no probability, choice, and score decisions through MCP. |
| [nirvana124/typesafe-mcp](https://github.com/nirvana124/typesafe-mcp) | MCP server exposing Jev to MCP-compatible clients. |
| [vineetagarwal54/jev-mcp-middleware](https://github.com/vineetagarwal54/jev-mcp-middleware) | Intercepts agent tool calls and combines deterministic policy with Jev risk judgments before forwarding upstream. |
| [seb4ez/jevguard-mcp](https://github.com/seb4ez/jevguard-mcp) | Evaluates shell-command safety, patch regression risk, and decision certainty, with SQLite WAL caching and escape injection. |
| [eaisdevelopment/jevmcp](https://github.com/eaisdevelopment/jevmcp) | MCP server for tooling, code audits, CI/CD analysis, and other software-development workflows. |
| [King4s/jev-loop](https://github.com/King4s/jev-loop) | MCP server and skill where Jev decides and Claude Code, Codex, or Hermes builds. |
| [simota/tenbin](https://github.com/simota/tenbin) | MCP server that decomposes judgments, lints `Choice`/`Score`/`Noul` questions, and proposes confidence thresholds from labelled examples. |

### Coding-Agent Plugins & Skills

| Project | Details |
| --- | --- |
| [shitianfang/jev-use](https://github.com/shitianfang/jev-use) | Claude Code / Codex / pi plugin: `jev_judge` batches typed questions into one call, `jev_gate` can only deny or ask, and unreachable backends escalate instead of allowing. |
| [Nasrallah-AL/jev-cli](https://github.com/Nasrallah-AL/jev-cli) | CLI (`jevctl`) turning judgments into exit-code-gated shell commands — verify, screen, classify, reroute, compact transcripts — plus a Claude Code plugin. |
| [formulahendry/jev-acp](https://github.com/formulahendry/jev-acp) | Standalone ACP agent exposing Choice/Score/Noul decisions through guided input and reusable templates. |
| [yuyang2230/jev-agent-skill](https://github.com/yuyang2230/jev-agent-skill) | Claude Code / ZCode skill offloading classify, screen, score, and compliance checks; includes a retry-hardened caller and a comment-triage pipeline. |
| [giorgiocerruti/jev-skils](https://github.com/giorgiocerruti/jev-skils) | Claude Code skill with JS/TS integration primitives, SDK usage patterns, and evaluation triggers. |
| [kitze/skillbox](https://github.com/kitze/skillbox) | Self-hosted skill library with opt-in Jev recommendations over task text; failures fall back to deterministic search. |
| [Dicklesworthstone/skillranker](https://github.com/Dicklesworthstone/skillranker) | Rust CLI ranking skills for the next agent step, with Claude Code hooks, abstention, and local feedback. |
| [kerpopule/hermes-jev-skills](https://github.com/kerpopule/hermes-jev-skills) | Python toolkit and nine agent skills for Hermes, Claude Code, and Codex: model routing, passage filtering, skill selection, and bounded computer/browser actions. |
| [Mrribvar/hermes-jev-plugin](https://github.com/Mrribvar/hermes-jev-plugin) | Hermes Agent plugin exposing Jev through Vercel AI Gateway for classification and routing. |
| [RaulLazaro/dsh-jev](https://github.com/RaulLazaro/dsh-jev) | DeepSeek Harness plugin for batch typed judgments with per-user settings. |
| [xienda/dsh-jev-verify](https://github.com/xienda/dsh-jev-verify) | Decision tools for choice/score/no-yes plus a live verification benchmark. |
| [CSlawyer1985/dsh-jev-router](https://github.com/CSlawyer1985/dsh-jev-router) | DSH plugin choosing reasoning intensity, guarded by hard gates and cost limits. |
| [mejiasd3v/pi-jev-router](https://github.com/mejiasd3v/pi-jev-router) | Automatic per-request model routing for the Pi coding agent via Vercel AI Gateway. |
| [y0usaf/pi-jev](https://github.com/y0usaf/pi-jev) | Adds a measured tool-call gate to the Pi coding agent. |
| [iefnaf/pi-jev](https://github.com/iefnaf/pi-jev) | Pi extension suite for selective context compaction and model routing (TypeSafe or OpenRouter transports). |
| [notque/vexjoy-agent](https://github.com/notque/vexjoy-agent) | Cross-harness agent/skill/pipeline selection, then an intent check before dispatch; deterministic rules bypass Jev. |
| [24601/Augustus](https://github.com/24601/Augustus) | Skill for building and improving decision-model systems, with composition rules and an offline paired-outcome evaluator. |
| [hoaphm/jev-decision-maker](https://github.com/hoaphm/jev-decision-maker) | OMP plugin letting Jev choose the next coding step from agent-supplied candidates. |
| [ab2webco/orca-jev-advisor](https://github.com/ab2webco/orca-jev-advisor) | Jev-backed decision layer judging what Orca Lab agents are about to run. |

---

## 5. Model Routing & Gateway Infrastructure

Routers and gateways where one Jev decision picks the model, the tier, the reasoning effort, or the tool — the cost-control layer of a multi-model stack.

| Project | Routing behavior |
| --- | --- |
| [0xNatoshi/jev-codex-router](https://github.com/0xNatoshi/jev-codex-router) | Selects Codex's model, reasoning depth, and speed mode on every turn. |
| [xinyao27/jevonian](https://github.com/xinyao27/jevonian) | Local OpenAI/Anthropic-compatible proxy; `jevonian/auto` asks Jev to choose model and thinking level after deterministic compatibility and quota filters. |
| [dirien/jev-router](https://github.com/dirien/jev-router) | Pass-through router selecting a model tier for each human turn in Claude Code and Codex CLI. |
| [hyspacex/jev-router](https://github.com/hyspacex/jev-router) | Self-hosted OpenAI-compatible proxy that evaluates requests with Jev, then applies YAML rules to pick the upstream model and reasoning effort. |
| [AABBAASS1/jev-router](https://github.com/AABBAASS1/jev-router) | Cross-platform router choosing between Claude, ChatGPT, Cursor, and other agents in under a second. |
| [mjmiller41/jev-router-harness](https://github.com/mjmiller41/jev-router-harness) | AI terminal harness combining Vercel Eve and Jev for dynamic model routing. |
| [prismhq/jev-router](https://github.com/prismhq/jev-router) | Open-source LiteLLM-based router where a Jev decision picks the serving model. |
| [suenot/codex-jev-router](https://github.com/suenot/codex-jev-router) | Selects a Codex subagent model and reasoning effort; uncertain decisions fall back to Sol. |
| [miniLV/Jev-Auto-Router](https://github.com/miniLV/Jev-Auto-Router) | Per-call Codex router choosing model and reasoning effort, with an independent verification step. |
| [gargpratyush/jev-router](https://github.com/gargpratyush/jev-router) | Routes Claude Code tasks to the cheapest capable model. |
| [lorensation/llm-cost-optimizer-jev](https://github.com/lorensation/llm-cost-optimizer-jev) | Analyzes request complexity, selects the cheapest capable model, and validates its own routing decisions. |
| [iamvatsalpatel/tiershift](https://github.com/iamvatsalpatel/tiershift) | Policy-bounded model routing for TypeScript and Python. |
| [vinilana/jev-gateway](https://github.com/vinilana/jev-gateway) | Local gateway using Jev to choose coding-agent tools, with Codex/Claude Code launchers and routing on/off comparisons. |
| [FreeJolan/jev-gateway](https://github.com/FreeJolan/jev-gateway) | Lightweight Vercel-deployable API gateway exposing an `ask` endpoint with SDK compatibility. |
| [dzhng/duet-agent](https://github.com/dzhng/duet-agent) | Agent harness keeping a Jev-backed routing table for deciding which model serves a request. |
| [BillionsBobby/JevRouter](https://github.com/BillionsBobby/JevRouter) | Routes models, skills, MCP tools, CLIs, and plugins through typed choices while code enforces availability, permissions, and confirmation; includes offline demo mode and decision receipts. |
| [nidhi-singh02/agent-router](https://github.com/nidhi-singh02/agent-router) | Filters eligible coding models by quota and policy, then lets Jev rank them. |
| [yusukebe/hono-jev-router](https://github.com/yusukebe/hono-jev-router) | Routes Hono HTTP requests by meaning. |
| [samuelfaj/distill](https://github.com/samuelfaj/distill) | Harness that can use Jev to select a model and effort, route utility tasks, and judge what context to retain. |
| [colinmcdermott/grok-jev-router](https://github.com/colinmcdermott/grok-jev-router) | Routes decisions through Jev while Grok Bot executes; humans keep control of irreversible actions. |
| [Bodila51/muse-jev-playbook](https://github.com/Bodila51/muse-jev-playbook) | Muse playbook adding a fast Jev decision layer with confidence policies and routing before costly agent execution. |
| [backant-io/jevelry](https://github.com/backant-io/jevelry) | Runtime accepting Jev inputs and producing typed verdicts, with reusable templates and a local decision/outcome log. |

---

## 6. Safety, Guardrails & Verification

Guardrails, safety gates, and verification layers: tool-call firewalls, prompt-injection screening, evidence ledgers, calibration, and community moderation.

| Project | What it checks |
| --- | --- |
| [klauswg/jev-guard](https://github.com/klauswg/jev-guard) | Real-time crypto exchange deposit/withdrawal risk gateway: four typed questions per transfer, a hard-rule veto layer, and a direction-aware gate that composes the final action. |
| [qkal/Canny](https://github.com/qkal/Canny) | Evidence ledger preventing coding agents from claiming completion without proof; append-only, no runtime dependencies. |
| [Yasir-Khan-7/jev-sentinel](https://github.com/Yasir-Khan-7/jev-sentinel) | Prompt-injection protection and tool-call gating for LangChain/LangGraph: allow, review, or block. |
| [CMaintz/jev-guard](https://github.com/CMaintz/jev-guard) | Vets an agent's tool calls with allow/block/hold outcomes and fails safe when the verdict is uncertain. |
| [CMaintz/jev-triage](https://github.com/CMaintz/jev-triage) | Near-free issue triage using typed labels with escalation for uncertain cases. |
| [lgy1027/jevshield](https://github.com/lgy1027/jevshield) | LangChain-ready security gate with calibrated-confidence routing, fail-closed parsing, and a local fallback. |
| [prakash7474/JevShield](https://github.com/prakash7474/JevShield) | TypeScript SDK plus desktop IDE with state determinism, prompt-injection defenses, and tree chunking. |
| [omkarghugarkar007/actiongate-jev](https://github.com/omkarghugarkar007/actiongate-jev) | Runtime authorization and guardrails for agent tool calls using deterministic policies plus Jev through OpenRouter. |
| [kallurayaankit/jev-safety-gate](https://github.com/kallurayaankit/jev-safety-gate) | Safety-layer repository gating AI-agent actions with Jev. |
| [ThiagaoBR/typesafe_agent_gates](https://github.com/ThiagaoBR/typesafe_agent_gates) | LangChain/Deep Agents middleware applying typed judgments to shell-command safety, issue severity, merge requests, and weakened tests. |
| [RiskAverseTech/toolgate](https://github.com/RiskAverseTech/toolgate) | Claude Code hook firewall that calibrates and gates tool calls. |
| [agent-chaperone/agent-chaperone](https://github.com/agent-chaperone/agent-chaperone) | Screens AI-agent tool calls and their results before they proceed. |
| [celolopes/jev-dev-harness](https://github.com/celolopes/jev-dev-harness) | Developer harness and runtime safety toolkit for Jev-powered coding agents. |
| [0xshikhar/jev-fuse](https://github.com/0xshikhar/jev-fuse) | Governed execution layer adding policy controls and auditing between Jev decisions and Claude Code, MCP, or AI SDKs. |
| [AndreuVM/jev-reasoning-navigator](https://github.com/AndreuVM/jev-reasoning-navigator) | Cognitive supervision, loop prevention, and anti-hallucination checks for agents. |
| [aishwary-dongre/jev-xray](https://github.com/aishwary-dongre/jev-xray) | Decision forensics estimating which input regions influence a Jev probability through systematic ablation. |
| [VeridicalTech/Edward](https://github.com/VeridicalTech/Edward) | One batched `Choice` over a cross-turn coding-agent trajectory (continue / pause / escalate), with low-confidence verdicts routed to humans and Ed25519-signed receipts. |
| [valentynkit/jev-belay](https://github.com/valentynkit/jev-belay) | Claude Code Stop hook that checks the transcript for evidence before trusting a "done" claim; fails open on every error path. |
| [valentynkit/jev-commit](https://github.com/valentynkit/jev-commit) | Pre-commit hook judging whether the commit message matches the staged diff; blocks only on detected credentials. |
| [doeixd/jev-pref](https://github.com/doeixd/jev-pref) | Lints code changes against project preferences from `jev-pref.json` and feeds findings back to agents. |
| [jpowersdev/neuralint](https://github.com/jpowersdev/neuralint) | AI code review that checks repositories against their own stated rules. |
| [tincke10/Jevest](https://github.com/tincke10/Jevest) | Millisecond decision layer around an LLM pull-request review pipeline. |
| [fewhnhouse/jev-review-action](https://github.com/fewhnhouse/jev-review-action) | GitHub Action classifying code reviews, providing concrete CI integration. |
| [gauravkhuraana/jev-qa-demos](https://github.com/gauravkhuraana/jev-qa-demos) | Demos for CI-failure triage, command safety checks for test agents, RAG grounding checks, and documented failure modes. |
| [Ashadeepa/typesafe-jev-model-use-cases](https://github.com/Ashadeepa/typesafe-jev-model-use-cases) | Parallel `Noul` judgments plus a `Choice`-based citation and claim checker. |
| [seb4ez/jevguard](https://github.com/seb4ez/jevguard) | Deterministic decision execution, zero-token caching, and certainty calibration around Jev. |
| [luantak/is-malicious](https://github.com/luantak/is-malicious) | Scans codebases for hidden, deceptive, or data-stealing code and points to suspicious files and lines. |
| [teyhouse/jev-secret-detection](https://github.com/teyhouse/jev-secret-detection) | Benchmarks Jev on secret-detection datasets derived from gitleaks, GitGuardian, and others. |
| [ohernandezdev/jevmod](https://github.com/ohernandezdev/jevmod) | Moderation toolkit for Discord, Telegram, and Reddit with per-category probabilities, configurable thresholds, CLI, SDKs, HTTP API, and MCP. |
| [ItisShikhar/gg-friggin-ez](https://github.com/ItisShikhar/gg-friggin-ez) | Node.js multilingual profanity and toxicity screener covering leetspeak, spacing, and romanized forms. |
| [noelserdna/red-ciberseguridad-jev](https://github.com/noelserdna/red-ciberseguridad-jev) | Didactic project capturing packets with Wireshark/tshark and judging them from a cybersecurity perspective. |
| [michelbrigante46-art/Twitter-keyword-shield](https://github.com/michelbrigante46-art/Twitter-keyword-shield) | Userscript combining local rules with Jev decisions to block spam and hidden promotions on X. |

---

## 7. Classification, Extraction & Scoring

High-volume judgment calls: ticket triage, log classification, email and document categorization, field extraction, rubric scoring, and ranking.

| Project | What Jev decides |
| --- | --- |
| [superagents-lab/jev-search](https://github.com/superagents-lab/jev-search) | Query interpretation, source selection, and relevance ranking in a Cloudflare Worker search engine. |
| [kyotofin/tax-doc-classifier](https://github.com/kyotofin/tax-doc-classifier) | Classifies text-bearing PDF pages into IRS form and page-kind candidates behind a confidence gate. |
| [jexp/neo4jev](https://github.com/jexp/neo4jev) | Classifies neighboring graph relationships to navigate a Neo4j graph. |
| [parth-kp/jev-mail-classifier](https://github.com/parth-kp/jev-mail-classifier) | Classifies email and triggers configurable tag, move, flag, and notification actions. |
| [reachjalil/jevlogs](https://github.com/reachjalil/jevlogs) | Structured log-record questions, routing low-value records away from deeper LLM analysis. |
| [deepdave98/jev-playground](https://github.com/deepdave98/jev-playground) | Benchmarked inbound-lead triage reporting 90% routing accuracy at ~366 ms and $0.04 per thousand leads. |
| [RavioliCodes/jev-support-agents](https://github.com/RavioliCodes/jev-support-agents) | FastAPI + Ollama support system using Jev for routing, response evaluation, and retry/escalation, with a 60-ticket benchmark. |
| [rathan-bk/jev-ai-project](https://github.com/rathan-bk/jev-ai-project) | Alert triage proof of concept benchmarked against a rules-only baseline. |
| [tuhinmitra888/ai-jev-ticket-triage](https://github.com/tuhinmitra888/ai-jev-ticket-triage) | Classifies support tickets, then applies plain TypeScript routing rules. |
| [GhrezaKh74/JevTicktRouter](https://github.com/GhrezaKh74/JevTicktRouter) | .NET and React application for structured AI-powered ticket triage. |
| [alseif0x/jev-inbox-triage](https://github.com/alseif0x/jev-inbox-triage) | Two-phase inbox triage using a typed prefilter, confidence gating, and a pre-send guard. |
| [iikareem/skillfeed](https://github.com/iikareem/skillfeed) | Ranks a technology reading feed by the reader's declared skills. |
| [jasonli0226/jev-playground](https://github.com/jasonli0226/jev-playground) | Tests Jev as an incident-triage agent tool and as a gate for a smart model router. |
| [tjkimcloud/jev-site-auditor](https://github.com/tjkimcloud/jev-site-auditor) | Combines regex checks with Jev semantic judgments to score pages against custom brand and AEO rules. |
| [iamachilles/jev-gtm](https://github.com/iamachilles/jev-gtm) | Seven ready-made questions for GTM list qualification, deduplication, audience signals, and title sweeps, launched from CSV. |
| [arnab621/typesafe-jev-plugin](https://github.com/arnab621/typesafe-jev-plugin) | Runs reusable solution signatures over CSV, Excel, or text datasets and exports structured results. |
| [Simon-zj1/jev-exam](https://github.com/Simon-zj1/jev-exam) | Turns study material into self-tests and grades answers point by point with confidence gating and weak-area analysis. |
| [JeronimoRepetto/local-issue-classifier](https://github.com/JeronimoRepetto/local-issue-classifier) | Scores GitHub issues for complexity, criticality, effort, and relevance, with filtering, ranking, and export in the browser. |
| [wafaa-alhayek/masroufi](https://github.com/wafaa-alhayek/masroufi) | Categorizes household expenses from bank statement exports with confidence-aware transaction categories. |
| [vincenth19/are-they-into-you](https://github.com/vincenth19/are-they-into-you) | Cloudflare Workers demo combining typed answers with Workers AI OCR to assess pasted messages. |
| [ayushkushwaha609/Jev-resume-screener](https://github.com/ayushkushwaha609/Jev-resume-screener) | Resume screening using Jev typed judgments. |
| [gtaras7/typesafe-jev](https://github.com/gtaras7/typesafe-jev) | Screens a folder of CVs against an editable policy and re-scores candidates when the policy changes. |
| [ravikadam/jev-loan-triage](https://github.com/ravikadam/jev-loan-triage) | Assesses voice-call intent, information sufficiency, and a lending decision. |
| [0xZee/jev-stock-decision-maker](https://github.com/0xZee/jev-stock-decision-maker) | Combines market data with a 20-question assessment to score conviction, financial health, and risk. |
| [yasdelayu/jev-crypto-scout](https://github.com/yasdelayu/jev-crypto-scout) | Blends CoinGecko quant signals with Jev news judgments for sentiment, catalysts, and confirmation (not a trading bot). |
| [daisuke7/jevlergy](https://github.com/daisuke7/jevlergy) | Flutter iOS/Android project estimating food allergens from camera input. |
| [lirantal/discoprint](https://github.com/lirantal/discoprint) | Terminal dashboard classifying an artist's discography by theme, mood, and lyrical complexity. |
| [jexp/watfile](https://github.com/jexp/watfile) | Categorizes and sorts text or PDF files using Jev or a local calibrated decision model. |
| [schalkneethling/jev-lint](https://github.com/schalkneethling/jev-lint) | Experimental linter performing semantic code analysis. |
| [AkashPriyadarshii/jev-curate](https://github.com/AkashPriyadarshii/jev-curate) | Streaming filter and scorer for Parquet and JSONL datasets. |
| [koala73/worldmonitor](https://github.com/koala73/worldmonitor) | Batches headline-severity and topic classifications for a geopolitical dashboard, with validation and fallback. |
| [Eliot5566/JEV-Paper-Radar](https://github.com/Eliot5566/JEV-Paper-Radar) | Daily arXiv/bioRxiv radar asking one `Noul` per plain-English interest; publishes a must-read page and RSS (501 papers in 33 s for $0.0196). |
| [shimo4228/jev-research-pipeline](https://github.com/shimo4228/jev-research-pipeline) | Research monitor applying `Noul` gates and `Score` dimensions per paper, routing each pair to keep/review/drop. |
| [choxos/jev-reviewer](https://github.com/choxos/jev-reviewer) | Selects and verifies source lines for verbatim quotes in research documents; findings require human review. |
| [zzz1YAO/DataJev](https://github.com/zzz1YAO/DataJev) | Reads compressed analytical state and decides whether a data-analysis agent should continue, switch, verify, or stop. |
| [TKY-27/JevSlop](https://github.com/TKY-27/JevSlop) | Scores public articles on eight axes in a single request and reduces them to a 0–100 quality score. |

---

## 8. Search, Retrieval & Data Infrastructure

Semantic layers for data and search: DuckDB, PostgreSQL, MySQL, and Google Sheets integrations, RAG rerankers, and semantic grep over code and logs.

| Project | What it enables |
| --- | --- |
| [colliber/duckdb-jev](https://github.com/colliber/duckdb-jev) | DuckDB extension exposing Jev judgments as SQL values with return types derived from declared criteria. |
| [realZachi/pg-jev](https://github.com/realZachi/pg-jev) | PostgreSQL extension for semantic questions over individual table rows. |
| [giuliosmall/pg_typesafe](https://github.com/giuliosmall/pg_typesafe) | Pre-alpha PostgreSQL C extension exposing Choice, Noul, Score, and batched judgments from SQL. |
| [maayanlevy/mysql-ailike](https://github.com/maayanlevy/mysql-ailike) | MySQL plugin filtering rows by a natural-language predicate instead of a literal one. |
| [Cab14bacc/jev-sheets](https://github.com/Cab14bacc/jev-sheets) | Google Sheets custom functions (`JEV_IF`, `JEV_PROB`, `JEV_CHOICE`, `JEV_SCORE`) returning `UNSURE` below threshold. |
| [kylemclaren/jevql](https://github.com/kylemclaren/jevql) | psql-shaped client with Go/TypeScript/Python SDKs: plain SQL runs first, then Jev filters, sorts, or groups rows. |
| [EugeneBoondock/jevsql](https://github.com/EugeneBoondock/jevsql) | SQL-like filtering, ranking, classification, and scoring with natural-language predicates. |
| [kylemclaren/jevsearch](https://github.com/kylemclaren/jevsearch) | shadcn/ui site-search block: local keyword pass shortlists pages, then Jev answers per page and picks the best. |
| [kylemclaren/jevpdf](https://github.com/kylemclaren/jevpdf) | Browser PDF search where pdf.js extracts lines locally and one `Noul` per line decides relevance. |
| [WiktorB2004/llama-index-jev](https://github.com/WiktorB2004/llama-index-jev) | LlamaIndex reranker and selector using Jev Score and Choice answers with configurable confidence handling. |
| [hotchpotch/jev-reranker](https://github.com/hotchpotch/jev-reranker) | Retrieval reranker assessing documents for relevance and usefulness as answer evidence, with optional filtering. |
| [shinpr/jev-reranker](https://github.com/shinpr/jev-reranker) | Rust JSON-in/JSON-out CLI that reranks, filters, and compresses search results. |
| [fajarhide/askgrep](https://github.com/fajarhide/askgrep) | Searches code by questions that cannot be expressed as a text pattern. |
| [romeromarcelo/jev-retrieval](https://github.com/romeromarcelo/jev-retrieval) | Rust CLI: local BM25 recall, `Noul` window judgments, then a `Choice` rerank into `path:line` results. |
| [can1357/jegrep](https://github.com/can1357/jegrep) | Rust semantic grep scoring live repository files and ranges with probabilities — no embedding index or daemon. |
| [kyu1204/jgrep](https://github.com/kyu1204/jgrep) | Chunked semantic grep for files and diffs with grep-style exit codes, so CI lint rules can be written in English. |
| [allebee/jevgrep](https://github.com/allebee/jevgrep) | Streaming grep-by-meaning (one `Noul` per line) for logs and `tail -f` streams. |
| [mrnugget/jev-shell-history](https://github.com/mrnugget/jev-shell-history) | Ranks existing zsh history entries for inline completion; accepting a suggestion never executes it. |
| [tpellet/jevify](https://github.com/tpellet/jevify) | No-key CLI for finding errors in large logs, commits by description, and natural-language command search. |
| [altryne/jevify](https://github.com/altryne/jevify) | Agent skill that finds where a codebase could hand a decision to Jev and designs the typed questions. |
| [reachjalil/jev-tree](https://github.com/reachjalil/jev-tree) | Recursive choice over taxonomies larger than Jev's direct option limit. |
| [bartlomein/oko](https://github.com/bartlomein/oko) | Local code search shortlisting function-level chunks, then `Noul` relevance per chunk over MCP; cutoffs live in code. |
| [jerryjliu/docjev](https://github.com/jerryjliu/docjev) | Classifies documents against natural-language category rules or finds sub-document boundaries; a 40-document pilot classified 40/40 originals at ~182 ms p50. |
| [AkashPriyadarshii/jev-seo](https://github.com/AkashPriyadarshii/jev-seo) | Zero-cost SEO/GEO search radar CLI suite and MCP server built on DuckDuckGo plus Jev. |

---

## 9. Browser, Mobile & Computer Use

Computer use, browser agents, voice control, and content filters across macOS, Windows, Android, Chrome, and the web.

| Project | What Jev controls |
| --- | --- |
| [awlevin/typesafe-computer-use](https://github.com/awlevin/typesafe-computer-use) | macOS automation loop using OCR, action selection, and confidence gates, reserving a writing model for text fields. |
| [browser-use/jev-ultrafast](https://github.com/browser-use/jev-ultrafast) | Dynamic indexed action space with batched operation and DOM target decisions; includes traces and a measured demo. |
| [Ying-Kai-Liao/jev-browser](https://github.com/Ying-Kai-Liao/jev-browser) | Library, CLI, and MCP server combining LLM planning with Jev decisions for browser automation. |
| [timpratim/macbrow](https://github.com/timpratim/macbrow) | macOS tool where Jev selects tools and typed arguments in roughly 300 ms, reserving the LLM for text generation. |
| [trycua/cua](https://github.com/trycua/cua) | Open repository presenting CUA-S1, a System One-style model aimed at computer-use tasks. |
| [hqman/JevScout](https://github.com/hqman/JevScout) | Drives visible Chrome over CDP and scores links and job pages instead of letting the host LLM choose clicks. |
| [ibrahimhajjaj/barq](https://github.com/ibrahimhajjaj/barq) | MCP server, Claude Code plugin, library, and CLI selecting browser clicks toward a named outcome. |
| [jiangkoumo/ego-jev](https://github.com/jiangkoumo/ego-jev) | Drives the Ego Lite browser by turning an indexed element table into one operation and target (~2× faster than per-step LLM loops). |
| [flxbl-io/sf-autopilot](https://github.com/flxbl-io/sf-autopilot) | Salesforce autopilot: an LLM plans, Jev chooses each action, and Playwright executes. |
| [zurfyx/jev-browser-skill](https://github.com/zurfyx/jev-browser-skill) | Plug-and-play skill letting Jev drive browser interactions through Claude Code and Codex. |
| [0x7067/jev-browse](https://github.com/0x7067/jev-browse) | Browser automation using Jev as the decision model. |
| [cooper667/jev-browse](https://github.com/cooper667/jev-browse) | Plain-English browser QA for Claude Code, with judgments served through Cloudflare Workers AI. |
| [mjvmsteixeira/jev-browser-mcp](https://github.com/mjvmsteixeira/jev-browser-mcp) | Browser agent for Claude Code with domain guards, pauses before irreversible actions, and outcome verification. |
| [eralabs-ai/jev-dom](https://github.com/eralabs-ai/jev-dom) | Operates web pages through their DOM without relying on WebMCP. |
| [socai-io/jev-social](https://github.com/socai-io/jev-social) | Local Instagram/TikTok/LinkedIn research app selecting bounded browser operations from observed state. |
| [droidrun/mobile-jev](https://github.com/droidrun/mobile-jev) | Local Android agent and studio using Mobilerun; code rejects stale actions after the page changes. |
| [Friedjof/jev-mobile](https://github.com/Friedjof/jev-mobile) | Android agent making bounded per-step choices over prevalidated UI actions, with confidence gates and escalation. |
| [dougsong/jev-android](https://github.com/dougsong/jev-android) | Kotlin Android SDK for UI automation with an accessibility runtime and sample app. |
| [antiyro/jevdroid](https://github.com/antiyro/jevdroid) | Python framework choosing Android actions from accessibility trees, executed via ADB or UIAutomator2. |
| [Sur-Cai/macos-computer-use-kit](https://github.com/Sur-Cai/macos-computer-use-kit) | AX-first macOS computer-use kit with optional Jev semantic guards and read-back verification. |
| [moritzkremb/jev-voice-browser](https://github.com/moritzkremb/jev-voice-browser) | Maps partial speech transcripts to browser intents and observed targets, deciding whether to act, wait, or ask. |
| [chris-wozniczek/jev-voice-control](https://github.com/chris-wozniczek/jev-voice-control) | Swift menu-bar app converting speech into Jev decisions and then macOS actions. |
| [julianoczkowski/jev-demo](https://github.com/julianoczkowski/jev-demo) | Next.js demo combining local Whisper transcription, Jev, json-render, and shadcn/ui to turn speech into UI. |
| [RyanErkal/jevcast](https://github.com/RyanErkal/jevcast) | Native macOS launcher and window manager using Jev for natural-language matching. |
| [zbcoding/jev-userflow-browser-monitor](https://github.com/zbcoding/jev-userflow-browser-monitor) | Daily Jev + Playwright production user-flow checks running through GitHub Actions. |
| [JackLee992/jev-reflex-automation](https://github.com/JackLee992/jev-reflex-automation) | Fan-out decisions across Chrome, Android, and iOS, including canvas digitisation for games. |
| [adamnroman/slop-filter](https://github.com/adamnroman/slop-filter) | Chrome extension scoring and hiding AI-generated posts and comments on X, LinkedIn, and Reddit. |
| [harodggg/jev-x-filter](https://github.com/harodggg/jev-x-filter) | Chrome MV3 extension filtering X posts across six configurable categories, defaulting to rehearsal mode. |
| [fatsopanda-v3/jev-linkedin-slop](https://github.com/fatsopanda-v3/jev-linkedin-slop) | Chrome extension identifying AI-generated or low-quality content in LinkedIn feeds. |
| [kitze/unclutter](https://github.com/kitze/unclutter) | Browser extension identifying page clutter and saving reusable, reversible hiding rules. |
| [ufec/jev-block-android-ad](https://github.com/ufec/jev-block-android-ad) | Android app suppressing only notifications and SMS that Jev explicitly flags as noise, with a local pre-filter for verification codes. |

---

## 10. Agent Memory & Context Engineering

Memory admission, retrieval routing, context compaction, and agent wake gating — the long-context side of agent engineering.

| Project | What Jev governs |
| --- | --- |
| [kitfunso/hippo-memory](https://github.com/kitfunso/hippo-memory) | Zero-dependency SQLite/MCP memory system with an opt-in hosted Jev reranker and retrieval benchmarks. |
| [libingzheren/Jev-Mem](https://github.com/libingzheren/Jev-Mem) | Memory admission, graph relationships, retrieval routing, scoring, and stopping, while another model generates answers. |
| [Bonzokoles/36_chambers](https://github.com/Bonzokoles/36_chambers) | Routes agent queries across FTS5, ChromaDB, and graph backends, then reranks the evidence. |
| [tamaratran/fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction) | Claude Code plugin and TypeScript library that keeps, truncates, or drops older tool calls and results. |
| [HAR5HA-7663/jev-compact](https://github.com/HAR5HA-7663/jev-compact) | Claude Code tool that prunes rather than summarizes context, with Jev guiding what to compact. |
| [ljedrz/nachalnik](https://github.com/ljedrz/nachalnik) | kamchatka agent examples for Jev-assisted content-aware compaction and color-coded assisted shell. |
| [Asymptote-Labs/agent-beacon](https://github.com/Asymptote-Labs/agent-beacon) | Cross-harness memory: Jev judges bounded, redacted trace projections for reusable lessons that a person reviews before adoption. |
| [wojciechwiesner/jit-context](https://github.com/wojciechwiesner/jit-context) | Hermes JIT Context OS — just-in-time context assembly for agents. |
| [shitianfang/wakegate](https://github.com/shitianfang/wakegate) | Before a sleeping agent's LLM resumes, one `Choice` (wake / not yet / unrelated) decides whether to skip the wakeup, with a 21-scenario eval. |
| [thruwire/foreman](https://github.com/thruwire/foreman) | Experimental Codex/OpenCode supervisor sending bounded job, output, and diff context to Jev for progress checks. |
| [parkavenue9639/jevloop](https://github.com/parkavenue9639/jevloop) | Python agent runtime where Jev selects typed actions and targets, low confidence can trigger LLM arbitration, and a guarded kernel executes file/shell operations in Docker sandboxes. |
| [heliowap/delegador](https://github.com/heliowap/delegador) | Coding delegator choosing models per task with deterministic permissions, real-test verification, and escalation only after proven failure. |
| [lucianoon/backoffice-agents](https://github.com/lucianoon/backoffice-agents) | Back-office agent pilot where an LLM generates and reasons while Jev decides, routes, and verifies. |

---

## 11. Developer Utilities & CLIs

Command-line tools for piping typed judgments into shell scripts, CI pipelines, and coding agents.

| Project | Details |
| --- | --- |
| [okooo5km/jev](https://github.com/okooo5km/jev) | Shell tooling running typed judgments for tasks such as refund checks and review escalation, with TypeSafe and OpenRouter backends. |
| [shiftynick/jev-axi](https://github.com/shiftynick/jev-axi) | AXI-convention CLI giving agents judgments for blocking risky tool calls, screening fetched content, triaging build logs, and ranking items. |
| [joshLong145/jev-cli](https://github.com/joshLong145/jev-cli) | Command-line tool for interacting with the typed-decision model. |
| [andrueandersoncs/jev-cli](https://github.com/andrueandersoncs/jev-cli) | Sends typed questions about JSON state from the shell. |
| [tumf/jev-cli](https://github.com/tumf/jev-cli) | Small dependency-free CLI. |
| [saembit/jeff-cli](https://github.com/saembit/jeff-cli) | Go CLI scoring items on weighted dimensions from a YAML spec in one request; `noul`, `choice`, and `score` thresholds become exit codes. |
| [logicrw/ask-jev](https://github.com/logicrw/ask-jev) | Zero-dependency CLI routing small semantic judgments (Choice, Noul, Score, batches, verbatim extraction) for agents and pipelines. |
| [andududu/jeview](https://github.com/andududu/jeview) | Loopback proxy and live map of Jev calls, grouping decisions by project and linking later calls to earlier answers (local SQLite; keep off public addresses). |
| [RevocGG/typesafe-jev-bridge](https://github.com/RevocGG/typesafe-jev-bridge) | Zero-dependency OpenAI-compatible CLI and HTTP bridge exposing typed judgments to 9Router, Claude Code, Cursor, Cline, and OpenAI SDK clients. |
| [sutro-sh/jev-align](https://github.com/sutro-sh/jev-align) | Active-learning CLI evaluating CSV/Parquet/JSONL, surfacing uncertain or audited rows for human labelling, and proposing improved definitions for review. |
| [jyatesdotdev/jev-logtriage](https://github.com/jyatesdotdev/jev-logtriage) | Scores collapsed Loki log batches for noise, severity, and actionability, then maps answers to suppress, watch, review, notify, or page. |
| [KNambiarDJsc/second-thought](https://github.com/KNambiarDJsc/second-thought) | Python SDK, CLI, and dashboard capturing typed decisions, measuring calibration, and routing uncertain cases to human review. |
| [evoke-build/evoke](https://github.com/evoke-build/evoke) | Turns sentences into calls to small programs selected by Jev, with shareable reflex recipes, a Git package manager, a CLI, and a TypeScript SDK. |

---

## 12. Applications & End-User Tools

Finished end-user tools: email clients, PDF form fillers, YouTube sponsor skipping, writing scores, and interactive demos.

| Project | What it does |
| --- | --- |
| [fazlerocks/jevmail](https://github.com/fazlerocks/jevmail) | Open-source local Gmail client assigning inbox trays, urgency, and human-sent likelihood with read-only Gmail access. |
| [kellystuard/jev-gmail-classifier](https://github.com/kellystuard/jev-gmail-classifier) | Google Apps Script classifying email with typed answers and applying Gmail labels under confidence thresholds. |
| [bquigley1/jev-imap-router](https://github.com/bquigley1/jev-imap-router) | Sorts IMAP inboxes into plain-English categories with preview-first operation; never deletes mail. |
| [takumi-golf/jev-fill-pdf](https://github.com/takumi-golf/jev-fill-pdf) | Browser app filling Japanese government PDF forms using Jev for labels while user values stay local; supports OCR. |
| [Manta-Boardgame/jev-chat](https://github.com/Manta-Boardgame/jev-chat) | Windows and Android app answering questions about books and office documents, with probabilities and on-device OCR. |
| [ycs77/jev-girlfriend-analysis](https://github.com/ycs77/jev-girlfriend-analysis) | Chinese-language app inferring likely intent from messages. |
| [cocktailpeanut/jevthoven](https://github.com/cocktailpeanut/jevthoven) | Symbolic-music studio where Jev chooses plans, instruments, and bar patterns, and code renders editable music and MIDI. |
| [achimala/jev-paint](https://github.com/achimala/jev-paint) | Local browser app turning batched per-pixel Jev distributions into paintings; prompts describe pixels and regions rather than raw images. |
| [valentynkit/jev-skip](https://github.com/valentynkit/jev-skip) | Browser extension painting a per-segment sponsor probability on the YouTube seek bar (caught 77% of SponsorBlock's sponsor seconds across 23 videos at $0.0008 per video). |
| [trungdq88/youtube-sponsor-detection](https://github.com/trungdq88/youtube-sponsor-detection) | Finds sponsor reads in transcripts or transcribed audio while code owns timestamps and playback skipping. |
| [ChetasLua/jevmeter](https://github.com/ChetasLua/jevmeter) | Scores every sentence in a video and renders the result as a shareable overlay. |
| [Dearest/plotveil](https://github.com/Dearest/plotveil) | Chrome extension guarding YouTube comments against concrete plot spoilers, keeping comments covered when checks fail. |
| [harshil1712/slidepilot](https://github.com/harshil1712/slidepilot) | Experimental Slidev controller judging speech transcripts for slide completion, with deterministic checks and manual navigation. |
| [cwdx/1-million-emojis](https://github.com/cwdx/1-million-emojis) | Shared 1000 × 1000 emoji canvas where Jev joins each stroke by choosing a square and an emoji as one `Choice`. |
| [cwdx/chess-with-jev](https://github.com/cwdx/chess-with-jev) | Jev chooses one move per turn from legal moves described with code-computed facts; the page draws its candidates as arrows. |
| [ayyazzafar/needle-jev](https://github.com/ayyazzafar/needle-jev) | Find-in-page tool using Jev semantic search with the user's own API key. |
| [amycardoso/jev-palette](https://github.com/amycardoso/jev-palette) | Command palette turning one `Choice` over a 77-command catalog into per-keystroke ranking, with a fuzzy-match baseline shown side by side. |
| [mcgalleg/grokbot-jev-jobs](https://github.com/mcgalleg/grokbot-jev-jobs) | Daily Vercel cron scoring public job postings against one resume so only plausible matches surface. |
| [narceliosousa-coder/jev-architecture-3d](https://github.com/narceliosousa-coder/jev-architecture-3d) | Interactive 3D scene presenting the system architecture of the Jev System One model. |
| [RiwRiwara/jev-computer](https://github.com/RiwRiwara/jev-computer) | Hardware experiment implementing an 8-bit computer from 2,102 NAND gates generated by one Jev yes/no decision. |
| [pc418/jev-calculator](https://github.com/pc418/jev-calculator) | Calculator with no arithmetic code: one `Choice` over 13 options per answer character, exposing step-by-step probabilities and call-to-call jitter. |
| [waynesutton/ask-jev-ai](https://github.com/waynesutton/ask-jev-ai) | Realtime public wall for short yes/no/depends judgments, tracking cumulative cost toward one million asks. |

---

## 13. Games, Simulation & Robotics

Games, simulations, and robots where Jev chooses actions — the most latency-sensitive corner of the ecosystem.

| Project | What it demonstrates |
| --- | --- |
| [Atikpui007/clash-jev](https://github.com/Atikpui007/clash-jev) | Clash Royale bot making every decision from live game state without a trained policy. |
| [GabrielBigardi/TibiaJevBot](https://github.com/GabrielBigardi/TibiaJevBot) | Autonomous game-playing decision engine for Tibia/Open Tibia. |
| [Zboubkiller/jev-plays-sts2](https://github.com/Zboubkiller/jev-plays-sts2) | Controls gameplay in Slay the Spire 2 using fast classification decisions without text generation. |
| [GitNimay/jev-plays-tetris](https://github.com/GitNimay/jev-plays-tetris) | Live Tetris choosing every move through Vercel AI Gateway. |
| [rishi-raj-jain/flappy-jev](https://github.com/rishi-raj-jain/flappy-jev) | Real-time Flappy Bird racing the player against a Jev-controlled bird (Next.js + Neon Postgres). |
| [dperezcabrera/jev-chess](https://github.com/dperezcabrera/jev-chess) | Chess game against Jev via OpenRouter, built with the pico framework. |
| [mansicer/jev-plays](https://github.com/mansicer/jev-plays) | Plays Craftax while an LLM sets goals and Jev chooses actions. |
| [tatsuo48/jev-poc](https://github.com/tatsuo48/jev-poc) | Go CLI and Cloudflare Workers web demo playing 2048. |
| [deemkeen/jevgeni](https://github.com/deemkeen/jevgeni) | Voice-only claw machine combining Jev decisions with Whisper v3 Turbo through Groq. |
| [KeWang0622/jev-board-game](https://github.com/KeWang0622/jev-board-game) | Instruments Undercover, Werewolf, and Avalon with calibrated decisions, treating belief as a game primitive. |
| [AppChainAI/Jevatar](https://github.com/AppChainAI/Jevatar) | React companion mapping each message to one of 14 facial moods, driving a morphing avatar. |
| [southleft/component-charades](https://github.com/southleft/component-charades) | Taboo-style parlour game where Jev referees component-charades rounds for design systems. |
| [mikecann/magic-jev-ball](https://github.com/mikecann/magic-jev-ball) | three.js Magic 8 Ball asking one `Choice` over the 20 classic answers and showing every probability. |
| [spoonnotfound/soupbase](https://github.com/spoonnotfound/soupbase) | Lateral-thinking puzzle engine requiring supported facts, a coherent explanation, and sufficient confidence before marking a puzzle solved. |
| [skcache/jevtrafficsim](https://github.com/skcache/jevtrafficsim) | Applies Jev to simulate traffic across an entire city. |
| [kavehmz/typesafe-playground](https://github.com/kavehmz/typesafe-playground) | Interactive experiments including support routing and 3D driving simulations with visible sensor inputs. |
| [Didixdan/jev-games-poc](https://github.com/Didixdan/jev-games-poc) | Proof of concept showing multiple games solved with the System One model. |
| [tomerab1/vampire-survivor](https://github.com/tomerab1/vampire-survivor) | Rust/Bevy horde-survival game for native and WASM where Jev directs the horde. |
| [OuchengLiu/Jev-Game-Theory-Arena](https://github.com/OuchengLiu/Jev-Game-Theory-Arena) | Browser arena for poker, liar's dice, and prisoner's dilemma where Jev assigns probabilities to legal moves (educational, no real money). |
| [sorrycc/typesafe-snake](https://github.com/sorrycc/typesafe-snake) | Browser Snake where code computes legal moves, food distance, and reachable space, then Jev picks one move per tick. |
| [phyous/tsai-sc](https://github.com/phyous/tsai-sc) | Structured-state harness controlling original StarCraft shareware, with a verified run, probability trace, and evidence bundle. |
| [fhshaik/typesafe-mario](https://github.com/fhshaik/typesafe-mario) | Super Mario Bros. agent choosing actions from structured emulator state. |
| [anxkhn/jevplayspokemon](https://github.com/anxkhn/jevplayspokemon) | Playable demonstration of Jev driving a Pokémon run. |
| [dperezcabrera/system-one-poker](https://github.com/dperezcabrera/system-one-poker) | Routes Texas Hold'em decisions through Jev and compares results with expected value. |
| [TomRichner/can-jev-bayes](https://github.com/TomRichner/can-jev-bayes) | Tests whether Jev can solve Bayesian decision problems, contrasting outputs with optimal strategies. |
| [robokrunch/jev-physical-ai](https://github.com/robokrunch/jev-physical-ai) | Reproducible warehouse-fleet triage demo with 300 Jev calls, raw results, and a local-model cost comparison (simulated incidents, no hardware). |
| [lykycy123/RoboJEV](https://github.com/lykycy123/RoboJEV) | Two-stage `Choice` decisions over structured state selecting intent and Cartesian motion/gripper commands for a Franka Panda in MuJoCo, with independent physics-based success checks. |
| [RomanSlack/jev-drone](https://github.com/RomanSlack/jev-drone) | Simulated MuJoCo quadrotor where Jev makes slower tactical judgments from processed camera observations while deterministic code flies. |
| [kxzk/typesafe-jev-drone-demo](https://github.com/kxzk/typesafe-jev-drone-demo) | Three.js drone simulator with a Python backend where Jev drives navigation decisions. |
| [tfolkman/jev-village](https://github.com/tfolkman/jev-village) | Village simulation sending every decision to Jev, with live cost comparisons against frontier LLMs. |
| [az9713/jev-projects](https://github.com/az9713/jev-projects) | Demo collection via Vercel AI Gateway including a wiki race, a town of agents, and bullet chess. |
| [nikhil1raghav/jev-playground](https://github.com/nikhil1raghav/jev-playground) | Toy projects including a Snake autopilot, Todoist sorter, Hacker News re-ranker, and a Dangerous Dave autopilot. |

---

## 14. Trading & Financial Applications

Trading and finance applications: pre-trade gates, paper-trading desks, and sentiment-assisted decision cards.

| Project | What Jev decides |
| --- | --- |
| [OpenByteInc/QuantDinger](https://github.com/OpenByteInc/QuantDinger) | Pre-trade gate evaluating order and risk context, recording probabilities and confidence, and failing open on provider failure while exits stay ungated. |
| [jarrodwatts/jev-trader](https://github.com/jarrodwatts/jev-trader) | Buy/sell decisions for a Kuru/Monad on-chain order book; defaults to a mock model and dry-runs without a private key. |
| [Jev-trading/Jev-trading](https://github.com/Jev-trading/Jev-trading) | Visual desktop platform combining Jev with algorithmic-trading tools. |
| [aowang-ai/jev-trade](https://github.com/aowang-ai/jev-trade) | Hyperliquid desk asking `Choice` questions for long/short, open/close/hold, and leverage; defaults to dry run. |
| [original0211/jev-perp-paper-trader](https://github.com/original0211/jev-perp-paper-trader) | Crypto perpetuals simulation dashboard routing decisions through Jev; paper trading only, no real orders. |
| [markusbug/jevymarket](https://github.com/markusbug/jevymarket) | Polymarket trading bot driving decisions through Jev via OpenRouter. |
| [brainstormity/Jev-X-Sentiment-Analysis](https://github.com/brainstormity/Jev-X-Sentiment-Analysis) | Ingests 50–1,000 tweets per request through statistical pre-processing and SQLite deduplication, then produces a decision card with entry ranges, stop losses, and targets — without executing trades. |
| [AlgoVaultLabs/algovault-integrations](https://github.com/AlgoVaultLabs/algovault-integrations) | `examples/typesafe-jev`: decides whether to act on a composite market verdict and how well a regime fits a directional entry; read-only, dry-run, never places orders. |

---

## 15. Open Models & Local Inference

Jev-compatible servers, retrained decision heads, and adapters that reproduce the typed-decision interface without the hosted API. Independent efforts — not official TypeSafe releases or verified reproductions of its architecture or training. Useful when you need offline inference, private processing, zero per-call cost, or a research baseline against hosted Jev.

| Project | Approach |
| --- | --- |
| [Heman10x-NGU/Verdict-open-jev](https://github.com/Heman10x-NGU/Verdict-open-jev) | 151M non-autoregressive ModernBERT decision engine with calibrated uncertainty, a benchmark audit, and an in-browser WebGPU playground. |
| [Heman10x-NGU/openJev-verdict-2.0](https://github.com/Heman10x-NGU/openJev-verdict-2.0) | Successor with separate distribution and confidence heads, saved evaluation artifacts, public weights, and a WebGPU demo. |
| [emnlmn/snap](https://github.com/emnlmn/snap) | Local, deterministic typed decisions from unstructured state in one forward pass, explicitly Jev-compatible. |
| [Mushroom-Systems/lichen](https://github.com/Mushroom-Systems/lichen) | Local project intended as an API-compatible replacement for Jev. |
| [GitHub30/OpenJev](https://github.com/GitHub30/OpenJev) | Open-weight model implementing calibrated Noul/Choice/Score in one forward pass, aiming to work with the TypeSafe SDK unchanged. |
| [razorback16/openjev](https://github.com/razorback16/openjev) | Independent Jev-compatible server over DiffusionGemma/vLLM (documented custom vLLM patches). |
| [ekzhang/openjev-sglang](https://github.com/ekzhang/openjev-sglang) | Jev-compatible API endpoint backed by open models and prefill-only inference. |
| [TheoLeeCJ/SemIf-OpenJev](https://github.com/TheoLeeCJ/SemIf-OpenJev) | Independent replication on open models with an MLX backend, measuring that typed decisions arrive together while JSON streams token by token. |
| [Lasimeri/Intel-Phi-Jev](https://github.com/Lasimeri/Intel-Phi-Jev) | Serves Noul/Choice/Score judgments locally, offloading matrix work to Intel Xeon Phi cards. |
| [ollaya-dev/ollaya](https://github.com/ollaya-dev/ollaya) | Rust daemon and CLI pulling open decision models by name and serving `/v1/systemone`, `/v1/decisions`, and `/v1/models` behind a TypeSafe-compatible surface (answers come from open models, not Jev). |
| [zhengxuyu/litjev](https://github.com/zhengxuyu/litjev) | Turns any Qwen model into a fast decision model serving the same `/v1/systemone` schema with no training. |
| [bnsd55/jevmlx](https://github.com/bnsd55/jevmlx) | Jev-style parallel constrained decisions for MLX models on Apple Silicon. |
| [jaredpalmer/kev](https://github.com/jaredpalmer/kev) | Qwen2.5-0.5B adapter and decision head with training code, released weights, and parallel typed-question inference. |
| [tamnd/kime-compat](https://github.com/tamnd/kime-compat) | 48-requirement spec of the `POST /v1/systemone` wire contract plus a conformance suite for any Jev-compatible server, with a deliberately broken mock and a fixing proxy. |
| [vladvlsu/jev_ollama_ornith](https://github.com/vladvlsu/jev_ollama_ornith) | FastAPI server connecting an Ollama-hosted model to the TypeSafe SDK interface. |
| [b0bleet/syn](https://github.com/b0bleet/syn) | Open System One-compatible API emitting typed decisions from next-token probabilities in one forward pass. |
| [Sharkelot/jev-laya-free](https://github.com/Sharkelot/jev-laya-free) | Free local Jev-compatible decisions with a TypeSafe-SDK-compatible Python surface and deterministic guards. |
| [MorrisZJ/AnyJev](https://github.com/MorrisZJ/AnyJev) | Turns any transformers or vLLM model into a Jev-style decision source using cyclic-shift marginalization and label-free prior estimation, with order-flip/Brier/ECE benchmarks. |
| [izam-mohammed/decisionsmith](https://github.com/izam-mohammed/decisionsmith) | Tools for using and fine-tuning System One models on custom data with an LLM as teacher. |
| [hulryung/jev-testbed](https://github.com/hulryung/jev-testbed) | Runs hosted Jev and self-hosted alternative examples side by side and reports measured results for both paths. |
| [Code-Forge-AU/jev-llm](https://github.com/Code-Forge-AU/jev-llm) | Experiment generating text word-by-word via choice selection and candidate reranking, without a drafting LLM. |
| [islee23520/omo-jevlike-router](https://github.com/islee23520/omo-jevlike-router) | Shrinks a skill catalog in the system prompt with one forward pass over a frozen Qwen, routing Jev-style. |
| [genai-craft/openvons](https://github.com/genai-craft/openvons) | Open decision layer for finite options across text, images, and Japanese voice commands. |

---

## 16. Benchmarks, Evaluations & Research

Independent benchmarks, calibration and robustness studies, audits, and research artifacts — including runs where Jev lost.

| Project | What it measures |
| --- | --- |
| [priorbench/jev](https://github.com/priorbench/jev) | Pre-registered independent evaluation: 5,721 calls, 21 experiments, 50 predictions registered before data collection, raw data included. |
| [iammrduncan/typesafe-ai-benchmark](https://github.com/iammrduncan/typesafe-ai-benchmark) | Compares direct Jev calls with Qwen structured output, preserving validated responses, raw requests, and timings. |
| [TheWayWithin/jev-bench](https://github.com/TheWayWithin/jev-bench) | 42-claim fact-verification benchmark comparing Jev with GPT-5.4, Claude Sonnet 5, and Gemini 3.1 Pro. |
| [4esv/jev-eval](https://github.com/4esv/jev-eval) | Independent Jev vs GPT-5.6 Terra comparison across three labeled classification tasks (accuracy, calibration, latency, cost). |
| [vinilana/jev-eval-agent](https://github.com/vinilana/jev-eval-agent) | Compares LLM tool selection with Jev routing in a personal-assistant harness containing 100 mocked tools. |
| [blowxian/jev-fanout-bench](https://github.com/blowxian/jev-fanout-bench) | Reproducible batched-vs-single-question comparison; a 2,976-request run reports ~261 fixed input tokens per request. |
| [assembledadam/typesafe-jev-benchmark](https://github.com/assembledadam/typesafe-jev-benchmark) | Inbox benchmark testing System One models (Jev, EigenJev, Kev). |
| [dm8000/Metapicker](https://github.com/dm8000/Metapicker) | Systematic-review screening benchmark against DeepSeek V4 Flash and Qwen3-Reranker using documented author judgments. |
| [sksq96/jevgram](https://github.com/sksq96/jevgram) | Pangram-style detection benchmark across 7,139 RAID, HC3, and MAGE texts using one typed question per text for $0.97. |
| [OrMizL/jev-skill-router-bench](https://github.com/OrMizL/jev-skill-router-bench) | Independent benchmark of a Jev skill router across 81 labelled turns, with an inconclusive agent-level analysis. |
| [AnilDeshpande/jev-youtube-demo](https://github.com/AnilDeshpande/jev-youtube-demo) | Compares Jev and GPT-4o-mini for classifying YouTube comments with typed outputs. |
| [jmanhype/jev-dspy-lab](https://github.com/jmanhype/jev-dspy-lab) | Reproducible calibration and selective-risk benchmarks for Jev decisions integrated into DSPy workflows. |
| [JustinDumasCarr/Jev](https://github.com/JustinDumasCarr/Jev) | Compares Jev with Claude models on prompt-injection validation and skill routing across 1,000 labelled cases per task. |
| [shaifulshabuj/jev-test](https://github.com/shaifulshabuj/jev-test) | Empirical benchmarks, task telemetry, and an engineering thesis about Jev in autonomous agentic organizations. |
| [Jevals/jevals-data](https://github.com/Jevals/jevals-data) | Per-decision logs behind an independent benchmark grading hosted Jev and six LLMs on the same Noul, Choice, and Score questions. |
| [Pasblinn/jev-lab](https://github.com/Pasblinn/jev-lab) | Open lab for measured Jev routing bugs, a patch, hard fallback behavior, and alerts in front of Claude Code. |
| [moguone/jev-lab](https://github.com/moguone/jev-lab) | Collection of small unofficial applications for evaluating Jev. |
| [vpicone/jev-lab](https://github.com/vpicone/jev-lab) | Test bench for Jev on Vercel AI Gateway. |
| [itani404/jev-explained](https://github.com/itani404/jev-explained) | Hands-on explainer with examples, a playground, and independent benchmark results. |
| [WallerChen/jev-measured](https://github.com/WallerChen/jev-measured) | Reproducible measurement of live API costs, latency, network overhead, and response-shape pitfalls across eight use cases. |
| [Zaious/jev-capability-atlas](https://github.com/Zaious/jev-capability-atlas) | Bilingual evidence map with recorded API runs and reusable suites, separating own tests, third-party benchmarks, and editorial synthesis. |
| [abhixhek/jevcal](https://github.com/abhixhek/jevcal) | Fits per-question confidence thresholds to a target accuracy on labelled data, verifies on a held-out split, and re-checks in CI. |
| [stillmarcus24/jev-verify](https://github.com/stillmarcus24/jev-verify) | Recomputes confidence and expected-score identities against outputs published in public repositories. |
| [BFLabsAI/bf-jev-deep-research](https://github.com/BFLabsAI/bf-jev-deep-research) | Agent skill plus a verbatim study covering typed questions, RLCD, usage patterns, and the SDK ecosystem. |
| [brian-w-zhang/askjev](https://github.com/brian-w-zhang/askjev) | Tree of closed questions answered by Jev to document capabilities, defaults, and jaggedness (explicitly not a benchmark). |
| [rubinagentagi-tech/jev-heart-risk-bench](https://github.com/rubinagentagi-tech/jev-heart-risk-bench) | Benchmarks Jev on 5,000 real CDC survey respondents with an interactive demo of model answers per profile. |
| [mori-ikuri/jev-divination-lab](https://github.com/mori-ikuri/jev-divination-lab) | Research lab comparing independent divination readings on shared axes. |

---

## 17. Learning Resources, Cookbooks & Examples

Cookbooks, tutorials, notebooks, translations, and reference demos for learning Jev quickly.

| Project | What it teaches |
| --- | --- |
| [nexibeo/jev-cookbook](https://github.com/nexibeo/jev-cookbook) | Fifteen runnable recipes for support triage, data cleanup, search, browser actions, and Gmail labelling, with small labelled samples and saved live results. |
| [paramjeetn/jev-cookbook](https://github.com/paramjeetn/jev-cookbook) | 120+ use cases, 10 runnable examples, composition patterns, and first-principles theory. |
| [agencyenterprise/jev-recipes](https://github.com/agencyenterprise/jev-recipes) | 200+ reusable recipes for routing, grading, gating, comparison, and labelling, callable from JS/TS or a JSON CLI. |
| [ReallyArtificial/jev-by-example](https://github.com/ReallyArtificial/jev-by-example) | Ten JavaScript lessons pairing typed questions with explicit application policies; offline fixtures by default, live calls opt-in. |
| [harshithsunku/learn-jev-end-to-end](https://github.com/harshithsunku/learn-jev-end-to-end) | Twelve Python notebooks putting Jev inside a hand-rolled LLM agent loop as router, tool-call guard, done gate, and judge, with comparisons against two LLMs. |
| [rickysullivan/typesafe-tutorial](https://github.com/rickysullivan/typesafe-tutorial) | Notebooks created while learning Jev. |
| [miounet11/jevcode](https://github.com/miounet11/jevcode) | Chinese-language technical solutions and best practices with a companion site. |
| [Bald0Wang/jev-docs-zh](https://github.com/Bald0Wang/jev-docs-zh) | Unofficial Chinese translation of the official Jev documentation. |
| [datawhalechina/jev-cookbook](https://github.com/datawhalechina/jev-cookbook) | Unofficial Chinese translation of the Jev documentation. |
| [lnuxe/typesafe-docs-zh](https://github.com/lnuxe/typesafe-docs-zh) | Mintlify-powered Simplified Chinese documentation site for TypeSafe AI. |
| [thiagoadril/typesafe-docs](https://github.com/thiagoadril/typesafe-docs) | TypeSafe AI and Jev documentation extracted as Markdown for LLM use and training. |
| [api-evangelist/typesafe-ai](https://github.com/api-evangelist/typesafe-ai) | Documents TypeSafe AI, the System One endpoint, and the typed decision interface. |
| [replynodes/jev-web-analyzer](https://github.com/replynodes/jev-web-analyzer) | Inspectable Next.js demo fetching public page Markdown and exposing Boolean, Choice, Score, probability, and streaming results via Vercel AI Gateway. |
| [Ashadeepa/typesafe-showcase](https://github.com/Ashadeepa/typesafe-showcase) | Deployable Next.js UI demonstrating parallel Noul judgments and a Choice-based citation checker. |
| [Quintui/jev-use-cases](https://github.com/Quintui/jev-use-cases) | Demo application presenting Jev use cases with the AI SDK and shadcn/ui. |
| [vamsikrishna2421/jev-usecases](https://github.com/vamsikrishna2421/jev-usecases) | Catalogs real-world builds, cost calculations, design patterns, and a critical assessment of vendor claims. |
| [naveenreddy61/jev-experiments](https://github.com/naveenreddy61/jev-experiments) | Collected experiments with the Jev/System One model. |
| [dabit3/jev-experiments](https://github.com/dabit3/jev-experiments) | Twenty-two latency-focused Jev applications, each with its own README and testing notes: shell guards, log sentinels, instant search, reranking, and voice turn-taking. |
| [rajivkuriakose/typesafe-jev-examples](https://github.com/rajivkuriakose/typesafe-jev-examples) | Runnable OpenRouter examples asking seven parallel questions to route tickets and assess impact, churn risk, and billing confidence. |
| [GiesN/typesafe-jev-workflow](https://github.com/GiesN/typesafe-jev-workflow) | LangGraph email-intent workflow built around one typed Jev choice. |
| [matthewp/flue-jev-demo](https://github.com/matthewp/flue-jev-demo) | Routes a Flue agent's work with Jev through Cloudflare AI Gateway. |

---

## Frequently Asked Questions

### What is Jev by TypeSafe AI?

Jev is TypeSafe AI's flagship **System One** model: a hosted model that returns **typed, calibrated decisions** instead of generated text. You send a piece of *state* (text, JSON, or a document) along with *typed questions*, and Jev answers with constrained values — an option, a level, or a probability — each with confidence your code can gate on. It targets classification, routing, scoring, verification, and guardrails rather than conversation.

### What are Choice, Score, and Noul?

They are Jev's three question primitives. **`Choice`** picks one option from a set you define and returns a probability for every option plus a confidence. **`Score`** rates the state on an ordered scale and returns a probability-weighted position. **`Noul`** answers a yes/no question with a single probability between 0 and 1 — the value *is* the answer, and no separate confidence is returned. The [official primitives reference](https://docs.typesafe.ai/primitives) documents each one.

### How is Jev different from an LLM such as GPT or Claude?

An LLM generates free text, so any structured value has to be parsed back out and validated. Jev never generates text: its output space is closed by the questions you supply, so answers are directly consumable by code. In production the two are usually combined — a generative model writes and reasons, while Jev makes the many small decisions inside the loop. [Framework & Platform Integrations](#3-framework--platform-integrations) collects integration patterns.

### Is Jev open source?

Jev itself is a hosted, closed-weights model from TypeSafe AI. Its **SDKs and the ecosystem around it are open source**, and independent projects reimplement a Jev-compatible `/v1/systemone` interface on open models — see [Open Models & Local Inference](#15-open-models--local-inference) — for offline, private, or zero-per-call use. Every entry in this directory is a public GitHub repository.

### How do I use Jev from Python or TypeScript?

Install an official SDK — [`typesafe-sdk` for Python](https://github.com/typesafe-ai/typesafe-sdk-python) or the [TypeScript/JavaScript SDK](https://github.com/typesafe-ai/typesafe-sdk-js) — define a typed question set, and call `system_one` / `systemOne` with your state. Community ports cover Go, Rust, Java, Kotlin, Scala, .NET, Ruby, PHP, Elixir, Haskell, and more in [Language SDKs & Client Libraries](#2-language-sdks--client-libraries).

### Where can I find Jev examples, cookbooks, and demos?

Start with [Learning Resources, Cookbooks & Examples](#17-learning-resources-cookbooks--examples), the [official playground](https://github.com/TypeSafeAI/typesafe-playground), and the community cookbooks with runnable recipes. Each entry here includes a one-line summary of what Jev decides and what the surrounding code does with the answer.

### Does Jev replace my LLM?

No — Jev is a **decision layer**, not a generator. The recurring pattern across the projects in this directory is *generative model does the writing, Jev does the judging*: routing, classifying, scoring, gating, and verifying. [Benchmarks, Evaluations & Research](#16-benchmarks-evaluations--research) collects independent comparisons, including results where classical classifiers or LLMs beat Jev on specific tasks.

### Why does this directory list GitHub projects only?

So that every entry is verifiable. Articles, videos, and forum posts rotate or disappear, and they cannot be inspected the way a repository can — they are credited as discovery sources in [Sources & Acknowledgements](#sources--acknowledgements) but never listed as entries. That also makes this a **GitHub-only alternative to awesome-style indexes** that mix formats.

### How do I get a Jev project listed here?

See [Contributing](#contributing): a public repository, genuine Jev (or documented Jev-compatible) usage, an inspectable decision path, and one factual line. Additions, corrections, and removals are all welcome.

---

## Contributing

Contributions are welcome — additions, corrections, and removals alike. The full guidelines live in [`CONTRIBUTING.md`](CONTRIBUTING.md).

**To add a project**, open a pull request that edits the most relevant section of this README, following this format:

```md
| [owner/repo](https://github.com/owner/repo) | One factual sentence: what Jev decides and what the surrounding code does with the answer. |
```

**Please ensure the entry meets all of the following:**

1. **Public GitHub repository** with a working URL.
2. **Genuine Jev (or documented Jev-compatible/derivative) usage** — not a generic classifier, router, or LLM judge.
3. **An inspectable decision path** — a typed question, a typed answer (with probability or confidence), and code that gates, routes, or acts.
4. **One line only**, written factually, with limitations noted when known.
5. **No duplicates** — the project must not already appear in another section.

**Review expectations**

- Maintainers may request a link to the specific file that calls Jev, an evaluation artifact, or clearer wording around limitations.
- Claims of accuracy, latency, or cost should be traceable to the linked repository.
- Descriptions are summarized for this index and must not be copied verbatim from project READMEs.

> A listing is **not** an endorsement. This directory applies inclusion rules only; it does not review code quality, security, maturity, or whether a project runs at all — and it is not affiliated with TypeSafe AI.

---

## Sources & Acknowledgements

This directory is compiled from public GitHub repositories, cross-checked against community indexes and trackers. The following community resources were used as **sources** for discovery (they are indexes, not listed entries here):

<table>
<tr><td><a href="https://jessie.romeos.cc/full/apps/jev-tracker">jessie.romeos.cc — Jev tracker</a></td><td>Daily scan across GitHub, Reddit, Hacker News, YouTube, and the web; the durable copy is the <a href="https://github.com/Jessie-QingYu/jev-in-the-wild">jev-in-the-wild</a> data repository.</td></tr>
<tr><td><a href="https://jev-directory.com/">jev-directory.com</a></td><td>Community project showcase with copyable examples (source repository: <code>kong75/jev-directory</code>).</td></tr>
<tr><td><a href="https://www.jevdirectory.org/">jevdirectory.org</a></td><td>Curated resource directory covering repos &amp; SDKs, practices, guides, cookbooks, and tools.</td></tr>
<tr><td><a href="https://github.com/cobanov/awesome-jev">cobanov/awesome-jev</a></td><td>Source-backed list with dated research notes and pinned evidence.</td></tr>
<tr><td><a href="https://github.com/yibie/awesome-jev">yibie/awesome-jev</a></td><td>Fast-scanning field guide with category files and a tag-audit script.</td></tr>
<tr><td><a href="https://github.com/AbdelStark/awesome-typesafe-jev">AbdelStark/awesome-typesafe-jev</a></td><td>Field guide with per-project pages, action policies, and caveats.</td></tr>
</table>

**Not affiliated with TypeSafe AI.** Jev and System One are products and trademarks of TypeSafe AI. All linked projects belong to their respective authors under their own licenses.

---

## License

Released under the [MIT License](LICENSE).

Copyright (c) 2026 MicroDeft
