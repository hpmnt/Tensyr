# Security Policy

Thank you for helping keep Tensyr and its users safe. If you believe you have found a security vulnerability in Tensyr, please report it privately as described below. **Please do not open a public issue, discussion or pull request for security problems.**

## Supported versions

Tensyr updates itself automatically. Security fixes are made in the **latest release** only, so please check that the problem still exists in the newest version on the [Releases page](../../releases) before reporting.

| Version | Supported |
| --- | --- |
| Latest release | ✅ |
| Older releases | ❌ (update to the latest release) |

## How to report a vulnerability

Open the **Security** tab of this repository and click **[Report a vulnerability](../../security/advisories/new)**. Only the maintainers can see the report.

Please include as much of the following as you can:

- the Tensyr version (bottom left of the Tensyr window) and your Windows version
- what kind of problem it is (for example: leaking a stored API key, sending a key to the wrong host, running code from a crafted server response, a problem with the update process)
- step-by-step instructions to reproduce it, and a sample server response if one is needed
- what an attacker could achieve, and anything you know about how to fix it

Please do **not** include real passwords, API keys, internal host names or other people's personal data in a report.

## What happens next

- We aim to confirm that we received your report within **3 business days**.
- We will investigate, keep you updated on our progress, and may ask you for more details.
- Once a fix is ready, it is published as a new release. Tensyr installs it automatically.
- With your permission, we will thank you by name in the release notes. If you would rather stay anonymous, just say so.

Please give us a reasonable amount of time to fix the problem before you share details publicly. We will agree on a disclosure date with you; normally that is no later than **90 days** after your report.

## Scope

**In scope:** the Tensyr desktop app and its installer and updater as published on this repository's Releases page.

**Out of scope:**

- Problems in the servers Tensyr reads from (vLLM, SGLang, TGI, llama.cpp, Ollama, LM Studio, NVIDIA dcgm-exporter …). Please report those to their makers. If Tensyr itself uses them in an unsafe way, that **is** in scope.
- Attacks that need someone who already controls your Windows account or has administrator access to the PC.
- Social engineering, physical access, denial-of-service and spam.
- Reports from automated scanners without a demonstrated, working problem.

## Safe harbor

We will not take legal action against anyone who acts in good faith under this policy, which means:

- testing only on your own computer and your own servers
- not accessing, changing or deleting other people's data
- reporting the problem privately and giving us time to fix it before going public

Tensyr is free software and does not offer a paid bug bounty.
