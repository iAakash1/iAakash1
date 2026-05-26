<h1 align="center">Hey, I'm Aakash 👋</h1>

<p align="center">
  I build things at the intersection of <b>systems programming</b>, <b>AI/ML</b>, and <b>full-stack web</b> — from raw POSIX sockets to agentic risk engines.<br/>
  3rd-year Computer Engineering @ PCCOE · CHANAKYA Fellow @ IIT Bombay · Open to SDE / ML internships
</p>

<p align="center">
  <a href="mailto:aakashjawle101@gmail.com">
    <img src="https://img.shields.io/static/v1?message=Gmail&logo=gmail&label=&color=D14836&logoColor=white&style=for-the-badge" height="28"/>
  </a>
  &nbsp;
  <a href="https://www.linkedin.com/in/YOUR_LINKEDIN_HANDLE/">
    <img src="https://img.shields.io/static/v1?message=LinkedIn&logo=linkedin&label=&color=0077B5&logoColor=white&style=for-the-badge" height="28"/>
  </a>
  &nbsp;
  <a href="https://leetcode.com/YOUR_LEETCODE/">
    <img src="https://img.shields.io/static/v1?message=LeetCode&logo=leetcode&label=&color=FFA116&logoColor=white&style=for-the-badge" height="28"/>
  </a>
  &nbsp;
  <a href="https://www.codechef.com/users/YOUR_CODECHEF/">
    <img src="https://img.shields.io/static/v1?message=CodeChef&logo=codechef&label=&color=5B4638&logoColor=white&style=for-the-badge" height="28"/>
  </a>
</p>

---

## A bit about me

I'm the kind of person who goes from wiring up a React frontend one week to writing raw POSIX socket code the next — not because I have to, but because I genuinely find both interesting. I like understanding systems from the ground up: how TCP actually works under the hood, why thread-per-client doesn't scale, what a yield curve inversion actually signals for equity risk. That curiosity tends to show up in what I build.

Right now I'm a **CHANAKYA Fellow at IIT Bombay's TIH-IoT**, working on edge-AI models for agricultural use at national scale. Before that I've shipped a systemic-risk prediction engine, a blockchain-based deepfake registry, and a multithreaded TCP server — all from scratch.

---

## 🚀 Featured Projects

### 🧞 miniAladdin — Agentic Risk & Equity Prediction Engine
> *Inspired by BlackRock's Aladdin. Built by a student who wanted to understand why.*

Instead of treating stocks in isolation, miniAladdin pulls macro signals from the **Federal Reserve (FRED API)**, runs **live news sentiment** through a keyword-based scoring engine, and combines them with **technical indicators** (RSI-14, Sharpe/Sortino, drawdown) — all concurrently via an async pipeline.

The centerpiece is the **Systemic Risk Multiplier (SRM)**: a macro-aware dampening factor computed from the yield curve, CPI inflation, and the Fed Funds Rate. When conditions are tight (SRM > 1.3), "Strong Buy" signals get downgraded to "Hold" automatically. It's the kind of logic institutional quant desks actually use.

Ships with a FastAPI backend, Next.js + Tailwind dashboard, Vercel deployment, and Pytest suite at 80%+ coverage.

**Stack:** Python · FastAPI · Next.js 16 · React 19 · Tailwind CSS · FRED API · yfinance · Vercel  
**Code:** [github.com/iAakash1/miniAladdin](https://github.com/iAakash1/miniAladdin)

---

### ⚡ MTCP — Multithreaded TCP Server (C++17 / POSIX)
> *No frameworks. No event loops. Just systems programming.*

Built a production-grade TCP server entirely from scratch using raw POSIX APIs and C++17. The architecture uses a **fixed thread pool** with a **bounded producer-consumer queue** — so idle workers sleep inside `pthread_cond_wait()` at zero CPU cost, and the server applies backpressure when the queue fills instead of running out of memory.

Some things that make this more than a toy: `sendAll()` handles partial writes correctly, `MSG_NOSIGNAL` prevents SIGPIPE from killing the process on dead connections, per-socket `SO_RCVTIMEO` stops slow clients from starving workers, and a `std::atomic<uint64_t>` metrics subsystem tracks everything lock-free. Graceful shutdown with `pthread_cond_broadcast` ensures zero resource leaks — verified under Valgrind and ThreadSanitizer.

**Benchmarks:** 400+ connections/sec · p99 < 10ms on a 4-core machine · stress-tested with 500 concurrent Python clients.

**Stack:** C++17 · POSIX · pthreads · CMake · Python (test harness)  
**Code:** [github.com/iAakash1/MTCP](https://github.com/iAakash1/MTCP) ⭐

---

### 🪙 MirrorMarket — AI Deepfake Authenticity + On-chain Registry
Detects AI-generated media, verifies authenticity via **Chainlink oracles**, and permanently records proofs on-chain via **IPFS**. Built for the Bytecrackers hackathon.

**Stack:** Next.js · Node.js · Chainlink · IPFS  
**Live:** [bytecrackers.vercel.app](https://bytecrackers.vercel.app) · **Code:** [github.com/iAakash1/bytecrackers](https://github.com/iAakash1/bytecrackers)

---

### 🎬 QuickShow — Movie Booking Platform
Full-featured booking app with **real-time seat selection**, Clerk authentication, Stripe payments, and TMDB integration for live movie data. Handles both admin (show management) and user (booking) flows.

**Stack:** React (Vite) · Express · MongoDB · Clerk · Stripe  
**Code:** [YOUR_REPO_LINK]

---

### 🔢 MNIST Digit Generator (from scratch)
Trained a generative model entirely from scratch — no pretrained weights — on a T4 GPU. Wraps into a Streamlit app where you pick a digit 0–9 and it generates one.

**Stack:** Python · PyTorch · Streamlit  
**Demo:** [YOUR_DEMO_LINK] · **Code:** [YOUR_REPO_LINK]

---

### 🌿 Cotton Crop Disease Prediction
NLP-powered recommendation system that classifies plant disease across **8 disease classes** with **93% accuracy** and suggests real-time remedial actions across 3 languages. Includes rigorous data-mining and preprocessing pipeline that cut training time by 25%.

**Stack:** Python · TensorFlow · NLP  
**Code:** [YOUR_REPO_LINK]

---

## 🏛️ Experience

**CHANAKYA Fellow — TIH-IoT, IIT Bombay** *(Dec 2025 – May 2026)*  
Contributed to a ₹500 Crore national-level initiative building edge-AI models for 2M+ farmers. Led model design using lightweight PyTorch/TensorFlow pipelines (MobileNetV2, ResNet) — hit **95%+ accuracy** on-device. Used Generative AI for synthetic data augmentation, boosting dataset diversity by 40%. Reduced edge deployment latency by 30% through large-scale environmental data analysis.

---

## 🧰 Tech Stack

<p>
  <img src="https://skillicons.dev/icons?i=cpp,python,ts,js,react,nextjs,fastapi,nodejs,express,pytorch,tensorflow,mongodb,postgres,redis,docker,aws,git,linux" />
</p>

**Languages:** C++17 · Python · TypeScript · JavaScript · SQL  
**AI/ML:** PyTorch · TensorFlow · scikit-learn · Generative AI · NLP · Data Mining  
**Web:** React · Next.js · FastAPI · Node.js · Express · Tailwind CSS  
**Infra:** Docker · AWS · Azure · Vercel · Git

---

## 📊 GitHub at a glance

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=iAakash1&show_icons=true&theme=dracula&cache_seconds=7200" height="155"/>
  &nbsp;
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=iAakash1&layout=compact&theme=dracula&card_width=320&cache_seconds=7200" height="155"/>
</div>

---

## 🏆 Achievements

- **CHANAKYA Fellow** — Selected for IIT Bombay's national IoT/AI research initiative
- **ML Wars Runner-Up** — Top 2 finish at PCCOE TechFest under competition constraints
- **ACM-W Coordinator** — Ran tech workshops for 300+ students, co-organized Women's Hackathon
- **Open Source Contributor** — Resolved CI linter failures on a public repository
- **CodeChef 3★** · **LeetCode 200+** · **HackerRank 5★**

---

## 📝 Currently exploring

- System Design (working through it level by level)
- DSA — grinding LeetCode consistently
- Building AI × Web products end-to-end

---

## 🐍 Contribution Graph

<img src="https://raw.githubusercontent.com/iAakash1/iAakash1/output/snake.svg" alt="Snake animation"/>

---

<p align="center">
  <i>If something I've built interests you — whether it's the risk engine, the TCP server, or something else — feel free to reach out. Always happy to talk shop.</i>
</p>
