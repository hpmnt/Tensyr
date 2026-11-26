# Tensyr

**Live GPU and LLM server monitoring for Windows.**

Tensyr shows what your GPU servers and the AI models running on them are doing, right now: tokens per second, how long people wait for an answer, how full the GPUs and the KV cache are, how much power it all draws — and an alert the moment something needs attention. It works with **vLLM, SGLang, Hugging Face TGI, llama.cpp, Ollama** and any **OpenAI-compatible** server, with GPU stats from NVIDIA's dcgm-exporter.

**[⬇ Download the latest version](https://github.com/hpmnt/Tensyr/releases/latest)** · [Installing Tensyr](https://github.com/hpmnt/Tensyr/wiki/Installing-Tensyr) · [Getting started](https://github.com/hpmnt/Tensyr/wiki/Getting-Started) · [Connecting servers](https://github.com/hpmnt/Tensyr/wiki/Connecting-Servers) · [Feature sheet](https://github.com/hpmnt/Tensyr/wiki/Feature-Sheet)

---

![Tensyr's machine dashboard: totals, four GPUs and the models running on them](https://github.com/hpmnt/Tensyr/wiki/images/machine.png)

## What Tensyr does

- **Every model server you run, on one screen** — vLLM, SGLang, TGI, llama.cpp, Ollama and OpenAI-compatible servers (LM Studio, LocalAI …). Pick the **server type** or let **Auto-detect** work it out. See [Connecting servers](https://github.com/hpmnt/Tensyr/wiki/Connecting-Servers).
- **Real time** — polls every 250 ms to 5 s (1 s by default) and animates smoothly between readings.
- **Machines and models** — a machine's GPUs show once, with one card per model and charts with one line per model. Several machines get an **Overview** with fleet totals.
- **Throughput that means something** — generation and prompt tok/s with a **time-weighted 5-minute average**, requests per second, and **efficiency** in tokens per joule (and kWh per million tokens).
- **Latency the way users feel it** — time to first token, inter-token latency, end-to-end time and time waiting in the queue (p50/p95).
- **Capacity** — running and waiting requests, KV-cache use, preemptions, prefix-cache hits, average prompt and output length, speculative-decoding acceptance.
- **GPUs in detail** — utilization and **tensor-core activity**, temperature (core and HBM), power against the limit, VRAM, clocks, NVLink and PCIe traffic, and **why** a GPU is throttled.
- **The whole server** — CPU, memory, disks, network and CPU temperature from node_exporter, and inlet / exhaust air, fans, power supplies and server power from the management controller of any make (IPMI or Redfish: Dell iDRAC, HPE iLO, Lenovo XClarity, Supermicro, Cisco …).
- **Alerts** — GPU temperature, throttling, **hardware errors (XID, ECC, row remapping)**, a growing queue, a full KV cache, slow first tokens, and servers that stop answering. They run in the background with Windows notifications. **Red always means an alert, and nothing else.** See [Alerts](https://github.com/hpmnt/Tensyr/wiki/Alerts).
- **Scoreboard** — the record of each stat (latency: the worst) per machine and for the fleet, for today, this week and all time. See [The scoreboard](https://github.com/hpmnt/Tensyr/wiki/Scoreboard).
- **Your layout** — **Customize** shows or hides any tile, section or chart and lets you drag them into your own order; **compact GPU cards** fit eight GPUs on a row. See [Customizing the dashboard](https://github.com/hpmnt/Tensyr/wiki/Customizing-the-Dashboard).
- **Safe with API keys** — optional per model, encrypted with Windows (DPAPI), only ever sent to that model's own URL.
- **Demo mode** — simulated servers (with overloads and alerts) so you can explore before connecting anything.
- **Updates itself** — checks every hour, installs with a 10-second countdown, and shows **what's new** afterwards.
- **Built-in help** — press **F1** anywhere.

## Your data stays with you

Tensyr only **reads** the metrics pages of the servers you add. It has no server of its own, needs no account, and sends nothing anywhere; the only other address it contacts is this GitHub repository, to look for updates. See [Privacy](PRIVACY.md).

## Pages

- [Feature sheet](https://github.com/hpmnt/Tensyr/wiki/Feature-Sheet) — every feature on one page, to print or share
- [Installing Tensyr](https://github.com/hpmnt/Tensyr/wiki/Installing-Tensyr) — requirements, installing, updates, uninstalling
- [Getting started](https://github.com/hpmnt/Tensyr/wiki/Getting-Started) — the first run and the basics
- [Connecting servers](https://github.com/hpmnt/Tensyr/wiki/Connecting-Servers) — dcgm-exporter and every supported model server, step by step
- [The dashboard](https://github.com/hpmnt/Tensyr/wiki/The-Dashboard) — what every number means
- [The scoreboard](https://github.com/hpmnt/Tensyr/wiki/Scoreboard) — the top value of each stat
- [Customizing the dashboard](https://github.com/hpmnt/Tensyr/wiki/Customizing-the-Dashboard)
- [Alerts](https://github.com/hpmnt/Tensyr/wiki/Alerts)
- [FAQ and troubleshooting](https://github.com/hpmnt/Tensyr/wiki/FAQ-and-Troubleshooting)
- [Feedback and Security](https://github.com/hpmnt/Tensyr/wiki/Feedback-and-Security) — bug reports, ideas and reporting vulnerabilities ([security policy](SECURITY.md))
- [Release history](https://github.com/hpmnt/Tensyr/wiki/Release-History) — everything that changed in each version

## The full user guide is built in

Press **F1** anywhere in Tensyr, or click **?** at the top right, to open the user guide.

---

Tensyr is free, closed-source software, provided under its End User License Agreement (shown during installation).

---

© 2026 Tensyr. All rights reserved. · [Wiki](https://github.com/hpmnt/Tensyr/wiki) · [Releases](https://github.com/hpmnt/Tensyr/releases) · [Report a bug](https://github.com/hpmnt/Tensyr/issues) · [Security policy](SECURITY.md)
