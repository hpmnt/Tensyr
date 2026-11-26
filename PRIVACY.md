# Privacy

Tensyr is a monitoring dashboard that runs on your own Windows PC. In short: **it reads from the servers you add, and from nothing else, and it sends your data nowhere.**

## What Tensyr reads

- The **metrics pages** of the model servers you add (for example `http://gpu-server-01:8000/metrics`), or for Ollama and OpenAI-compatible servers, their model list. These pages contain counters such as tokens generated and requests waiting — not prompts, answers or user data.
- The **GPU metrics** page of NVIDIA dcgm-exporter, if you add one.

## What Tensyr keeps

- **Settings** (your machines, URLs, alert thresholds and layout) in `%APPDATA%\Tensyr\settings.json` on your PC.
- **API keys**, if you enter any, encrypted with Windows DPAPI so only your Windows user on that PC can read them. They are never shown again, never written in plain text, and only sent to the model URL they belong to.
- **Recent readings** (the last 5 minutes, for the charts and averages) in memory only. Nothing is stored when Tensyr closes.

## What Tensyr sends

- **Nothing about your servers or your use of Tensyr.** There is no account, no telemetry, no analytics and no crash upload.
- To check for **updates**, Tensyr asks this GitHub repository for the latest version. GitHub sees your IP address, as with any download. See [GitHub's privacy statement](https://docs.github.com/site-policy/privacy-policies/github-general-privacy-statement).
- **Windows notifications** for alerts are shown by Windows on your PC.

## Questions

Ask on the [issue tracker](https://github.com/hpmnt/Tensyr/issues) — or, for anything sensitive, through a [private security report](https://github.com/hpmnt/Tensyr/security/advisories/new).
