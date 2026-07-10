# Developer commands

Use these commands to control Codex from the VS Code Command Palette. You can also bind them to keyboard shortcuts.

## Assign a key binding

To assign or change a key binding for a Codex command:

1. Open the Command Palette (**Cmd+Shift+P** on macOS or **Ctrl+Shift+P** on Windows/Linux).
2. Run **Preferences: Open Keyboard Shortcuts**.
3. Search for `Codex` or the command ID (for example, `chatgpt.newChat`).
4. Select the pencil icon, then enter the shortcut you want.

## Extension commands

| Command                   | Default key binding                        | Description                                             |
| ------------------------- | ------------------------------------------ | ------------------------------------------------------- |
| `chatgpt.addToThread`     | -                                          | Add selected text range as context for the current task |
| `chatgpt.addFileToThread` | -                                          | Add the entire file as context for the current task     |
| `chatgpt.newChat`         | macOS: `Cmd+N`<br/>Windows/Linux: `Ctrl+N` | Create a new task                                       |
| `chatgpt.newCodexPanel`   | -                                          | Create a new Codex panel                                |
| `chatgpt.openCommandMenu` | -                                          | Open the Codex command menu                             |
| `chatgpt.openSidebar`     | -                                          | Open the Codex sidebar panel                            |

Slash commands let you control Codex without leaving the composer. Use them to check status, switch between local and cloud mode, or send feedback.

## Use a slash command

1. In the Codex composer, type `/`.
2. Select a command from the list, or keep typing to filter (for example, `/status`).
3. Press **Enter**.

## Available slash commands

| Slash command        | Description                                                                             |
| -------------------- | --------------------------------------------------------------------------------------- |
| `/approve`           | Approve one retry of a recent automatic-review denial, when automatic review is active. |
| `/cloud`             | Run the task in the cloud, when cloud execution is available.                           |
| `/cloud-environment` | Choose the cloud environment for the task.                                              |
| `/compact`           | Compact the current task's context.                                                     |
| `/fast`              | Turn a catalog-provided Fast service tier on or off, when available.                    |
| `/feedback`          | Open the feedback dialog to submit feedback and optionally include logs.                |
| `/fork`              | Copy a local task into a new local task.                                                |
| `/goal`              | Set a persistent goal for Codex to work toward.                                         |
| `/ide-context`       | Turn automatic IDE context on or off.                                                   |
| `/init`              | Generate an `AGENTS.md` scaffold for the current project.                               |
| `/local`             | Run the task in your local workspace.                                                   |
| `/mcp`               | Open MCP status to view connected servers.                                              |
| `/memories`          | Configure whether the task can use or generate memories, when Memories is available.    |
| `/model`             | Choose the model for the current task.                                                  |
| `/personality`       | Choose how Codex responds, when the current model supports personalities.               |
| `/plan`              | Toggle plan mode for multi-step planning.                                               |
| `/project`           | Choose a project for new tasks.                                                         |
| `/reasoning`         | Choose the reasoning effort for the current task.                                       |
| `/review`            | Start code review mode to review uncommitted changes or compare against a base branch.  |
| `/side`              | Start a temporary side conversation without interrupting the main task.                 |
| `/status`            | Show the task ID, context usage, and rate limits.                                       |
| `/worktree`          | Run the task in a new Git worktree.                                                     |