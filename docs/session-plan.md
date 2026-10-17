# Session plan

**Rule of thumb:** everything is deployed before you go live. Click, talk, and breathe. If anything fails, play the backup clip and keep going.

## Before you go live
- [ ] The app is deployed and working (open it once).
- [ ] Tabs are open: the app, this repo, Microsoft Foundry, and Application Insights.
- [ ] Backup clips are ready.
- [ ] The font is large and notifications are off.

## 0:00 · Welcome and the story (8 min)
- Slides: modernization is the foundation for what comes next.
- Show the Todo app we start from: "It works, but only on my laptop."

## 0:08 · Demo 1: It runs on Azure Container Apps (10 min) · [Step 1](https://github.com/roryp/java-modernization-foundry/issues/7)
- **Click:** the app URL, then the `infra` folder and `azure.yaml`, then the container app's identity in the Azure portal.
- **Say:** "One `azd up` created all of this. The app has no passwords; Azure gives it an identity."

## 0:18 · Demo 2: GitHub builds and ships it (10 min) · [Step 2](https://github.com/roryp/java-modernization-foundry/issues/12)
- **Click:** the issues, then a pull request Copilot made, then the green check, then the deploy run.
- **Say:** "I described the work in an issue. Copilot wrote the code, and GitHub tested and deployed it, with no secrets in GitHub."

## 0:28 · Demo 3: Now it's AI (15 min) · [Step 3](https://github.com/roryp/java-modernization-foundry/issues/17)
- **Click:** the `luna` deployment in Microsoft Foundry, then the app's **Ask** box.
- **Type:** "What should I do first?"
- **Show:** the Spring AI code (about 20 lines).
- **Say:** "Luna is the low-cost GPT-6 model. The app calls it with its identity, so there's no API key anywhere."

## 0:43 · Demo 4: Watch it and keep cost down (9 min) · [Step 4](https://github.com/roryp/java-modernization-foundry/issues/21)
- **Click:** Application Insights, then the Ask request, then the model call and its token count, then the budget.
- **Say:** "If you can see the tokens, you can manage the cost: right-size the model, cap the answers, and set a budget."

## 0:52 · Recap and Q&A (8 min)
- Cloud-native → GitHub → AI → observe and optimize.
- What's next: a database, letting Foundry agents use the app's MCP tools, guardrails, and evaluations.

## If something fails
Play the backup clip for that demo and keep talking. Nobody minds.
