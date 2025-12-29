# Agent Lee — Agentic Operating System (AOS)

Agent Lee is a client-side, local-first Agentic Operating System that runs in the browser.
It focuses on data sovereignty, portable artifacts, and policy-gated connectivity (Zero-Egress by default).

# Agentic Operating System

A compact developer guide for the AgenticOperatingSystem frontend and voice runtime.

## Overview

This repository contains a React + TypeScript frontend that provides a unified voice subsystem (voice profiles, a single voice runtime, and a guaranteed local Web Speech fallback). The workspace exposes a global runtime bridge so non-React code can call `speak` and `stop` reliably.

## Quick start

Install dependencies and start the dev server:

```bash
npm install
npm run dev
```

Open the app in your browser at the address printed by Vite.

## Voice subsystem (summary)

- **Unified configuration:** voice state lives in a single store so `SystemSettings` is authoritative.
- **Local fallback:** Web Speech API is used as a guaranteed local TTS fallback for offline or gated scenarios.
- **Global runtime bridge:** the runtime is exposed to non-React callers so `speak` / `stop` functions are always available.

Files of interest:

- [src/SystemSettings.tsx](src/SystemSettings.tsx#L1) — UI to choose and tune voices.
- [src/voice/voiceStore.ts](src/voice/voiceStore.ts#L1) — unified voice configuration persistence.
- [src/voice/VoiceRuntimeProvider.tsx](src/voice/VoiceRuntimeProvider.tsx#L1) — provides and exposes the runtime.
- [src/voice/voiceAgentControl.ts](src/voice/voiceAgentControl.ts#L1) — speak/stop helpers for non-React callers.

## Manual smoke-checks

1. Start the dev server.
2. In the browser, open the app and grant audio playback permissions if prompted.
3. Open the developer console and verify `window.AGENT_VOICE` (or similar bridge) is present.
4. Use the `System Settings` voice panel to pick a voice and press the test speak button.

## Contributing

1. Create a branch for your change.
2. Run the dev server and verify voice behavior locally.
3. Keep PRs focused and include manual verification steps when touching the voice runtime.

## License

This project follows the repository LICENSE.

---

If you want richer, collapsible documentation or inline SVGs, we should move those assets into a `docs/` directory and keep `README.md` minimal and lint-clean. Tell me which option you prefer and I will either expand `README.md` further (staying markdownlint-clean) or scaffold `docs/` with richer content.
      Local Reasoning (RAG)
            ↓
      New Artifacts Saved

```

</details>
</details>

---

<details>
<summary><strong>Device Compatibility</strong></summary>

<a id="device-compatibility"></a>

| Device           | Supported | Notes                                   |
| ---------------- | --------- | --------------------------------------- |
| Desktop / Laptop | ✅         | Optional GPU acceleration               |
| Tablet           | ✅         | Mobile-optimized models                 |
| Mobile Phone     | ✅         | 0.5B models recommended                 |
| Offline Mode     | ✅         | Fully functional once models are cached |

</details>

---

<details>
<summary><strong>Education & Classroom</strong></summary>

<a id="education--classroom"></a>

### Learning Goals

- Data sovereignty
- Client-side compute
- Evidence-based reasoning (RAG)

### Vocabulary

- **AOS** — Agentic Operating System
- **Artifact** — Durable, auditable record
- **Zero-Egress** — No outbound data by default

</details>

---

<details>
<summary><strong>Developer Manual</strong></summary>

<a id="developer-manual"></a>

### Quick Start

<details>
<summary><strong>Install & Run</strong></summary>

```bash
git clone https://github.com/leeway-innovation/agent-lee.git
npm install
npm run dev
```

Open: `http://localhost:5173`

</details>

### Model Directory Protocol

<details>
<summary><strong>Model Layout</strong></summary>

```text
public/models/
  all-minilm-l6-v2/
    config.json
    onnx/model.onnx
  qwen2.5-0.5b-instruct/
    tokenizer.json
    onnx/model.onnx
```

</details>

### Local Inference Example

<details>
<summary><strong>TypeScript Example</strong></summary>

```ts
import { loadLocalModel } from './leeway-core/LocalModelHub';

const agentBrain = await loadLocalModel('qwen2.5-0.5b-instruct');

const response = await agentBrain.generate({
  prompt: "What were my main tasks from yesterday's LeeMail?",
  useMemoryLake: true
});

console.log(response.text);
```

</details>
</details>

---

<details>
<summary><strong>Security & Survival</strong></summary>

<a id="security--survival"></a>

### Zero-Egress Policy

- Network access is **blocked by default**
- Operator must explicitly enable outbound access

### Portable Shards

<details>
<summary><strong>Export / Import</strong></summary>

```text
• Export encrypted Memory Lake snapshots
• Import on any device
• Restore full system continuity
```

</details>
</details>

---

<details>
<summary><strong>Corporate Identity</strong></summary>

<a id="corporate-identity"></a>

**Leeway Innovation Development**
*A Division of Leeway Industries*

- Architecture: **Leeway v12 Discovery Architecture**
- Core Tech: Vite, React, TypeScript, Tailwind, ONNX Runtime Web
- License: **MIT**

> “The cloud is someone else’s computer. Agent Lee is yours.”

</details>

---

**v8.0 | © 2025 Leeway Industries | Zero-Egress Standard**
**Agent Lee is not a chatbot. He is a local operating partner.**

---

v8.0.0 · © 2025 Leeway Industries

- Persistent local memory
- Evidence-based reasoning
- Policy-controlled connectivity

</details>

---

<a id="core-philosophy"></a>
<details>
<summary><strong>🧠 Core Philosophy — The Leeway Standard</strong></summary>

1. **Zero-Egress by Default** — No data leaves unless explicitly authorized.

2. **Artifact-Based Memory** — Durable, inspectable records—not chat logs.

3. **Hardware Independence** — CPU-first. Acceleration is optional.

</details>

---

<a id="system-architecture"></a>
<details>
<summary><strong>🏗 System Architecture — The Five Organs</strong></summary>

- **Memory Lake** — IndexedDB artifact vault
- **LeeMail** — Email → Tasks → Evidence
- **Reasoning Core (RAG)** — Local retrieval + generation
- **Policy Gate** — Zero-Egress + sensor gating
- **Communications Outlet** — Structured message artifacts

</details>

---

<a id="visual-diagram"></a>
<details>
<summary><strong>🧩 Architecture Diagram (Text)</strong></summary>

```text
Inputs → Artifacts → Memory Lake
            ↓
        Reasoning (RAG)
            ↓
      New Artifacts Saved
```

Internet access exists only if policy allows.

</details>

---

<details>
<summary><strong>⚙ Core Capabilities</strong></summary>

- Local ONNX inference
- Persistent Memory Lake
- Artifact lineage & mistake learning
- Email, communications, file intake
- Policy-gated sensors & network
- Export / Import (Portable Shards)

</details>

---

<details>
<summary><strong>🛠 Developer Manual</strong></summary>

### Quick Start

```bash
npm install
npm run dev
```

Open: `http://localhost:5173`

### Model Staging

```text
public/models/
  qwen2.5-0.5b-instruct/
  all-minilm-l6-v2/
```

Local inference only. No cloud fallback.

</details>

---

<details>
<summary><strong>🛡 Security & Backup</strong></summary>

- Zero-Egress blocks outbound traffic by default
- Mic / camera require explicit permission
- Browser storage can be cleared → **export is survival**
- Portable shards restore full system state

</details>

---

<details>
<summary><strong>📖 Operator Playbook</strong></summary>

- Treat memory as an evidence vault
- Export weekly
- Integrity scan monthly
- Keep Zero-Egress enabled unless intentionally overridden

</details>

---

<details>
<summary><strong>🏫 Teacher / Classroom Version</strong></summary>

**Learning Goals**

- Client-side vs cloud computing
- Data sovereignty
- Evidence-based reasoning (RAG)

**Activity**
Map: Input → Artifact → Retrieval → Decision

</details>

---

<details>
<summary><strong>🏢 Corporate Identity</strong></summary>

**Leeway Innovation Development** — A division of Leeway Industries

Architecture: Leeway v12
License: MIT

</details>

---

<details>
<summary><strong>🌟 The Manifesto</strong></summary>

We do not connect you to the world.
We give you dominion over your own.

**Local by default. Sovereign by design.**

</details>

---

**v8.0.0 · © 2025 Leeway Industries · Zero-Egress Standard**

# AOS-Agentic_Operating_System
<!-- ============================================================================
   LEEWAY HEADER — DO NOT REMOVE
   OWNER: LEEWAY INDUSTRIES
   DIVISION: LEEWAY INNOVATION DEVELOPMENT
   PROFILE: LEEWAY-ORDER
   TAG: CORE.APP.COMPONENT.MAIN
   REGION: 🟢 CORE
   VERSION: 8.0.0
   ============================================================================
   README.md

   DISCOVERY_PIPELINE:
     MODEL=Voice>Intent>Location>Vertical>Ranking>Render;
     ROLE=support;
     INTENT_SCOPE=n/a;
     LOCATION_DEP=none;
     VERTICALS=n/a;
     RENDER_SURFACE=in-app;
     SPEC_REF=LEEWAY.v12.DiscoveryArchitecture

   SPDX-License-Identifier: MIT
   ============================================================================ -->

# Agent Lee — Agentic Operating System (AOS)
>
> **A Product of Leeway Industries** · **Leeway Innovation Development**  
> **Zero-Egress Standard (v12)** · **Local-First / Device-Native**

| Property | Specification |
|:--|:--|
| **Version** | 8.0.0 (Dec 27, 2025) |
| **Runtime** | Browser · Client-Side |
| **Security** | Zero-Egress (Default) |
| **Compute** | CPU-First · Optional Acceleration |
| **License** | MIT |

> **“The cloud is someone else’s computer. Agent Lee is yours.”**

---

## 🎓 Student-Friendly Explainer (Always Visible)

Agent Lee is like a **smart notebook that lives on your device**.  
It remembers notes, emails, tasks, and decisions **without sending them to the internet**.

- Simple device → simple operation  
- Powerful device → faster operation  
- Either way → **you stay in control**

---

## 🔎 Agent Lee vs ChatGPT (Always Visible)

| Topic | Agent Lee | ChatGPT |
|---|---|---|
| Runs where | On your device | Cloud servers |
| Internet | ❌ Not required | ✅ Required |
| Memory | Artifacts (auditable) | Session-based |
| Data ownership | Yours | Platform-owned |
| Offline | ✅ Yes | ❌ No |

---

## 📱 Device Compatibility (Always Visible)

      .muted { font: 500 13px system-ui, -apple-system, Segoe UI, Roboto, Arial; fill: #374151; }
      .pill { fill: #f3f4f6; stroke: #111827; stroke-width: 1.5; rx: 999; ry: 999; }
      .arrow { stroke: #111827; stroke-width: 2.5; fill: none; marker-end: url(#m); }
    </style>
    <marker id="m" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="7" markerHeight="7" orient="auto-start-reverse">
      <path d="M 0 0 L 10 5 L 0 10 z" fill="#111827"/>
    </marker>
  </defs>

  <rect x="20" y="20" width="920" height="480" class="box"/>
  <text x="44" y="56" class="title">Your Device</text>
  <text x="44" y="82" class="muted">Browser Environment (client-side runtime)</text>

  <rect x="70" y="120" width="520" height="320" class="box"/>
  <text x="94" y="156" class="title">Agent Lee (Client-Side OS)</text>
  <text x="94" y="180" class="muted">Runs locally • Stores locally • Policy-gated connectivity</text>

  <rect x="105" y="220" width="210" height="64" class="pill"/>
  <text x="125" y="248" class="text">Inputs</text>
  <text x="125" y="270" class="muted">Email • Chat • Notes • Files</text>

  <rect x="330" y="220" width="210" height="64" class="pill"/>
  <text x="350" y="248" class="text">Reasoning (RAG)</text>
  <text x="350" y="270" class="muted">Retrieves evidence • synthesizes</text>

  <rect x="218" y="320" width="210" height="64" class="pill"/>
  <text x="238" y="348" class="text">Memory Lake</text>
  <text x="238" y="370" class="muted">Artifacts • timestamps • traceability</text>

  <rect x="105" y="400" width="435" height="28" class="pill"/>
  <text x="125" y="420" class="muted">Policy & Settings: Zero-Egress default • sensors gated • operator controls</text>

  <rect x="640" y="140" width="260" height="90" class="box"/>
  <text x="662" y="176" class="title">Internet (Optional)</text>
  <text x="662" y="200" class="muted">Blocked by default</text>
  <text x="662" y="222" class="muted">Enabled only by operator</text>

  <path d="M 590 190 C 620 190 620 190 640 190" stroke="#111827" stroke-width="2.5" fill="none" stroke-dasharray="7 6" marker-end="url(#m)"/>

  <rect x="640" y="260" width="260" height="140" class="box"/>
  <text x="662" y="296" class="title">Compute (Adaptive)</text>
  <text x="662" y="322" class="muted">CPU-first (default)</text>
  <text x="662" y="346" class="muted">Optional acceleration if available</text>
  <text x="662" y="370" class="muted">No forced hardware assumptions</text>
</svg>
```

</details>

---

<details>
<summary><strong>🧠 Core Capabilities</strong></summary>

<br/>

- **Local AI Processing:** ONNX + Transformers.js in a browser runtime.
- **Memory Lake:** IndexedDB-based artifact vault with durable state.
- **RAG Lake:** Evidence retrieval + synthesis; supports mistake learning.
- **LeeMail Intake:** Email → summarize → extract tasks → store as evidence.
- **Communications Outlet:** Phone/messages/video treated as structured inputs.
- **Policy Gate:** Zero-Egress defaults; mic/camera/network permission gates.
- **Export/Import Inventory:** Portable shards + link-file container strategy.
- **Defensive Logging:** Corruption detection, quarantine, incident reports.
- **Lake Bus:** Event-driven “Lake changed” signaling across modules.

</details>

---

## 🛠 Developer’s Manual

<details>
<summary><strong>Open: Quick Start</strong></summary>

<br/>

```bash
npm install
npm run dev
```

Open:

```text
http://localhost:5173
```

</details>

<details>
<summary><strong>Open: Model Directory Protocol</strong></summary>

<br/>

```text
public/models/
  all-minilm-l6-v2/
    config.json
    tokenizer.json
    onnx/
      model.onnx

  qwen2.5-0.5b-instruct/
    config.json
    tokenizer.json
    onnx/
      model.onnx
```

</details>

<details>
<summary><strong>Open: Code Example (Local Inference)</strong></summary>

<br/>

```ts
import { loadLocalModel } from './src/LocalModelHub';

const agentBrain = await loadLocalModel('qwen2.5-0.5b-instruct');

const response = await agentBrain.generate({
  prompt: "What were my main tasks from yesterday's LeeMail?",
  useMemoryLake: true,
});

console.log(response.text);
```

</details>

<details>
<summary><strong>Open: ONNX Runtime + Vite Notes</strong></summary>

<br/>

ONNX Runtime Web relies on `.wasm` and runtime modules that must be served as **real static assets**.
Vite can accidentally transform or inline these binaries if not handled carefully.

Leeway-safe approach:

- Copy ORT wasm/runtime assets into `public/models/onnx/` (or equivalent).
- Set runtime `wasmPaths` to that folder at startup.
- Avoid bundler transformations of ORT binaries.

</details>

---

<details>
<summary><strong>🛡 Security, Backup, & Survival</strong></summary>

<br/>

### Zero-Egress Standard (v12)

- Internet is treated as a **risk zone**.
- External connections are **blocked by default**.
- Operator enables **Network Override** to allow egress.

### Sensor Gating

- Mic/camera are disabled unless explicitly authorized.
- If blocked, the system closes the feature rather than bypassing policy.

### Portable Shards (Export/Import)

Browsers can clear storage. Therefore:

- **Exporting is survival.**
- Shards restore memory on new devices.
- Link-file containers enable scale.

</details>

---

<details>
<summary><strong>📖 Operator Playbook</strong></summary>

<br/>

- Treat the Lake as an evidence vault.
- Quarantine suspect artifacts early.
- Export weekly; integrity scan monthly.
- Keep Zero-Egress enabled unless intentionally doing a trusted workflow.

</details>

---

<details>
<summary><strong>🏫 Teacher / Classroom Resource</strong></summary>

<br/>

### Learning Goals

- Data sovereignty (local-first privacy)
- Client-side compute (WASM, Web Workers, local inference)
- Evidence-based reasoning (artifacts vs guesses)
- Permission gates (mic/camera/network)

### Key Vocabulary

- **AOS**, **Zero-Egress**, **Artifact**, **RAG**

### Activity

Have students map: **Input → Artifact → Retrieve → Answer → New Artifact**.

</details>

---

<details>
<summary><strong>📄 Corporate Identity & Credits</strong></summary>

<br/>

**Leeway Innovation Development**
*A Division of Leeway Industries*

Built with: ONNX Runtime, Transformers.js, Vite, React, TypeScript, Tailwind CSS
License: MIT

</details>

---

<details>
<summary><strong>🌟 The Manifesto</strong></summary>

<br/>

Agent Lee represents a return to computational sovereignty.

**We do not connect you to the world.**
**We give you dominion over your own.**

Local by default. Sovereign by design.

</details>

---

**v8.0.0 | © 2025 Leeway Industries | Zero-Egress Standard**
# AOS-Agentic_Operating_System
