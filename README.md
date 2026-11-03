# Shira Flow Builder — VS Code extension builds

Packaged builds (`.vsix`) of the **Shira Flow Builder** extension for Visual Studio Code — the canvas
for authoring KeenAgents flows, with Connect → Upload deployment and the flow / script debuggers.

| Build | For |
|---|---|
| `shira-flow-builder-vs-0.0.4.vsix` | Keen 15.3 servers (current) |
| `shira-flow-builder-vs-0.0.2.vsix` | servers before Keen 15.3 |

Install a build from the command line:

```bash
code --install-extension shira-flow-builder-vs-0.0.4.vsix
```

or in VS Code: Extensions → `…` menu → **Install from VSIX…**.

The debuggers of 0.0.4 sign in with your console login: add `"user"` and `"password"` to the project's
`.vscode/keen.json` (keep that file out of git) and switch the debugger on in the console.
