---
published: true
title: "75,000 Chips, 140 Trillion Tokens: The Math Behind DeepSeek's Permanent Price Cut"
tags: ai, hardware, china, cloud
---

DeepSeek made its V4-Pro 75% price cut permanent on May 22. The conventional read: "they got cheaper hardware." The real story is more interesting — and it's about a gap that's not closing fast enough.

---

## What Happened

On May 22, 2026, DeepSeek announced that the 75% discount on its V4-Pro API would become permanent. The new pricing:

| Metric | Before | After | Cut |
|--------|-------|-------|:----:|
| Input (cache miss) | ¥12 / 1M tokens | ¥3 / 1M tokens | **75%** |
| Output | ¥24 / 1M tokens | ¥6 / 1M tokens | **75%** |
| Input (cache hit) | ¥0.1 / 1M tokens | ¥0.025 / 1M tokens | **75%** |

At current exchange rates, that's roughly $0.44/M input and $0.87/M output — making V4-Pro one of the cheapest frontier-class models on the market, on par with DeepSeek's own V4-Flash but with significantly more capability.

The move came exactly four weeks after V4's launch on April 24, and coincided with growing user frustration over rate limits at Google Gemini and Anthropic Claude.

---

## The Standard Narrative

The surface-level story has three parts:

**1. Architectural efficiency.** V4 uses a Mixture-of-Experts architecture with 1.6 trillion parameters, but only activates a fraction per token. This gives it a structural cost advantage over dense models of comparable capability — roughly 30% of the gap.

**2. Supply chain scaling.** Huawei's Ascend 950PR entered mass production in April 2026. Huawei plans to ship ~750,000 units through the year — a 2.5x increase over 2025's 910C output. DeepSeek specifically optimized V4 for the Ascend architecture. More chips → lower unit cost → lower API pricing.

**3. Competitive positioning.** Western AI providers (Google, Anthropic) have been quietly tightening rate limits as demand overwhelms their GPU supply. DeepSeek is exploiting the backlash, offering unlimited usage at a fraction of the cost to capture disgruntled developers.

All three are true. But none of them fully explains the magnitude of the cut — or why it's *permanent* rather than promotional.

---

## The Math That Changes Everything

Let's check the numbers.

### Demand Side

China's daily token consumption hit **140 trillion** in March 2026, according to the National Data Administration. The growth trajectory:

- Early 2024: 0.1 trillion/day
- End of 2025: 100 trillion/day
- March 2026: 140 trillion/day

That's a **1,000x increase in two years**, and a **40% jump in just the last quarter** — implying ~13% month-over-month growth.

### Supply Side

Huawei's mass-produced chip for 2026 is the **Ascend 950PR** (Prefill-optimized, 1 PFLOPS FP8), with the higher-end **950DT** (2 PFLOPS FP8) coming in Q4. The numbers:

| Chip | FP8 | Memory | Bandwidth | Inference Throughput (est.) |
|------|:---:|:------:|:---------:|:--------------------------:|
| 950PR | 1 PFLOPS | 128GB HBM | 1.6 TB/s | ~1,200 tokens/sec |
| 950DT | 2 PFLOPS | 144GB HBM | 4 TB/s | ~2,400 tokens/sec |

(Throughput derived from Huawei's published Atlas 950 SuperNode benchmark: 19.6M tokens/sec across 8,192 cards.)

Now the arithmetic:

| Item | Value |
|------|-------|
| Total chips (2026 target) | 750,000 (70% PR + 30% DT) |
| Raw daily throughput | **85.7 trillion tokens/day** |
| Inference-allocated (60%) | **51.4 trillion tokens/day** |
| vs Current demand (140T) | **37% coverage** |
| vs Demand in 6 months (~291T) | **18% coverage** |

Even in the most optimistic scenario — every single chip dedicated to inference at 100% utilization:

| Scenario | vs Current | vs +6 months |
|----------|:---------:|:------------:|
| 100% inference, 100% utilization | **61% coverage** | **29% coverage** |

The conclusion is stark: **750,000 Ascend 950 chips can't cover today's demand — let alone the demand in six months.**

---

## So Why Cut Prices?

If supply is still a fraction of demand, permanent price cuts don't make sense in a normal market. But this is not a normal market.

### The Real Logic: Pre-Commitment, Not Surplus

DeepSeek is not cutting prices because it has spare compute. It's cutting prices to **lock in routing commitments before the hardware arrives**.

Here's the timeline:

```
April 24:  V4 launched, optimized for Ascend
April 24+: ByteDance orders 350,000 Ascend 950 chips (~¥40B)
May 4:     Ascend 950PR mass production confirmed
May 22:    DeepSeek makes V4-Pro 75% cut permanent
```

The critical insight: DeepSeek's price cut is **not a cost pass-through**. It's a **market share pre-commitment** — using the promise of future Ascend supply to grab developer mindshare now, before Western competitors can resolve their own capacity issues.

### The Numbers Behind the Strategy

Western providers are capacity-constrained:

| Provider | Constraint | Signal |
|----------|-----------|--------|
| Google Gemini | TSMC CoWoS capacity | Rate limits tightened, user backlash |
| Anthropic Claude | H100/B200 availability | API throttling, compute-use monitoring |
| OpenAI | Inference cluster rollout | Delayed GPT-5 token limits |

DeepSeek's bet: "Spend the next 6 months building developer dependency on V4-Pro's API — by the time Ascend supply catches up in H2 2026, those developers won't switch back."

**This is AWS in 2006.** AWS wasn't cheaper than running your own servers in 2006. But it *would* be once scale kicked in. AWS priced for the scale it planned to have, not the scale it had. DeepSeek is doing the same.

---

## What 750,000 Chips Actually Buys

The popular framing in Chinese media is "75万颗昇腾950产能大爆发." But as the math shows, 750,000 chips isn't abundance — it's barely adequacy.

**Think of it this way:** China's token demand is growing at roughly 0.5 trillion tokens per day *every single month* (the monthly increment itself is larger than the entire market 18 months ago). By year-end, demand will be 300-400+ trillion. Against that, 750K chips at the 950PR/DT mix buy roughly 50-85T/day of inference capacity.

| Timeframe | Demand (est.) | Inference Supply | Gap |
|:---------:|:------------:|:----------------:|:---:|
| March 2026 | 140T | ~50T | **90T** |
| June 2026 | ~200T | ~50T | **150T** |
| September 2026 | ~290T | ~55T (DT ramp) | **235T** |
| December 2026 | ~420T | ~65T | **355T** |

The gap is *growing*, not shrinking. Even with 75万 chips fully deployed, the supply-demand deficit more than triples over nine months.

This means DeepSeek's price cut isn't a sign of market saturation. It's a sign of exactly the opposite: **a market so unsaturated that the winner gets to define the default API for an entire generation of developers, if they can lock them in before the hardware arrives.**

---

## Three Counter-Arguments (And Why They're Weak)

### "But cache hits reduce the effective compute needed"

True — cache-hit tokens cost ~1/100th of miss tokens. And DeepSeek's cache hit rates can be high for workloads with stable system prompts. But cache hits are mostly in the *input* direction. Output tokens — the expensive ones — still need full compute. And as agentic workloads grow (multi-turn, chain-of-thought), output-to-input ratios increase, making cache less effective.

### "But not all 140T tokens need 950-class inference"

Also true. Many tokens are generated by smaller models (Flash variants, Qwen, etc.) that don't need 950-level compute. But the *growth* is in the frontier-class tokens — longer context, more complex reasoning, higher quality requirements. That's exactly where 950-class chips are needed.

### "But they can still buy H20 / smuggled H100"

H20 is less capable than 950PR per chip (the US-designed it to be worse). And the CHIPS Act + export controls have made H100 procurement increasingly difficult. Relying on smuggled hardware is not a supply chain strategy.

---

## What This Means

### For Developers

Your inference costs are likely going **down** over the next 12 months, not up — even though demand is exploding. That's unprecedented in any computing market. The driver isn't efficiency gains or manufacturing scale. It's a **strategic subsidy** by Chinese AI firms betting that locking in your API calls today is worth negative margins for a year.

Take the subsidy. But don't assume today's prices reflect tomorrow's costs — they reflect tomorrow's *hopes*.

### For the Industry

The AI API market has entered a phase that looks like price war but functions like **infrastructure land-grab**. The playbook is AWS 2006, DoorDash 2019, Uber 2015: lose money on every transaction to own the default routing.

When the hardware *does* catch up — when Ascend 960 (2027) or 970 (2028) ships with 3-5x the throughput — the providers with the largest captive developer bases will convert negative margins to positive ones. Everyone else will be competing on price against incumbents they can't dislodge.

---

## The Bottom Line

> **DeepSeek's permanent price cut is not evidence that Chinese AI compute supply has caught up with demand. The math shows it hasn't — and won't for at least 12-18 months. It's evidence that DeepSeek is playing the long game: use today's negative margins to own tomorrow's default inference route, and trust that Huawei's future chips will eventually close a gap that's currently 3-5x wider than headlines suggest.**

The 75% cut isn't a cost breakthrough. It's a bet that developer lock-in is worth more than current margins — and that the 75万 Ascend 950 chips shipping this year are just the beginning.

---

*Numbers sourced from: National Data Administration (China daily token data, March 2026), Huawei Connect 2025 (Ascend 950 specs and roadmap), SCMP/DW (ByteDance order volume), DeepSeek official pricing page (May 2026). Throughput calculations based on published Atlas 950 SuperNode benchmarks. Growth projections assume continuation of 40%/quarter rate per published data.*
