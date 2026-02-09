# 🛡️ DefensiveScambaitingAI

A Local, GPU-Accelerated Conversational Agent for Defensive Scambaiting Research

---

## 📌 Overview

DefensiveScambaitingAI is a fully local, cross-platform conversational agent designed to engage telephone scammers in real time for cybersecurity research. The system integrates automatic speech recognition (ASR), large language model (LLM) inference, dialogue policy enforcement, and text-to-speech (TTS) synthesis into a modular C++20 architecture.

The project focuses on safely delaying scam operations, collecting behavioral data, and analyzing social engineering techniques while enforcing strict security and privacy constraints.

This system is developed as part of the *Information Technology Security & Privacy* course at Algoma University.

---

## 🎯 Project Goals

- Develop a real-time conversational agent for scam engagement  
- Maintain low-latency voice interaction  
- Enforce strict safety and policy controls  
- Operate fully offline (local-first design)  
- Support GPU acceleration via Vulkan  
- Enable modular and extensible architecture  
- Support controlled academic experimentation  

---

## 🏗️ System Architecture

The system is organized around a platform-independent core engine implemented as a static library.

```
+------------------------+
|    Application UI      |
|  (GLFW + Dear ImGui)   |
+------------------------+
            |
+------------------------+
|     Engine Core        |
|  - Dialogue Manager    |
|  - Policy Engine       |
|  - LLM Orchestrator    |
|  - Metrics Logger      |
+------------------------+
            |
+------------------------+
|   Platform Wrappers    |
|  - ASR (Whisper)       |
|  - TTS Engine          |
|  - Audio I/O           |
|  - GPU Backend         |
+------------------------+
```

The engine core is platform-agnostic and communicates with external components through narrow adapter interfaces. This design ensures portability and easy replacement of system modules.

---

## 🚀 Key Features

- 🎙️ Real-time speech recognition using Whisper
- 🧠 Local LLM inference using llama.cpp-compatible models
- 🔐 Policy-based safety enforcement
- ⚡ GPU acceleration with Vulkan (optional)
- 📊 Integrated latency and performance logging
- 🖥️ Cross-platform compatibility
- 🧩 Replaceable ASR, TTS, and LLM backends
- 📁 Structured experiment logging

---

## 🛠️ Technology Stack

| Component | Technology |
|-----------|------------|
| Language | C++20 |
| ASR | whisper.cpp |
| LLM | llama.cpp / LlamaLib |
| Audio | RtAudio |
| GPU | Vulkan |
| UI | GLFW + Dear ImGui |
| Logging | Chrome Trace Format |
| Build System | CMake |

---

## 📋 System Requirements

### Hardware

- 64-bit CPU (AVX2 recommended)
- Vulkan-capable GPU (optional)
- Microphone
- Headphones or speakers

### Software

- CMake 3.20+
- C++20 compatible compiler
- Vulkan SDK
- Git
- Python 3 (optional for tooling)

---

## 🔧 Installation Guide

### Step 1: Clone Repository

```bash
git clone https://github.com/your-username/DefensiveScambaitingAI.git
cd DefensiveScambaitingAI
```

### Step 2: Initialize Submodules

```bash
git submodule update --init --recursive
```

### Step 3: Configure Build

```bash
mkdir build
cd build
cmake ..
```

### Step 4: Compile

```bash
cmake --build . --config Release
```

---

## ▶️ Running the System

### Configuration

Edit the configuration file:

```
config/default.json
```

Set paths for:

- ASR model
- LLM model
- TTS engine
- Logging directory

### Launch

```bash
./DefensiveScambaitingAI --config config/default.json
```

### Audio Routing

For testing with calling software, use virtual audio routing tools such as:

- Virtual Audio Cable
- VB-Audio Cable

Configure input/output devices accordingly.

---

## 📊 Performance Evaluation

The system measures and logs:

- Speech recognition accuracy
- End-to-end response latency
- LLM inference time
- Policy trigger frequency
- Engagement duration

Logs are saved in Chrome Trace Format and can be viewed at:

```
chrome://tracing
```

---

## 📁 Project Structure

```
DefensiveScambaitingAI/
│
├── core/           # Engine core
├── asr/            # Speech recognition modules
├── llm/            # LLM runtime wrappers
├── tts/            # Text-to-speech modules
├── audio/          # Audio I/O
├── ui/             # User interface
├── config/         # Configuration files
├── logs/           # Experiment logs
├── tools/          # Utilities
└── docs/           # Documentation
```

---

## 🧪 Testing and Evaluation

Testing is conducted using:

- Synthetic callers
- Controlled human testers
- Pre-recorded scam scripts

All experiments are performed in controlled environments following ethical guidelines.

---

## 🔒 Security and Ethics Policy

This project is intended strictly for academic and defensive research.

### Allowed Use

- Academic research  
- Security experimentation  
- Educational demonstrations  

### Prohibited Use

- Harassment
- Impersonation
- Illegal surveillance
- Fraud
- Unauthorized recording

Users must comply with all applicable privacy and telecommunications laws.

The authors are not responsible for misuse.

---

## ⚠️ Legal Disclaimer

This software is provided for research purposes only.

No warranty is provided. Use at your own risk.

Always obtain proper consent before recording any calls.

---

## 👨‍💻 Development Team

Group 14 — Algoma University

- Martin Jajarmi  
- Sukhraj Singh  
- Yahya Fazal  

Instructor: Dr. Yazan Otoum

---

## 📄 License

This project is licensed under the MIT License.

See the `LICENSE` file for details.

---

## 🤝 Contributing

Contributions are welcome for academic purposes.

1. Fork the repository
2. Create a feature branch
3. Commit changes
4. Submit a pull request

All contributions must follow ethical guidelines.

---

## 📬 Support and Contact

For questions, bug reports, or academic inquiries, please open a GitHub issue.

---

## 📈 Future Work

Planned improvements include:

- Native VoIP integration
- Advanced behavioral analytics
- Multi-language support
- Federated learning extensions
- Enhanced GPU pipelines
- Automated experiment orchestration

---

## ⭐ Acknowledgments

- Algoma University  
- Open-source contributors to Whisper and llama.cpp  
- Khronos Group (Vulkan)  
- Course instructors and reviewers

---
