# Shira Flow Builder — VS Code extension builds

Packaged builds (`.vsix`) of the **Shira Flow Builder** extension for Visual Studio Code — the canvas
for authoring KeenAgents flows, with Connect → Upload deployment and the flow / script debuggers.

| Build | For |
|---|---|
| `shira-flow-builder-vs-0.0.9.vsix` | Keen 15.3 servers (current): thirteen new Google models in the LLM and Summarizer menus — Gemini 4 Hydrogen, Neon and Argon, Gemini 3.8 / 3.7 / 3.6 / 3.5 Flash, 3.5 Flash Lite, 3.1 Flash Lite, `gemini-pro-latest`, `gemini-flash-lite-latest`, and the open Gemma 4 31B and 26B A4B; each offers only the Thinking Level values its model accepts, Temperature, Top p and Max Tokens up to the model's limit; `gemini-2.0-flash-001` is gone (Google retired it) — choosing "google" now starts on `gemini-2.5-flash`, and a node that still names the old model shows no model selected until you pick another one |
| `shira-flow-builder-vs-0.0.8.vsix` | Keen 15.3 servers: nine new models in the LLM and Summarizer menus — Claude Opus 5.5, Fable 5.1, Fable 5.2, Sonnet 5.5 and Haiku 5.5 (Effort `low` … `max`), GPT-6.2 Astra and Sol (Reasoning Effort `low` … `xhigh`), GPT-6.1 Terra and GPT-6 Luna (`none` … `xhigh`); they show Max Tokens and their effort, no Temperature / Top p (these models refuse them); Claude Opus 4.7 no longer shows Temperature / Top p |
| `shira-flow-builder-vs-0.0.7.vsix` | Keen 15.3 servers: Upload and auto-sync send only `flows/`, `scripts/` and `keen-tools.json` (never a `.env`, `node_modules` or notes) and pause while the project has errors; the Problems panel shows what the platform's deploy would refuse; the debuggers' sign-in says the platform's real reason; the node forms always show and save the current data; an invalid `.flow` opens as an error instead of an empty canvas; the LLM model list matches the platform |
| `shira-flow-builder-vs-0.0.6.vsix` | Keen 15.3 servers: the Summarizer node, two-step sign-in for the debuggers |
| `shira-flow-builder-vs-0.0.4.vsix` | Keen 15.3 servers, accounts without two-step sign-in only |
| `shira-flow-builder-vs-0.0.2.vsix` | servers before Keen 15.3 |

Install a build from the command line:

```bash
code --install-extension shira-flow-builder-vs-0.0.9.vsix
```

or in VS Code: Extensions → `…` menu → **Install from VSIX…**.

The debuggers sign in with your console login: add `"user"` and `"password"` to the project's
`.vscode/keen.json` (keep that file out of git) and switch the debugger on in the console. When your
console account has two-step sign-in, 0.0.6 and later ask the 6-digit code (from your authenticator app or the
e-mail) each time a debugger starts; 0.0.4 cannot sign such an account in.
