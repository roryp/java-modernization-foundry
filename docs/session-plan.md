# Run of show

**Session:** Modernize for what's next: Java on Azure Container Apps → AI with Microsoft Foundry  
**Format:** Microsoft Reactor live stream, 60 minutes including Q&A  
**Golden rules:** pre-provision everything, type only what teaches, and end every act at a checkpoint tag you can jump back to.

Roadmap and status: [session roadmap](https://github.com/roryp/java-modernization-foundry/issues/1). Steps link to their issues.

## Timeline

| Time | Segment | On screen | Steps | Fallback |
|---|---|---|---|---|
| 00:00 | **Intro** | Why modernization is a foundation, not a destination. Run the baseline locally: the web UI, then the MCP tools from Copilot Chat. The README's "not production-ready" warning is the backlog. | — | Screenshots |
| 04:00 | **Act 1 · Cloud-native** | Assessment report, then the issue board. Tour `azure.yaml` and Bicep, run `azd deploy`. Scale to three replicas; todos stay consistent in PostgreSQL. Identity blade: `AcrPull` and an Entra database login. The secrets query comes back empty. | [1.1](https://github.com/roryp/java-modernization-foundry/issues/4), [1.4](https://github.com/roryp/java-modernization-foundry/issues/7), [1.5](https://github.com/roryp/java-modernization-foundry/issues/8) | Tag `act-1-cloud-native`, pre-deployed environment |
| 15:00 | **Act 2 · GitHub-powered delivery** | Assign the live issue to Copilot. CI and the ruleset; the Security tab and push protection. The federated credential, the deploy workflow, and a new revision taking traffic. | [2.4](https://github.com/roryp/java-modernization-foundry/issues/13), [2.5](https://github.com/roryp/java-modernization-foundry/issues/14), [2.1](https://github.com/roryp/java-modernization-foundry/issues/10), [2.2](https://github.com/roryp/java-modernization-foundry/issues/11), [2.3](https://github.com/roryp/java-modernization-foundry/issues/12) | Backup PR, recorded clip |
| 25:00 | **Act 3 · AI with Microsoft Foundry** | The `luna` deployment with keys disabled and Foundry User for the app identity. Live-code the Spring AI assistant; run it locally with `az login`, then on Container Apps with managed identity. The Foundry agent calls the app's MCP tools with the project managed identity. The prompt-injection todo meets guardrails. The evaluation gate. | [3.1](https://github.com/roryp/java-modernization-foundry/issues/15), [3.3](https://github.com/roryp/java-modernization-foundry/issues/17), [3.4](https://github.com/roryp/java-modernization-foundry/issues/18), [3.5](https://github.com/roryp/java-modernization-foundry/issues/19), [3.6](https://github.com/roryp/java-modernization-foundry/issues/20) | Tag `act-3-foundry`, recorded clips |
| 40:00 | **Act 4 · Observe, optimize, and scale** | An end-to-end trace from HTTP through Spring AI, Luna, the tool call, and PostgreSQL. The token and cost workbook, and the budget. Cost-aware patterns before and after. Stretch: an AI gateway 429. | [4.1](https://github.com/roryp/java-modernization-foundry/issues/21), [4.2](https://github.com/roryp/java-modernization-foundry/issues/22), [4.3](https://github.com/roryp/java-modernization-foundry/issues/23), [4.4](https://github.com/roryp/java-modernization-foundry/issues/24) | Saved KQL and screenshots |
| 50:00 | **Close the loop** | Back to Copilot's PR: agent log, Copilot code review, green CI. Merge it, and it deploys to dev. | [2.4](https://github.com/roryp/java-modernization-foundry/issues/13) | Backup PR |
| 53:00 | **Wrap-up and Q&A** | Recap the journey, share resources, and invite everyone to run `azd up` themselves. | [5.3](https://github.com/roryp/java-modernization-foundry/issues/28) | — |

## Talk track

- **Intro:** "Modernization isn't the finish line. It's the foundation for whatever comes next, and today that's AI."
- **Act 1:** "Cloud-native isn't about where it runs. It's stateless, disposable, observable, and it has no secrets."
- **Act 2:** "The identity story continues into the pipeline: no secrets in GitHub either. And Copilot is building part of the backlog while we talk."
- **Act 3:** "Luna is the right-sized default. The identity that reads the database now calls the model, and the MCP server we built for Copilot is now a tool for a Foundry agent."
- **Act 4:** "If you can't see tokens, you can't manage cost. Right-size, trim, cache, and cap."

## Checkpoints

| Tag | State | How to run |
|---|---|---|
| `baseline` | Baseline Todo app (in-memory, local only) | `./mvnw spring-boot:run` |
| `act-1-cloud-native` | Containerized, PostgreSQL, azd and Bicep, managed identity | `azd up` |
| `act-2-github` | CI, supply-chain security, OIDC deployments | `azd up` |
| `act-3-foundry` | Foundry and Luna, assistant, agent over MCP, guardrails, eval gate | `azd up` |
| `act-4-production` | Observability, dashboards, cost-aware patterns | `azd up` |

Only `baseline` exists so far. The other tags are created in [5.1](https://github.com/roryp/java-modernization-foundry/issues/26).

## Environment facts

Fill these in during [3.1](https://github.com/roryp/java-modernization-foundry/issues/15).

| Item | Value |
|---|---|
| Azure region | |
| `gpt-6-luna` quota (TPM) | |
| Foundry project endpoint | |
| App URL | |

## Rehearsal log

Time the Copilot task from [2.5](https://github.com/roryp/java-modernization-foundry/issues/14) on every run.

| Date | Total time | Copilot task time | Notes |
|---|---|---|---|
| | | | |

Pre-flight checklist: [5.2](https://github.com/roryp/java-modernization-foundry/issues/27) · Reset procedure: [5.1](https://github.com/roryp/java-modernization-foundry/issues/26)
