<div align="center">

<img src="https://raw.githubusercontent.com/SwarmCoder/swarmcoder/master/docs/brand/swarmcoder-logo.svg" width="96" alt="SwarmCoder logo">

# SwarmCoder

### Agentic software development that your organization can actually account for

[![swarmcoder.dev](https://img.shields.io/badge/swarmcoder.dev-1f6feb?style=flat-square&logo=firefoxbrowser&logoColor=white)](https://www.swarmcoder.dev)
[![Java 21+](https://img.shields.io/badge/Java-21%2B-e76f00?style=flat-square&logo=openjdk&logoColor=white)](https://openjdk.org/)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue?style=flat-square)](https://www.apache.org/licenses/LICENSE-2.0)

</div>

---

SwarmCoder is a multi-agent coding system that follows one fixed software development lifecycle
every time it runs. It uses expensive frontier models only where a task genuinely needs that level
of judgment, does the bulk of the work with swarms of cheap local models on your own hardware, and
writes down every decision it makes along the way so that you can go back and check it later.

You make two decisions per story, i.e. whether the suggested work is real work that you want done,
and whether the delivery is what you asked for. The system does everything in between.

## What makes it different

| | |
|---|---|
| **Every line of code can be traced back** | For any line you can see which worker wrote it, which candidate it was part of, which test proved it and which requirement asked for it, right back to the sentence in the document it came from. |
| **Your code stays on your network** | The token heavy part of the work, i.e. the loops that read through your whole repository, runs on your own hardware. The cloud based roles only see summaries and diffs, and whatever cloud spend remains is capped per run. |
| **Many cheap attempts instead of one expensive one** | Eight or more local workers attempt each task in parallel, the attempts that fail a real build are thrown away, and one winner is selected on the evidence. |
| **A specification that stays true** | Every requirement is bound to an executable check, so it is only marked as implemented when there is a commit and a passing test behind it. |
| **Built for the day the token subsidy ends** | Over 95% of the token volume runs locally at the cost of electricity, so even a 10× repricing of frontier tokens would not change your bill very much. |

## The project

### 🐝 [swarmcoder](https://github.com/SwarmCoder/swarmcoder)

[![Release](https://img.shields.io/github/v/release/SwarmCoder/swarmcoder?style=flat-square&color=1f6feb)](https://github.com/SwarmCoder/swarmcoder/releases)

The whole system in one repository: the requirement and story model, the fixed lifecycle, the swarm
scheduler and its sandboxes, the verification harness, and the operator console in the browser. It
is written in Java 21, and the console is built on [ZeroZ Stack](https://github.com/ZeroZ4j/zerozstack).

Version 0.1.0 is the first public release and it is an early one. The system is substantially
built, but it is not feature complete and there are known issues that are still open, so please
read the [changelog](https://github.com/SwarmCoder/swarmcoder/blob/master/CHANGELOG.md) before you
plan anything around it.

## Who this is for (and who it is not for)

SwarmCoder is for organizations that need proper traceability on their software development, i.e.
one process that is followed every time and leaves a record behind. It is not an IDE plugin, it is
not a hosted service and it is not fast, since it is built for long unsupervised runs that you
start in the evening and judge in the morning.

If you want an agent that will do anything you ask in any order, there are excellent ones out there
already and you should probably keep using them.

## Where to go next

- **[swarmcoder.dev](https://www.swarmcoder.dev)** has the overview, [how it works](https://www.swarmcoder.dev/how-it-works.html), [the agents](https://www.swarmcoder.dev/agents.html), [the principles](https://www.swarmcoder.dev/principles.html) and the [project status](https://www.swarmcoder.dev/status.html).
- **[The repository](https://github.com/SwarmCoder/swarmcoder)** has the code, the user manual and the build instructions.
- **[Issues](https://github.com/SwarmCoder/swarmcoder/issues)** is the place for bug reports and suggestions.

---

SwarmCoder is built on [ZeroZ4j](https://www.zeroz4j.com) by **Franz Schöning**, Principal
Enterprise Architect. If you are struggling with a complex IT portfolio, a legacy modernization, or
the need to bring AI into your development lifecycle safely, let's talk about your architecture at
[www.franzschoning.com](https://www.franzschoning.com).

Released under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).
