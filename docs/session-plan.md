# Run of show

**Session:** Modernize for what's next: Java on Azure Container Apps → AI with Microsoft Foundry  
**Format:** Microsoft Reactor live stream, 60 minutes including Q&A

## The idea in one line

Build everything before the session. On stage, do four things live and click through the rest.

## Timeline

| Time | Segment | On screen | Mode | Steps |
|---|---|---|---|---|
| 00:00 | **Intro** | Run the baseline locally and call its MCP tools from Copilot Chat. "It's modern, but it only lives on my laptop." | Live | — |
| 05:00 | **Act 1 · Cloud-native** | Dockerfile and safe cloud defaults, then a tour of `azure.yaml` and the Bicep. Run `azd deploy` and open the app on Container Apps. Show the identity's `AcrPull` role; the secrets query returns nothing. | Click through | [1.1](https://github.com/roryp/java-modernization-foundry/issues/5), [1.2](https://github.com/roryp/java-modernization-foundry/issues/7) |
| 15:00 | **Act 2 · GitHub-powered delivery** | **Assign the live issue to Copilot.** Then the CI check, and the deploy workflow signing in with OIDC: no secrets in GitHub. | Live: assign | [2.3](https://github.com/roryp/java-modernization-foundry/issues/14), [2.1](https://github.com/roryp/java-modernization-foundry/issues/10), [2.2](https://github.com/roryp/java-modernization-foundry/issues/12) |
| 25:00 | **Act 3 · AI with Microsoft Foundry** | In Foundry, the `luna` deployment with keys off and Foundry User for the app identity. **Live-code the Spring AI assistant** and ask "What should I tackle first?", locally and then on Container Apps. | Live: code | [3.1](https://github.com/roryp/java-modernization-foundry/issues/15), [3.2](https://github.com/roryp/java-modernization-foundry/issues/17) |
| 40:00 | **Act 4 · Observe and optimize** | One assistant request traced end to end with its token counts. Cost-aware patterns off vs. on, then the budget. | Click through | [4.1](https://github.com/roryp/java-modernization-foundry/issues/21), [4.2](https://github.com/roryp/java-modernization-foundry/issues/23) |
| 50:00 | **Close the loop** | **Merge Copilot's PR** (agent log, code review, green CI), watch it deploy, and refresh to see **Clear completed**. | Live: merge | [2.3](https://github.com/roryp/java-modernization-foundry/issues/14) |
| 53:00 | **Wrap-up and Q&A** | Recap, then "what's next": a database, securing MCP for Foundry agents, guardrails, and evaluations. | — | — |

## If something breaks

| Problem | Recovery |
|---|---|
| Deployment is slow or fails | The pre-deployed environment is already running, so show that. |
| Copilot is slow | Open the backup PR from rehearsal and continue. |
| Live coding goes wrong | `git checkout act-3-foundry` and run it. |
| The network drops | Play the recorded clip for that act. |

## Checkpoints

| Tag | State |
|---|---|
| `baseline` | The starting app (local only) |
| `act-1-cloud-native` | Running on Container Apps with managed identity |
| `act-2-github` | CI and OIDC deployments |
| `act-3-foundry` | Foundry, Luna, and the Spring AI assistant |
| `act-4-production` | Tracing and cost-aware patterns |

Only `baseline` exists so far. The rest are tagged as part of [5.1](https://github.com/roryp/java-modernization-foundry/issues/26).

## Environment facts

| Item | Value |
|---|---|
| Azure region | |
| `gpt-6-luna` quota (TPM) | |
| App URL | |

## Rehearsal log

| Date | Total time | Copilot task time | Notes |
|---|---|---|---|
| | | | |
