# Projects, chats, and tasks

Use a project to organize related tasks and give ChatGPT the context it needs.
The **Projects** view in the ChatGPT desktop app includes ChatGPT projects and
local projects that connect to folders on your computer.

## Choose a project or start without one

Create a project when work will continue over time, produce more than one
output, or depend on the same files and sources. Start a task without a project
when the work is self-contained and doesn't need shared project context.









<a id="work-in-a-project"></a>



## Work in a project

The **Projects** view brings ChatGPT projects and local projects into one place.
ChatGPT projects carry project files and context across related tasks. A local
project gives tasks access to one or more folders on your computer, such as a
collection of source files or a codebase.

Start a separate task for each distinct outcome so its messages and results stay
focused while the project keeps related work organized.

<CodexScreenshot
  alt="ChatGPT desktop app showing multiple projects in the sidebar and tasks in the main pane"
  lightSrc="/images/codex/app/multitask-light.webp"
  darkSrc="/images/codex/app/multitask-dark.webp"
  maxHeight="400px"
  class="my-8"
/>









<a id="manage-project-threads"></a>
<a id="organize-projects-and-chats"></a>



## Organize projects and tasks

Keep active work visible and move finished work out of the way:

- **Pin a project** to keep it near the top of the sidebar. You can also pin it
  from the Projects view.
- **Pin a task** when you return to it often, even if newer tasks appear in the
  project.
- **Rename a task** with a short title that describes its outcome, such as “Q3
  launch brief” or “Checkout accessibility review.”
- **Search projects** from the Projects view. Press
  <kbd>Cmd</kbd>/<kbd>Ctrl</kbd>+<kbd>G</kbd> to search past tasks when you
  remember a phrase or branch name but not the title.
- **Archive a task** when you finish the work. From a project's menu, select
  **Archive tasks** to archive its tasks together.

Pinning doesn't add context or change what ChatGPT can access. It only changes
where the project or task appears in the sidebar.

Restore archived tasks from **Settings > Archived tasks**.







<a id="use-local-projects-for-folders-and-codebases"></a>



## Use local projects for folders and codebases

Add a local project when ChatGPT needs to read or change files in a folder on
your computer. For a codebase, the project folder becomes the working directory
for Codex tasks.

If a repository contains more than one app or package, use distinct local
projects when each task should access only one part of the repository. This
keeps the working context focused. Use [local environments](https://learn.chatgpt.com/docs/environments/local-environment)
to define setup actions and common commands for a project.

When you want to isolate code changes from your current checkout, select Codex
and start the task in a [worktree](https://learn.chatgpt.com/docs/environments/git-worktrees). Projects and worktrees organize work,
but the [sandbox](https://learn.chatgpt.com/docs/sandboxing) enforces what local commands can
read, change, or access over the network.



<a id="start-without-a-project"></a>


## Start a task without a project

Select **New task** when the work is self-contained and doesn't need shared
project files, instructions, or folder access. Create a project first when
several tasks will depend on the same context.





<a id="start-a-chat"></a>
<a id="start-a-standalone-chat"></a>


## Use Quick Chat for a quick conversation

Quick Chat opens an ordinary ChatGPT chat, separate from Work and Codex tasks.
Use it for quick questions and ideas that don't need a project or durable task
context.

Select **Chat** in the sidebar. You can also press <kbd>Cmd+Option+N</kbd> on
macOS or <kbd>Ctrl+Alt+N</kbd> on Windows. If a conversation becomes part of
larger work, select **Add to task** to bring it into the current task. Open
**Recent chats** from Quick Chat to return to an earlier conversation.



## Bring in other tools and context



- Attach files or [image inputs](https://learn.chatgpt.com/docs/image-inputs) directly to a task
  when they apply only to that request.
- Install [plugins](https://learn.chatgpt.com/docs/plugins) to bring in context and actions from other
  services.
- Configure [MCP](https://learn.chatgpt.com/docs/extend/mcp) servers when your organization or developer setup
  exposes tools through Model Context Protocol.
- Use [memories](https://learn.chatgpt.com/docs/customization/memories), where available, to carry useful context from
  past work into future tasks.









## Next steps

- [Learn how to write and refine prompts](https://learn.chatgpt.com/docs/prompting)
- [Learn how to use ChatGPT](https://learn.chatgpt.com/docs/use-chatgpt)
- [Continue long-running work](https://learn.chatgpt.com/docs/long-running-work)