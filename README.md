<!--
  XXJones21 GitHub profile README — draft.

  Repo target: github.com/XXJones21/XXJones21 (special "profile repo" — name must match username)

  Video upload workflow before commit:
    1. Open a throwaway issue in any of your repos (e.g. XXJones21/Moonlight-SpatialSDK).
    2. Drag-and-drop each of these files into the comment box one at a time:
         C:\Users\josh2\Downloads\everything.mov                          (7.25 MB)
         C:\Users\josh2\Downloads\Selene_animation_test(2).mp4            (5.78 MB)
         C:\Users\josh2\Downloads\walls-right-side-up.mov                 (5.14 MB)
         C:\Users\josh2\Downloads\SilentHill2Test-spatialSDK-2(2).mp4    (19.85 MB)
    3. Wait for each to finish uploading — GitHub will replace the placeholder text
       with a markdown image/video tag containing a https://github.com/user-attachments/assets/<uuid> URL.
    4. Copy the four user-attachments URLs.
    5. Replace the four <!-- VIDEO: ... --> placeholders below with:
         <video src="<paste URL here>" controls></video>
    6. Discard the throwaway issue (do NOT submit). The uploaded asset URLs persist.
    7. Delete this entire comment block before committing.

  GitHub video embedding rules (current as of 2026-05):
    - Only https://github.com/user-attachments/assets/<uuid> URLs render as inline video.
    - Repo-relative paths and raw.githubusercontent.com URLs do NOT render.
    - Free-tier issue-comment upload limit is 25 MB per file. All four videos are under that.
-->

# Joshua Jones

AI engineer working on the reasoning layer that makes LLMs reliable on long-horizon work. Currently at Meta as an Information Solutions Engineer. Background spans full-stack Rust and Python, the behavioral science of LLM reasoning, and a decade of decomposing complex systems into precise, actionable instructions -- the foundational craft of context engineering for agents.

Santa Clara, CA - [joshjones.tech](https://joshjones.tech) - [@MrSwazzy21](https://twitter.com/MrSwazzy21)

---

## What I'm building

The thread connecting the projects below: reasoning quality, expressed through a domain-agnostic loop, outperforms tool sprawl. I design multi-agent frameworks that impose structured cognition on LLMs rather than wrapping them in dozens of specialized skills. The same loop drives documentation generation, code scaffolding, MR persona orchestration, and -- soon -- financial decision-making.

The audience shifted. It is no longer whether humans can understand our context; it is whether agents and LLMs can read and reason over it.

---

## Featured projects

### Valinor -- Local-first mixed-reality AI companion platform

A multi-year independent research platform. Privacy-first, cross-platform AI companion with three fully-featured clients -- iOS / visionOS, Meta Quest 3, and Desktop -- sharing a single persona-driven conversation engine over WebSocket. All inference (LLM, STT, TTS, image generation) runs locally on a Windows host. Zero telemetry, zero cloud dependency. The architecture predates and shares direct lineage with the reasoning frameworks deployed in my current Meta role.

**Everything together -- the Valinor stack running end-to-end:**

<!-- VIDEO: paste user-attachments URL for everything.mov here -->

**Selene persona -- voice-cloned, animated companion rendered on the Quest 3 client:**

<!-- VIDEO: paste user-attachments URL for Selene_animation_test(2).mp4 here -->

**Environment generation -- MRUK scene understanding streamed to the server for contextual mesh generation inside the user's actual room:**

<!-- VIDEO: paste user-attachments URL for walls-right-side-up.mov here -->

Stack: Python, Kotlin, Swift, Rust, TypeScript - llama.cpp + Qwen 3 MoE GGUF - NeuTTS Air - Whisper - SDXL-Turbo - Meta Spatial SDK + MRUK - MLX-Swift - MWDAT.

### Moonlight-SpatialSDK -- Quest 3 port of the Moonlight game-streaming client

Ported the open-source Moonlight game-streaming client to Meta Quest 3 using Meta Spatial SDK. Built as the first proof-of-concept after Valinor validated the Spatial SDK pipeline; still in personal daily use. Low-latency streaming with hardware video acceleration, in-VR pairing, passthrough MR mode, dynamic panel scaling, Bluetooth gamepad passthrough, and automatic stream recovery after sleep/wake cycles.

<!-- VIDEO: paste user-attachments URL for SilentHill2Test-spatialSDK-2(2).mp4 here -->

Source: [github.com/XXJones21/Moonlight-SpatialSDK](https://github.com/XXJones21/Moonlight-SpatialSDK) -- v1.0.0 December 2025.

Stack: C (Moonlight protocol layer), Kotlin + Jetpack Compose (Quest UI), Java, GLSL - Meta Spatial SDK - Android MediaCodec.

### Dreams.ai -- Interactive AI storytelling platform

Full-stack creative platform combining LLM narrative generation, image diffusion, and video synthesis into a social discovery experience. Custom `.imn` dream file format with feed, infinite-scroll discovery, trending tags, collections, and per-user profiles. Bridges the Technical Artist craft of creative content pipelines into modern generative-model engineering.

Stack: TypeScript, Python - React + Vite - Tailwind - Supabase - LangGraph - llama.cpp - Diffusers - Wan2.2.

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
