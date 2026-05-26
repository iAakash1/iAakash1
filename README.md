<h1 align="center">Aakash Jawle</h1>

<p align="center">
  Final-year Computer Engineering student at PCCOE &nbsp;·&nbsp; CHANAKYA Fellow @ IIT Bombay<br/>
  I like building things that are either very fast or very smart — ideally both.
</p>

<p align="center">
  <a href="mailto:aakashjawle101@gmail.com">
    <img src="https://img.shields.io/static/v1?message=Gmail&logo=gmail&label=&color=D14836&logoColor=white&style=for-the-badge" height="26"/>
  </a>
  &nbsp;
  <a href="https://www.linkedin.com/in/YOUR_LINKEDIN/">
    <img src="https://img.shields.io/static/v1?message=LinkedIn&logo=linkedin&label=&color=0077B5&logoColor=white&style=for-the-badge" height="26"/>
  </a>
  &nbsp;
  <a href="https://leetcode.com/YOUR_LEETCODE/">
    <img src="https://img.shields.io/static/v1?message=LeetCode&logo=leetcode&label=&color=FFA116&logoColor=white&style=for-the-badge" height="26"/>
  </a>
</p>

---

I'm someone who gets genuinely curious about how things work under the hood — which is why one week I'm writing raw POSIX socket code in C++, and the next I'm building a macro-aware risk engine modeled after BlackRock's Aladdin. I don't stay in one lane, and I think that's a feature.

Currently wrapping up a research fellowship at **IIT Bombay**, where I've been building edge-AI models that run on embedded hardware for farmers across India — real constraints, real users, real scale.

---

## Work that I'm proud of

### 🧞 miniAladdin — Systemic Risk & Equity Prediction Engine

Most stock screeners look at a company in isolation. miniAladdin doesn't.

It pulls **macro signals from the Federal Reserve (FRED API)** — yield curve, CPI, Fed Funds Rate — and computes a **Systemic Risk Multiplier** that adjusts every prediction based on the broader economic environment. Yield curve inverted? Inflation running hot? The engine knows, and it dampens bullish signals accordingly. It's the kind of logic quant desks actually use.

On top of that: live news sentiment scoring, RSI-14, Sharpe/Sortino ratios, momentum, and drawdown — all fetched concurrently via an async pipeline. The whole thing ships with a FastAPI backend, a Next.js dashboard, Vercel deployment, and a Pytest suite at 80%+ coverage.

`Python` `FastAPI` `Next.js` `FRED API` `yfinance` `Vercel`
&nbsp;&nbsp;**→** [github.com/iAakash1/miniAladdin](https://github.com/iAakash1/miniAladdin)

---

### ⚡ MTCP — Multithreaded TCP Server (C++17 / POSIX)

No frameworks. No libuv. No abstractions. Just raw POSIX sockets and C++17.

I built this to actually understand what happens below the network stack — and ended up with something that benchmarks at **400+ connections/sec with p99 under 10ms** on a 4-core machine. The architecture uses a fixed thread pool with a bounded producer-consumer queue, so idle workers sleep at zero CPU cost and the server applies backpressure instead of OOM-ing under load.

The details matter here: `sendAll()` handles partial TCP writes correctly, `MSG_NOSIGNAL` stops a dead client from killing the whole process, `SO_RCVTIMEO` prevents slow clients from starving the thread pool. Graceful shutdown via `pthread_cond_broadcast` drains in-flight work before exit. Zero leaks — verified under Valgrind and ThreadSanitizer.

`C++17` `POSIX` `pthreads` `CMake`
&nbsp;&nbsp;**→** [github.com/iAakash1/MTCP](https://github.com/iAakash1/MTCP)

---

### 🪙 MirrorMarket — Deepfake Detection + On-chain Proof Registry

Detects AI-generated media, verifies authenticity through Chainlink oracles, and records tamper-proof proofs on-chain via IPFS. Built for a hackathon, deployed and live.

`Next.js` `Node.js` `Chainlink` `IPFS`
&nbsp;&nbsp;**→** [Live](https://bytecrackers.vercel.app) &nbsp;·&nbsp; [github.com/iAakash1/bytecrackers](https://github.com/iAakash1/bytecrackers)

---

## Experience

**CHANAKYA Fellow — TIH-IoT, IIT Bombay** &nbsp;*(Dec 2025 – May 2026)*

Part of a ₹500 Crore national initiative building edge-AI for agriculture. I led model design for lightweight PyTorch/TensorFlow pipelines (MobileNetV2, ResNet) targeting embedded deployment — hit **95%+ accuracy** on-device, cut latency by 30%. Used generative AI for synthetic data augmentation, which boosted dataset diversity by 40% and meaningfully improved reliability in low-data crop conditions.

---

## Stack

<p>
  <img src="https://skillicons.dev/icons?i=cpp,python,ts,js,react,nextjs,fastapi,nodejs,pytorch,tensorflow,mongodb,docker,aws,git,linux" />
</p>

---

## A few other things

- **ML Wars Runner-Up** at PCCOE TechFest
- **ACM-W Coordinator** — organized workshops for 300+ students
- **CodeChef 3★ &nbsp;·&nbsp; LeetCode 200+ &nbsp;·&nbsp; HackerRank 5★**
- SGPA: 8.4 (last semester)

---

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=iAakash1&show_icons=true&theme=dracula&hide_border=true&cache_seconds=7200" height="150"/>
  &nbsp;&nbsp;
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=iAakash1&layout=compact&theme=dracula&hide_border=true&card_width=300&cache_seconds=7200" height="150"/>
</div>

<br/>

<img src="https://raw.githubusercontent.com/iAakash1/iAakash1/output/snake.svg" alt="contribution graph"/>
