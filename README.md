# YuJia Liang

**ML & Systems Engineer · Apple Platforms · Computer Vision & Audio**  
Apple WWDC26 Swift Student Challenge Winner · B.S. Computer Science, NTOU '26 · Taipei, Taiwan

<p>
  <a href="https://yujialiang.com"><img src="https://img.shields.io/badge/Website-yujialiang.com-18181B?style=flat-square" alt="Website"/></a>
  <a href="https://yujialiang.com/YuJia_resume.pdf"><img src="https://img.shields.io/badge/Resume-PDF-18181B?style=flat-square" alt="Resume"/></a>
  <a href="https://www.linkedin.com/in/yujia-liang-77ab022a7/"><img src="https://img.shields.io/badge/LinkedIn-YuJia%20Liang-18181B?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="mailto:ch993115@gmail.com"><img src="https://img.shields.io/badge/Email-Contact-18181B?style=flat-square&logo=gmail&logoColor=white" alt="Email"/></a>
</p>

I build on-device ML systems, audio DSP, computer vision pipelines, and native developer tools—focusing on measurable evaluation, low-latency deployment, and software people can actually use.

---

## Selected Work

### [RiffNode](https://github.com/RiffNode/riffnode-wwdc2026) · *WWDC26 Swift Student Challenge Winner*
Native guitar effects studio for iPadOS and macOS built entirely with Apple frameworks ([case study](https://yujialiang.com/portfolio/riffnode)).
- Low-latency `AVAudioEngine` + custom Audio Unit pipeline running an 11-stage board at **~59× real time** (p99.9 buffer < 0.5 ms of its 2.67 ms budget), plus a Swift/Accelerate port of Neural Amp Modeler matching the reference renderer at **132–135 dB SNR**.
- Tool-calling tone assistant over 13 rig tools backed by on-device **Apple Foundation Models** (with swappable CLI/API providers), clamping every model-proposed value to its `ParameterSpec` bounds before reaching DSP.

`Swift 6` `SwiftUI` `AVFoundation` `Audio Unit` `Accelerate/vDSP` `Foundation Models`

### [Soredemo](https://github.com/soredemo-dev/soredemo) · *Open Source (MIT)*
Mac screen recorder that explains its edits and lets your own coding agent cut takes into launch videos ([soredemo.dev](https://soredemo.dev)).
- Records an accessibility observation log alongside video so cursor motion, zooms, and steps are derived from ground truth—every zoom states its reason and can be overridden.
- Integrates Claude Code and Codex via an Agent tab and read-only **CLI/MCP** server, landing every agent edit as a single named undo step. Zero third-party dependencies.

`Swift 6` `SwiftUI` `ScreenCaptureKit` `AVFoundation` `Metal` `MCP`

### [Volleyball Match Analysis](https://github.com/DL-Volleyball-Analysis/volleyball-analysis) · *NTOU CSE Capstone Silver Award*
Single-camera broadcast volleyball analysis pipeline—started as a senior capstone and rebuilt solo as versioned, cached research stages ([project site](https://dl-volleyball-analysis.github.io/volleyvision-website/)).
- Panning/zooming court registration (**0.10 m** median error), YOLO26s + BoT-SORT tracking (**IDF1 0.690 / HOTA 0.636** on SportsMOT), ball-weighted per-player action classification (**macro F1 0.303 → 0.678** on 16 unseen matches), rally detection (**F1 0.742**), and ballistic 3D ball flights.
- React + FastAPI match review web app with play-by-play filtering, 2D/3D tactics boards, and per-player statistics.

`Python` `PyTorch` `YOLO` `VballNet` `BoT-SORT` `OpenCV` `FastAPI` `React` `Docker`

### [ToneLeak](https://github.com/missing-fundamental/ToneLeak) · *Independent Research*
Counterfactual audit of source leakage in reference-conditioned guitar tone models ([overview](https://yujialiang.com/portfolio/toneleak)).
- Audits 2,040 published Fx embeddings (99.3% tone BA, 87.3% source-decodable) and shows training-time linear projection and DANN adversaries only hide linear views—dropping a linear probe to chance (42.5%) while an MLP probe still reads **94.2%** (DANN: **90.6%**).
- Reports preregistered negative results: per unit of embedding motion, source swaps behave like content swaps (**R ≈ 1.02**), with ~0.55 cents vibrato difference.

`Python` `PyTorch` `scikit-learn` `librosa` `NumPy`

### [oops](https://github.com/itsYoga/oops) · *Published on [crates.io](https://crates.io/crates/oops-sh)*
Copy-on-write CLI safety layer in Rust (`run`, `diff`, `undo`, `commit`) built for autonomous coding agents.
- Provides **O(1) undo** via rootless Linux OverlayFS in a nested user namespace and macOS APFS `clonefile` snapshots, refusing to run unsandboxed on unsupported platforms.

`Rust` `OverlayFS` `Linux Namespaces` `APFS`

---

## Experience & Background

- **Teaching Assistant, Introduction to iOS Application Development** — National Taiwan Ocean University *(Sep. 2026 – Jan. 2027)*
- **AI Image Recognition Research Intern** — ITRI, Electronic & Optoelectronic System Research Labs *(Jul. – Aug. 2025)*  
  Trained multi-task YOLOPX driving perception (**0.972** drivable-area mIoU, **0.793** lane mIoU, **0.838** mAP@0.5), extended the codebase (~1,900 lines), and owned edge deployment to NVIDIA Jetson Nano via pruning, ONNX, and TensorRT/PyCUDA (~15 FPS inference, ZMQ/ROS streaming).
- **Education** — B.S. in Computer Science and Engineering, National Taiwan Ocean University *(2022 – 2026)*; auditing *Deep Learning for Music Analysis and Generation* (Prof. Yi-Hsuan Yang) at National Taiwan University *(Fall 2026)*.

---

## Technical Stack

| Domain | Tools & Frameworks |
|---|---|
| **Languages** | Python, Swift, Rust, C++, TypeScript, Dart, SQL |
| **ML & Audio / Vision** | PyTorch, TensorFlow, OpenCV, ONNX Runtime, TensorRT, YOLO, scikit-learn, NumPy, librosa, ROS, Jetson Nano |
| **Apple Platforms** | Swift 6, SwiftUI, AVFoundation, Audio Unit, Accelerate/vDSP, ScreenCaptureKit, Core Image, Metal, Foundation Models, Vision |
| **Web & Infrastructure** | React, Next.js, FastAPI, Celery, Flutter, MCP, Docker, Redis, PostgreSQL, Firebase, GCP, GitHub Actions, pytest, SwiftPM |

---

<sub>Outside of code: <a href="https://yujialiang.com/photography">photography</a> (darkroom officer at NTUPhoto), volleyball, guitar, and scuba diving.</sub>
