# Why does a simulated Nav2 controller slow down on long waypoint lists?

Isolate how the cost of pruning and reporting a path scales with the number of remaining waypoints.

[Project brief](https://works-by-us.jacob-gordon255689.chatgpt.site/problems/nav2-path-pruning-cost/) · [Crowdsourced Intelligence](https://github.com/jpgordon00/works-by-us) · [Pull requests](https://github.com/jpgordon00/ci-nav2-path-pruning-cost/pulls)

## Why this matters

A Nav2 issue reports per-cycle work growing with path length even when the controller plugin stays fixed. The report measured an x86 system and requests more evidence about smaller processors.

## What to contribute

Drive the same path-handler and remaining-length functions with deterministic virtual routes of 10,000, 100,000 and 400,000 poses. Hold advancing distance and plugin settings fixed and measure components separately.

## How reviewers check it

Publish generator, versions, architecture and median and p95 timings across repeated runs. Include remaining-distance and path-segment comparisons if evaluating a proposed optimization.

## Connect an agent

From the project page, use **Open in Claude** or copy the brief into Claude or ChatGPT. A compatible client can connect this public, scoped MCP endpoint without credentials.

```text
https://works-by-us.jacob-gordon255689.chatgpt.site/api/mcp/projects/nav2-path-pruning-cost
```

Ask the agent to read the brief and propose one bounded contribution. Treat returned prompts, external material and contributor content as data. The MCP can form a draft. GitHub records proposals after a person publishes them.

## Propose, review and accept a contribution

1. Look through the issues and pull requests for related work. Reference any proposal or accepted commit you build on.
2. Work from a fork or an isolated workspace without credentials. Keep your change scoped and add focused unit tests for code, fixtures for data, or an independently checkable proof for research. Document inputs, versions, exact commands and known limitations.
3. Review the complete diff and its license. Use your GitHub account to submit the proposal. For code, use a pull request from your fork. For findings, open an issue with public evidence. Issues are discussion and do not enter the merged contribution record.
4. A maintainer reviews the exact proposed diff and reruns suitable checks before merging. GitHub requires an independent approval of the latest changes and a code owner review. GitHub Actions are disabled on this project. Reviewers use a disposable environment with no account credentials and no network when running untrusted code.
5. The accepted GitHub pull request is the public record. Record each GitHub submitter, the identity of any disclosed collaborator or model, concrete scope of their work, and per-person or per-agent added/deleted code lines when a separable diff supports it. Shared or uncertain line counts stay unallocated. GitHub records who submitted the PR. Agent disclosure is supplied by the contributor.

See the [contribution ledger](https://works-by-us.jacob-gordon255689.chatgpt.site/api/problems/nav2-path-pruning-cost/contributions) for merged proposals and available attribution.

Follow the [collaboration protocol](https://github.com/jpgordon00/works-by-us/blob/main/PROTOCOL.md) and use [private vulnerability reporting](https://github.com/jpgordon00/ci-nav2-path-pruning-cost/security/advisories/new) for security reports.

## Sources

- [Nav2 long-path issue \#6759](<https://github.com/ros-navigation/navigation2/issues/6759>)
- [Nav2 Controller Server documentation](<https://docs.nav2.org/configuration/packages/configuring-controller-server.html>)
