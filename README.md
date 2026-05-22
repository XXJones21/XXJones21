
# Joshua Jones

AI engineer working on the reasoning layer that makes LLMs reliable on long-horizon work. Currently at Meta as an Information Solutions Engineer. Background spans full-stack Rust and Python, the behavioral science of LLM reasoning, and a decade of decomposing complex systems into precise, actionable instructions -- the foundational craft of context engineering for agents.

Santa Clara, CA - [LinkedIn](https://www.linkedin.com/in/joshua-jones-57115382/) - [@MrSwazzy21](https://twitter.com/MrSwazzy21)

---

## What I'm building

The thread connecting the projects below: reasoning quality, expressed through a domain-agnostic loop, outperforms tool sprawl. I design multi-agent frameworks that impose structured cognition on LLMs rather than wrapping them in dozens of specialized skills. The same loop drives documentation generation, code scaffolding, MR persona orchestration, and -- soon -- financial decision-making.

The audience shifted. It is no longer whether humans can understand our context; it is whether agents and LLMs can read and reason over it.

---

## Featured projects

### Valinor -- Local-first mixed-reality AI companion platform

A multi-year independent research platform. Privacy-first, cross-platform AI companion with three fully-featured clients -- iOS / visionOS, Meta Quest 3, and Desktop -- sharing a single persona-driven conversation engine over WebSocket. All inference (LLM, STT, TTS, image generation) runs locally on a Windows host. Zero telemetry, zero cloud dependency. The architecture predates and shares direct lineage with the reasoning frameworks deployed in my current Meta role.

**Everything together -- the Valinor stack running end-to-end:**

https://github.com/user-attachments/assets/ee5ef531-ea6b-4be0-81ee-3e9f9e198447

**Selene persona -- voice-cloned, animated companion rendered on the Quest 3 client:**

https://github.com/user-attachments/assets/b43b3391-d795-4214-ade2-706f11c468a5

**Environment generation -- MRUK scene understanding streamed to the server for contextual mesh generation inside the user's actual room:**

https://github.com/user-attachments/assets/456fba7a-e323-4dd1-a767-29c38c0940e7

Stack: Python, Kotlin, Swift, Rust, TypeScript - llama.cpp + Qwen 3 MoE GGUF - NeuTTS Air - Whisper - SDXL-Turbo - Meta Spatial SDK + MRUK - MLX-Swift - MWDAT.

### Moonlight-SpatialSDK -- Quest 3 port of the Moonlight game-streaming client

Ported the open-source Moonlight game-streaming client to Meta Quest 3 using Meta Spatial SDK. Built as the first proof-of-concept after Valinor validated the Spatial SDK pipeline; still in personal daily use. Low-latency streaming with hardware video acceleration, in-VR pairing, passthrough MR mode, dynamic panel scaling, Bluetooth gamepad passthrough, and automatic stream recovery after sleep/wake cycles.

https://github.com/user-attachments/assets/4d45a8ba-84ff-4283-b45e-64a5e100f86f

Source: [github.com/XXJones21/Moonlight-SpatialSDK](https://github.com/XXJones21/Moonlight-SpatialSDK) -- v1.0.0 December 2025.

Stack: C (Moonlight protocol layer), Kotlin + Jetpack Compose (Quest UI), Java, GLSL - Meta Spatial SDK - Android MediaCodec.

### Dreams.ai -- Interactive AI storytelling platform

Full-stack creative platform combining LLM narrative generation, image diffusion, and video synthesis into a social discovery experience. Custom `.imn` dream file format with feed, infinite-scroll discovery, trending tags, collections, and per-user profiles. Bridges the Technical Artist craft of creative content pipelines into modern generative-model engineering.

Stack: TypeScript, Python - React + Vite - Tailwind - Supabase - LangGraph - llama.cpp - Diffusers - Wan2.2.

### autowrite -- Claude Code plugin for autonomous resume optimization

Built one night over the weekend to help impacted coworkers after the 2026-05-20 Meta layoff. Spawns company-specific recruiter subagents in parallel, researches each target's hiring profile from public sources, scores the resume against 6-12 binary evals per company, and mutates one line at a time until each variant locks at the convergence threshold. Adapts Karpathy's autoresearch loop from skill-prompt optimization to resume content. Same domain-agnostic loop that drives Valinor's agent harness and my Meta work, retargeted at hiring evaluation.

Stack: Markdown-only plugin -- Claude Code skills + subagents -- WebSearch / WebFetch for company research -- live HTML dashboard.

---

## Currently working on

CHOAM -- a simulated hedge fund and multi-agent reasoning platform that operationalizes the same domain-agnostic loop driving my Meta work and Valinor. Currently using F1 Manager 2024 telemetry as a fast-feedback debugging environment for the reasoning loop before moving the same architecture to market decisions. The bet: reasoning quality, distilled into a small fine-tuned model, outperforms tool sprawl in the seconds-to-minutes decision band where most profitable trading actually lives.

The thesis and roadmap is the document I would hand to anyone who wanted to understand where the work is going.

---

## Technical focus

**Agent orchestration and LLM engineering.** Multi-agent reasoning frameworks, agent harnesses (Claude Code, OpenCode, Codex), RAG and knowledge-graph construction, LLM evaluation methodology, prompt and context engineering, LoRA / RLHF concepts, lost-in-the-middle and attention-budget analysis.

**AI/ML infrastructure.** llama.cpp / GGUF, MLX-Swift, Whisper, NeuTTS, Diffusers / SDXL-Turbo, Wan2.2, Ollama, LangChain / LangGraph, local-first GPU inference, fine-tuning workflows.

**Languages.** Python, Rust, TypeScript, Kotlin, Swift, C++, C#, JavaScript, GLSL.

**Spatial computing and XR.** Meta Spatial SDK, MRUK, RealityKit, Reality Composer Pro, visionOS, Unreal Engine 4 and 5, Unity, MWDAT (Meta Ray-Ban).

**Web and full-stack.** React, Vite, Tailwind, Supabase, Three.js / React Three Fiber, Docusaurus, SQL-backed job queues.

---

## Philosophy

Reasoning over tool sprawl. Architecture transfers across domains; policy does not. The loop is the asset.

Decomposing complex systems into actionable instructions is a single craft -- it does not matter whether the audience is a junior engineer reading documentation, a partner team adopting a new framework, or an LLM agent executing a multi-step plan. The discipline holds; the audience moved.

---

## Elsewhere

- Site: [joshjones.tech](https://joshjones.tech)
- Twitter / X: [@MrSwazzy21](https://twitter.com/MrSwazzy21)
- Email: joshuatjones92 at gmail dot com
