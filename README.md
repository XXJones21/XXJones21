# Joshua Jones

I build agent infrastructure and the clients that ship on top of it. Ten years of developer-facing work before that: documentation, SDKs, and sample code at Apple, Snap, Mojang, and Magic Leap.

Santa Clara, CA. [LinkedIn](https://www.linkedin.com/in/joshua-jones-57115382/), [@MrSwazzy21](https://twitter.com/MrSwazzy21)

---

## What I'm building

The thread connecting the projects below: reasoning quality, expressed through a domain-agnostic loop, outperforms tool sprawl. I design multi-agent frameworks that impose structured cognition on LLMs rather than wrapping them in dozens of specialized skills. The same loop drives documentation generation, code scaffolding, and persona orchestration.

The audience shifted. The question is no longer whether humans can read our context. It is whether agents can read and reason over it too, and those two readers do not want the same thing.

---

## Hearth

**Current focus.** A companion that runs entirely on your own machine. Conversations, memory, and your persona's voice stay on your hardware, because there is nowhere else for them to go.

Five clients on one backend. All inference (LLM, speech-to-text, text-to-speech, image generation) runs locally, with zero telemetry. The desktop client bundles the backend and supervises it as a tree of native processes, so installing Hearth installs the whole runtime. No WSL, no container.

A Rust crate, `hearth-probe`, inspects the machine first and decides what Hearth it can run. It ships as its own crate so the app, a command line, and a scripted installer all reach the same conclusions.

```
cargo run -p hearth-probe -- explain
cargo run -p hearth-probe -- explain --simulate m1-air-8gb
```

Source: [github.com/XXJones21/Hearth](https://github.com/XXJones21/Hearth). Pre-alpha, v0.1.0.

Stack: Rust, TypeScript, Kotlin, Swift, Python. Tauri v2 + React (desktop), Jetpack Compose (Android), SwiftUI (iOS and visionOS), llama.cpp + GGUF, Whisper, NeuTTS Air, Diffusers.

### Valinor, the testbed behind it

Hearth's repository starts in August 2026 with a working client and no commits behind it. The work is older. It grew inside a personal research platform called Valinor, which is still where surfaces get tried before they ship, and which carries things that will never ship in Hearth.

**Everything together. The stack running end-to-end:**

https://github.com/user-attachments/assets/ee5ef531-ea6b-4be0-81ee-3e9f9e198447

**Selene persona, voice-cloned and animated, rendered on the Quest 3 client:**

https://github.com/user-attachments/assets/b43b3391-d795-4214-ade2-706f11c468a5

**Environment generation. MRUK scene understanding streamed to the server for contextual mesh generation inside the user's actual room:**

https://github.com/user-attachments/assets/456fba7a-e323-4dd1-a767-29c38c0940e7

**Vision Pro client. A voice-driven persona and a live generative-UI weather card, world-locked in passthrough mixed reality: listening, to thinking, to a spoken answer as a card:**

https://github.com/user-attachments/assets/07f29f12-8ddd-4836-8a44-d916f47c2323

**Ambient panel. The same persona and protocol running always-on on a retail Echo Show 8 reflashed to LineageOS, a thin WebSocket voice client with server-side speech recognition:**

https://github.com/user-attachments/assets/1cc8d831-87d1-4727-bfa5-14871ad24559

---

## Other projects

### Moonlight-SpatialSDK: Quest 3 port of the Moonlight game-streaming client

Rebuilt the GameStream protocol layer's pairing and session handling in C for the Quest 3 variant of Android: certificate-based PIN pairing, Wi-Fi LAN host discovery, and stream recovery across sleep and wake. Underneath it, Bluetooth gamepad passthrough and MediaCodec hardware decode driving a Compose UI. Built as the first proof of concept after Valinor validated the Spatial SDK pipeline. Still in daily use.

https://github.com/user-attachments/assets/4d45a8ba-84ff-4283-b45e-64a5e100f86f

Source: [github.com/XXJones21/Moonlight-SpatialSDK](https://github.com/XXJones21/Moonlight-SpatialSDK). v1.0.0, December 2025.

Stack: C, Kotlin + Jetpack Compose, Java, GLSL. Meta Spatial SDK, Android MediaCodec.

### Dreams.ai: interactive AI storytelling platform

Full-stack platform combining LLM narrative generation, image diffusion, and video synthesis into a social discovery experience. Four specialized agents run in parallel per generation. Custom `.imn` dream format, with an infinite-scroll feed, weekly trending, collections, and per-user profiles.

Source: [github.com/XXJones21/Dreams.ai](https://github.com/XXJones21/Dreams.ai). Deployed on Netlify.

Stack: TypeScript, Python. React + Vite, Tailwind, Supabase, LangGraph, llama.cpp, Diffusers, Wan2.2.

### ComfyUI-Local-MCP: local-first ComfyUI client and MCP server

A device-aware Python library and MCP server that lets Claude Code, Codex, and Hearth generate images and video on a local ComfyUI instance. Reads the host GPU and recommends a workflow its VRAM can actually run. Ships as both an embeddable client and a Claude Code plugin, auto-wiring through `.mcp.json` stdio transport.

Source: [github.com/XXJones21/ComfyUI-Local-MCP](https://github.com/XXJones21/ComfyUI-Local-MCP). MIT licensed.

Stack: Python, FastMCP, ComfyUI runtime. Ships as an MCP server and an agentskills.io-format plugin.

### autowrite: Claude Code plugin for autonomous resume optimization

Built one night over a weekend to help coworkers impacted by the May 2026 Meta layoff. Spawns company-specific recruiter subagents in parallel, researches each target's hiring profile from public sources, scores a resume against 6 to 12 binary evals per company, and mutates one line at a time until each variant locks at the convergence threshold. Adapts Karpathy's autoresearch loop from skill-prompt optimization to resume content.

Source: [github.com/XXJones21/autowrite](https://github.com/XXJones21/autowrite). MIT licensed.

### Feanor: desktop client for local models, with a runtime tool system

Built for the problem MCP was written to solve. Tools are declared in JSON and resolved at runtime, so a new capability needs no client rebuild and no model reload. Direct ancestor of Hearth's gateway and tool registry.

Source: [github.com/XXJones21/Feanor](https://github.com/XXJones21/Feanor). January 2025.

Stack: React + TypeScript over a FastAPI proxy, packaged with Electron and PyQt6.

### Also public

[TheArchive](https://github.com/XXJones21/TheArchive), a visionOS custom immersive environment generator. [Vibes](https://github.com/XXJones21/Vibes), a visionOS music visualization built on RealityKit.

---

## Published work

I wrote the [Contributor Style Guide](https://learn.microsoft.com/en-us/minecraft/creator/documents/styleguide) for the Minecraft Creator Portal, which still governs tone, inclusivity, and naming conventions for every community contribution to the Bedrock docs. I also wrote and built every sample in the introductory visionOS series on developer.apple.com, writing the Swift and the documentation for each.

---

## Technical focus

**Agent orchestration and LLM engineering.** Multi-agent orchestration and state-machine design, agent harnesses at configuration level (Claude Code, OpenCode, Codex): skills, hooks, plugin packaging, context management. MCP server authoring, evaluation-harness design, RAG and knowledge-graph construction, prompt and context engineering, lost-in-the-middle and attention-budget analysis.

**AI/ML infrastructure.** llama.cpp / GGUF, MLX-Swift, Whisper, NeuTTS, Diffusers / SDXL-Turbo, Wan2.2, Ollama, LangGraph, local-first GPU inference, fine-tuning workflows.

**Languages.** TypeScript, Python, Rust, C, Kotlin, Swift, JavaScript, SQL, C++, C#, GLSL.

**Web, desktop, and cloud.** React, Vite, Tailwind, Supabase, Three.js / React Three Fiber. Tauri v2 and Electron packaging, FastAPI, Google Cloud Platform with CI/CD, Docker and Podman on WSL2.

**Developer enablement and XR.** Docs-as-code, Docusaurus, sample-code authoring, developer support and escalation, technical workshops and livestreams. Meta Spatial SDK, MRUK, RealityKit, visionOS, Unreal Engine, Unity, Lens Studio.

---

## Philosophy

Reasoning over tool sprawl. Architecture transfers across domains; policy does not. The loop is the asset.

Decomposing complex systems into actionable instructions is a single craft. It does not matter whether the audience is a junior engineer reading documentation, a partner team adopting a new framework, or an LLM agent executing a multi-step plan. The discipline holds. The audience moved.

---

## Elsewhere

- LinkedIn: [linkedin.com/in/joshua-jones-57115382](https://www.linkedin.com/in/joshua-jones-57115382/)
- Twitter / X: [@MrSwazzy21](https://twitter.com/MrSwazzy21)
- Email: joshuatjones92@gmail.com
