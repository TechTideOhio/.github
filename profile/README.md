# TechTide AI

We build agent infrastructure that survives contact with production: cost caps that
actually stop spending, approval gates on anything destructive, and checkpoints you
can resume from when a run dies at 3am.

Based in Ohio. Most of what we ship is Apache-2.0.

## Swarm 357

[**Site**](https://swarm357.techtideai.io) ·
[**Docs**](https://swarm357.techtideai.io/docs) ·
[**Blog**](https://swarm357.techtideai.io/blog) ·
[**PyPI**](https://pypi.org/project/techtide-swarm/) ·
[**Runtime repo**](https://github.com/TechTideOhio/swarm-357) ·
[**Site repo**](https://github.com/TechTideOhio/swarm-357-site)

A Python multi-agent orchestration framework for Claude agents. 357 agent roles across
six business layers — sales, support, marketing, SEO, research, operations — plus ten
management meta-agents that coordinate them.

The catalog is an organizational ontology, not 357 concurrent model sessions. You
compose the roles you need. What the runtime gives you underneath:

| | |
|---|---|
| **Cost control** | Per-layer USD budgets, logged downgrade to a cheaper model at 80 percent of cap |
| **Bash policy gate** | 13-pattern validation, denied by default in server and production |
| **Human approval** | Durable approval records for privileged operations, resolvable out of band |
| **Portable memory** | Flat-file topics plus optional single-file Memvid `.mv2` archives |
| **Durable runs** | Checkpoint, inspect, resume, cancel, replay, and fork any execution |

```bash
pip install techtide-swarm
swarm init && swarm demo
```

Honest maturity reporting is a design goal, not a footnote. Every component is graded
in the [maturity matrix](https://github.com/TechTideOhio/swarm-357/blob/main/STATUS.md),
and evaluation numbers on the site are rendered from committed baselines rather than
written by hand.

## Also public

| Repository | What it is |
|---|---|
| [techtide-harness-kit](https://github.com/TechTideOhio/techtide-harness-kit) | Trust contracts for AI agent skills. JSON Schema risk tiers, tool permissions, deny-by-default egress, prompt-injection fixtures, CI validation gates. |
| [scarlet-fiber-future-web](https://github.com/TechTideOhio/scarlet-fiber-future-web) | Marketing site for Buckeye DataCom, an Ohio fiber-optic network cabling firm. Vite, React, Supabase. |
| [SustainableFW](https://github.com/TechTideOhio/SustainableFW) | 3D sustainable-forests site. Next.js, React Three Fiber, GSAP, Lenis. |

Several smaller repositories package individual harness-kit skills for Lovable.

## Security

Report vulnerabilities privately through the security policy on the relevant
repository rather than opening a public issue. For Swarm 357, start at
[SECURITY.md](https://github.com/TechTideOhio/swarm-357/blob/main/SECURITY.md).

## Contact

Alex Cinovoj — [techtideai.io](https://techtideai.io) ·
[LinkedIn](https://www.linkedin.com/company/techtide-ai/)
