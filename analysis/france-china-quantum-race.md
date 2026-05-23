# €500 Million, 5 Qubits, 1 Winner: Why France Is Betting on Quantum — and What China Is Doing About It

**A deep dive into the PROQCIMA program, the five French quantum startups, China's parallel tracks, and what computer history tells us about who wins.**

---

## The Setup

In April 2026, France launched **PROQCIMA** — a €500 million, 10-year program managed by the Ministry of Defense (DGA) to build a fault-tolerant quantum computer. Five startups, five qubit architectures, a Darwinian elimination: five companies survive to year four, two to year eight, one wins at the end.

The goal: a 128-logical-qubit demonstrator by 2030, a 2,048-logical-qubit commercial machine by 2035.

The framing from French CEO Théau Peronnin (Alice & Bob) is blunt: "We have what it takes to win it. It's about believing in ourselves."

But France isn't the only player. China has been running a parallel effort at 10x the scale — and recently published results that make everyone pay attention.

This post analyzes both programs, their architectural choices, and what computer history suggests about who wins.

---

## Part I: The French Five

France's strategy is unique: instead of picking one qubit technology (as the US effectively did with superconducting), PROQCIMA funds **five architectures simultaneously**, letting the market of physics decide.

### 1. Pasqal — Neutral Atoms (The Breakthrough)

**Headline (May 21, 2026):** Pasqal demonstrated that **logical qubits outperform physical qubits** on real computational tasks — a world first.

- Solved differential equations using a quantum kernel algorithm
- Logical qubits beat physical qubits by 50% on average, **10x on specific nonlinear problems**
- Gate fidelity: 99.4%
- Used a [4,2,2] quantum error-detecting code (4 physical qubits → 2 logical qubits)
- Going public in 2026 at ~$2B valuation — Europe's first quantum IPO

**Why it matters:** This is the first experimental proof that error correction isn't just theoretical overhead — it produces **better results** than raw physical qubits, even on imperfect hardware.

**Roadblock:** Neutral atom gates are microseconds (vs nanoseconds for superconducting). This limits how fast you can run algorithms, even if the qubits are reliable.

### 2. Alice & Bob — Cat Qubits (The Architecture Bet)

Cat qubits encode information in superposed coherent states |α⟩ and |-α⟩, named after Schrödinger's cat. The genius: **bit-flip errors are exponentially suppressed at the hardware level**.

- This means their error correction only needs to handle phase-flip errors
- Result: a repetition code (5 cat qubits → 1 logical qubit) vs surface code (49 superconducting qubits → 1 logical qubit)
- Series B of €100M (Jan 2025), total €130M
- Building a $50M lab north of Paris with in-house chip fab

**Why it matters:** If cat qubits scale, they could achieve fault-tolerance with **5-10x fewer physical qubits** than superconducting approaches. The catch: manufacturing consistent cat qubit cavities is unproven at scale.

**Validation signal:** Google acquired Atlantic Quantum in 2025 — a cat-qubit-adjacent company. The same architectural bet, by the richest player.

### 3. Quobly — Silicon Spin Qubits (The Manufacturing Edge)

**Headline (Dec 2025):** Quobly ran the first silicon-28 FD-SOI quantum wafers through STMicroelectronics' 300mm fab in Crolles, France.

- Single-qubit gate fidelity approaching **99.999%**
- Uses standard 28nm FD-SOI CMOS process — the same lines that make conventional chips
- Roadmap: **million-qubit** scale
- Raised €19M (2023, European seed record) + €21M (2025)

**Why it matters:** While everyone else builds factories from scratch, Quobly walks into ST's existing fab. If silicon spin qubits work, the manufacturing supply chain already exists. This is the semiconductor industry's ultimate moat.

### 4. Quandela — Photonic Qubits (The First Deployment)

Delivered **Lucy**, a 12-qubit universal photonic quantum computer, to CEA's TGCC — the first photonic quantum computer deployed in a European computing center.

- 80% of components sourced in Europe
- Integrated with the Joliot-Curie supercomputer for hybrid HPC-quantum workflows
- Will connect to the Alice Recoque exascale supercomputer in 2026

### 5. C12 Quantum Electronics — Carbon Nanotubes

The most experimental of the five. Nanotube-based qubits. Earliest stage, most likely to be eliminated in the first Darwinian round.

### The French Comparison Table

| Company | Qubit Type | Key Metric | Advantage | Scaling Challenge |
|---------|-----------|-----------|-----------|------------------|
| Pasqal | Neutral Atom | Logical > Physical ✅ | Low connectivity cost | Gate speed (μs) |
| Alice & Bob | Cat Qubit | Noise-biased, 5:1 logical | Hardware-level error suppression | Cavity manufacturing |
| Quobly | Silicon Spin | 99.999% fidelity | Uses STMicro fab | Spin coherence |
| Quandela | Photonic | 12 qubits deployed | HPC integration | Photon loss |
| C12 | Carbon Nanotube | Early stage | — | — |

---

## Part II: China's Two Tracks

While France spreads bets across five architectures, China concentrates on **two deep tracks**, both led by the same team at USTC (Pan Jianwei's group).

### Track 1: Zuchongzhi-3 — Superconducting (March 2025)

- **105 qubits**, 182 couplers
- Single-qubit gate: 99.90%, two-qubit: 99.62%, readout: 99.13%
- 83-qubit random circuit sampling: **10^15x faster than Frontier supercomputer**
- **1 million times faster than Google's Sycamore**
- Running surface code distance-7, pushing to distance-9/11

**December 2025 milestone:** First below-threshold quantum error correction **outside the US**, using a novel all-microwave leakage suppression architecture. Same distance-7 surface code as Google Willow.

### Track 2: Jiuzhang 4.0 — Photonic (May 2026, Nature)

- **3,050 photons** manipulated and detected (up from 255 in Jiuzhang 3.0 — a 12x jump)
- 1,024 squeezed-state light sources → 8,176-mode interferometer
- 92% source efficiency, 51% overall system efficiency
- Gaussian Boson Sampling: **25 microseconds** vs El Capitan's **10^42 years**

**The nuance:** Jiuzhang solves a specialized problem (boson sampling), not general quantum computation. But it demonstrates China's ability to scale photonic systems at a rate no other country matches.

### China's Quantum Investment

| Metric | Estimate |
|--------|---------|
| 15th Five-Year Plan (quantum) | ~$16B (estimated, 2026-2030) |
| Q1 2026 private financing | ¥2.2B ($322M) |
| Total quantum companies | ~153 (2/3 in Hefei) |
| Listed quantum companies | QuantumCTek (2020 IPO), CIQTEK (IPO filed), Origin Quantum ($1B valuation, IPO prep) |
| Primary hub | Hefei National Quantum Laboratory |

---

## Part III: The French vs Chinese Strategy — Side by Side

| Dimension | 🇫🇷 France | 🇨🇳 China |
|-----------|-----------|----------|
| **Architectures** | 5 parallel (Darwinian) | 2 deep (superconducting + photonic) |
| **Primary executor** | 5 startups + academia | USTC (Pan Jianwei team) for both tracks |
| **Public funding** | €500M (PROQCIMA) + €1.8B (total quantum plan) | ~$16B estimated (15th FYP) |
| **Private funding** | Minimal (Pasqal IPO pending) | Active IPO pipeline, ¥11.2B cumulative |
| **Error correction** | Just proved logical > physical (May 2026) | Below-threshold surface code (Dec 2025) |
| **Commercial** | First HPC deployments (customer trials) | QuantumCTek listed since 2020 |
| **Cat qubit effort** | Alice & Bob (200-person company) | Academic theory only (USTC/Tsinghua) |
| **Manufacturing** | Building fabs (Alice & Bob) or using ST (Quobly) | State-built Hefei National Lab |

---

## Part IV: Does Anyone in China Research Cat Qubits?

Yes — but almost entirely at the academic level.

**USTC (Guo Guangcan / Zou Changling group)** published in February 2026 a theoretical framework for fault-tolerant preparation of arbitrary logical states in the **four-legged cat code**, achieving 99.99% fidelity in numerical simulation on a 3D superconducting cavity platform.

**Tsinghua University (Sun Luyan)** experimentally works on bosonic encoding and cat codes in superconducting cavities.

**But:** there is no Chinese equivalent of Alice & Bob — a dedicated, company-scale effort with 200 employees, dedicated fab, and €130M in funding. Cat qubits in China remain a university research topic, not a national hardware track. The strategic reasoning: when your transmon already has 105 qubits at 99.90% fidelity, you don't bet the farm on an unproven architecture.

**This is the biggest wildcard:** If Pan Jianwei decides to open a cat qubit hardware line at Hefei National Lab, China's manufacturing + capital could close the gap in 2-3 years. The theoretical foundation is already there.

---

## Part V: The Architecture Question That Nobody's Asking Correctly

The central question of this race is not "which country invests more" — it's **which physical qubit architecture gives you the best error correction efficiency**.

The key insight is **noise bias**:

| Qubit Type | Error Profile | Error Correction | Physical Qubits per Logical |
|-----------|--------------|-----------------|---------------------------|
| Transmon (Zuchongzhi, Google) | Symmetric (bit-flip + phase-flip) | Surface code | ~50-100 |
| Cat Qubit (Alice & Bob) | **Noise-biased** (bit-flip suppressed) | Repetition code (phase-flip only) | ~5-20 |
| Neutral Atom (Pasqal) | Low connectivity, flexible | [4,2,2] code, scaling to surface | ~10-50 |

**Transmon = CISC.** Complex, powerful per-qubit, but heavy error correction overhead.

**Cat qubit = ARM.** Weaker per qubit, but the architecture is clean, and the error correction overhead is 5-10x lower.

**Neutral atom = FPGA.** Flexible connectivity, but slower gate speeds limit throughput.

---

## Part VI: Historical Analogies — And What They Suggest

### Transistor vs Vacuum Tube (1947-1960s)

Vacuum tubes had better specs. Transistors had better fundamentals. The transistor won because it was **scalable** — the vacuum tube hit physical limits.

**Analog:** If cat qubits or neutral atoms turn out to be the "transistor" of quantum computing — a fundamentally more scalable approach — they could win despite early performance deficits.

But: the transistor analogy is imperfect because **no one has proved any qubit type is the "transistor" yet**.

### RISC vs CISC (1980s-2000s)

CISC (x86) dominated benchmarks for a decade. RISC (ARM) was considered an academic toy. Today ARM dominates mobile and is eating the world.

**Analog:** The noise-biased, lower-overhead architecture (cat qubit) could be the "RISC" that wins in the long run — but only if manufacturing scales.

### Beowulf Clusters vs Cray Supercomputers (1990s)

Cray built the most elegant, fastest single machines. Beowulf built ugly clusters from commodity parts. The cluster won because **linear scalability beats peak performance**.

**Analog:** The architecture that connects qubits most efficiently (cat qubit fiber links? neutral atom laser arrays?) could win, even if its single-qubit performance is worse.

### The Counter-Analogy: Google's Quantum Supremacy Was Reversed

In 2023, USTC researchers used **1,400 A100 GPUs + better algorithms** to reproduce Google's "quantum supremacy" result — turning Google's claim of "10,000 years" into **14 seconds**.

**Warning:** Jiuzhang 4.0's "10^42 years" statistic against El Capitan may suffer the same fate as classical algorithms improve.

---

## Part VII: Three-Window Prediction

### Window 1 (2026-2028): First Useful Demonstration

**Winner: Superconducting (China + Google).** Not because the architecture is better, but because they have 10x the resources and the most mature hardware. The first demonstration that a quantum computer does something a classical computer genuinely cannot (not just a benchmark) will come from a transmon system.

Probability: Superconducting 60% / Neutral Atom 25% / Cat Qubit 15%

### Window 2 (2028-2032): The Scaling Inflection

The critical question: **When transmon surface code reaches distance-11 or distance-13, does the wiring overhead become prohibitive?**

- If yes: cat qubits or neutral atoms benefit from lower connectivity costs
- If no: transmon continues to dominate

This window is the **real race**. The outcome depends on engineering execution, not architectural elegance.

Probability: Superconducting leads 50% / Cat Qubit catches up 30% / Other 20%

### Window 3 (2032+): The Manufacturing Winner

The ultimate winner is **the architecture whose manufacturing chain scales to thousands of logical qubits first.**

- Cat qubits have an elegant theoretical path (fiber-coupled cavities, minimal wiring)
- Silicon spin has the ultimate manufacturing moat (existing semiconductor fabs)
- Neutral atoms have the most flexible connectivity

**My bet:** The architecture that proves "can I make 1,000 identical high-quality qubits on a repeatable process" wins — regardless of its per-qubit gate fidelity.

### The Biggest Wildcard

**China has the theoretical capability to start a cat qubit hardware program within 2 years.** The research is already being published (USTC cat code paper, Feb 2026). If the government decides to add cat qubits as a third national track alongside Zuchongzhi and Jiuzhang, the funding and scale available could produce a credible competitor to Alice & Bob faster than anyone expects.

---

## Conclusion

France's €500M bet is not just about quantum computing. It's about a fundamental geopolitical conviction: **Europe can still win a technology race.** Quantum is early enough, unsettled enough, that a country of 68 million people with world-class physics research can compete.

China's response is not "we pick different architectures" — it's "we'll build everything, at 10x scale, and let the physics sort itself out." While France funds five startups with €500M, China funds 153 companies, builds the world's largest quantum laboratory, and already has two world-record systems.

But the history of computing suggests something uncomfortable for both:

> **The architecture that wins is almost never the one that looks best in benchmarks. It's the one whose manufacturing scales.**

On that measure, Quobly (silicon spin at STMicro) and Alice & Bob (cat qubits with fiber coupling) have the most elegant stories. Zuchongzhi has the best numbers. Pasqal has the most beautiful physics.

**No one knows who wins. That's exactly why it's worth watching.**

---

*Published: May 2026*
*Written from publicly available sources: Nature (Jiuzhang 4.0, May 13 2026; Zuchongzhi-3, Mar 2025; Alice & Bob cat qubits, Feb 2025), Pasqal press release (May 21, 2026), The Next Web, Tom's Hardware, The Quantum Insider, SCMP, CSIS, Chinese Academy of Sciences press releases.*
