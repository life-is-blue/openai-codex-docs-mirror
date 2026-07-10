# Skills & Plugins

Skills and plugins help ChatGPT complete repeatable work with the right
instructions, resources, and tools. They reduce the need to paste the same
prompt, template, requirements, or process into every conversation.

- A **skill** packages instructions and supporting resources for a specific
  task or workflow.
- A **plugin** is an installable bundle that can include skills, an app, or
  both. Apps are backed by Model Context Protocol (MCP) servers and can
  optionally include custom ChatGPT UI.

## Use skills for repeatable work

A skill is a reusable workflow that gives ChatGPT task-specific guidance. It
can capture the way you already perform recurring work so ChatGPT follows the
same process whenever that task comes up.

A skill can combine:

- A name and description that help ChatGPT recognize when the skill applies.
- Workflow instructions that define the process and expected result.
- Supporting resources such as templates, examples, brand guidance, schemas,
  or connected tools.

Skills are most useful when good results depend on a repeatable approach. For
example, a skill can prepare a daily brief, review documentation, create a
presentation, apply a team writing standard, or gather information from the
same connected tools each week.

Use skills to improve consistency, make team best practices available in the
workflow, and share a standard process instead of relying on undocumented
knowledge.

ChatGPT can choose a skill when your request matches its purpose. You can also
select one explicitly from the composer. ChatGPT supports `@` mentions, while
Codex supports `$` mentions for skills.

## Build skills

You can start by turning a task you already repeat into a simple playbook for
ChatGPT. Good first skills include a weekly update, a campaign brief, a meeting
follow-up, or any task where the steps and format should stay consistent.

To build a useful skill:

1. **Choose one focused task.** Note what you normally start with, such as
   files, links, or notes, and what a finished result should look like.
2. **Describe the workflow to ChatGPT.** Start a new chat with “Build me a
   skill…” and explain the goal, the steps to follow, the expected format, and
   anything it should always include or avoid. Add a template or a good example
   when you have one.
3. **Review and try the draft.** Check the instructions, test the skill with a
   realistic request, and refine it if the result misses a step or drifts from
   the format you want.
4. **Install and reuse it.** Once the skill is enabled, ChatGPT can use it for
   relevant requests, or you can select it explicitly. You can also share it
   with teammates when your workspace settings allow it.

For more details on building skills, see our dedicated guide below.

[<IconItem title="Build skills" className="mt-4">
    <span slot="icon">
      <Tools />
    </span>
    Create, test, and share reusable skills with Codex.
  </IconItem>](https://learn.chatgpt.com/docs/build-skills)

## Use plugins for tools and shared workflows

Plugins make reusable capabilities easier to install and share. A plugin can
combine skills with apps for services such as GitHub, Google Drive, or Slack,
and can include MCP servers for additional tools and context.

Browse the plugin directory when you want to add an existing workflow instead
of building one yourself. After installing a plugin, describe the task directly
or type `@` to choose a specific plugin or bundled skill.

[Learn how to install and use plugins](https://learn.chatgpt.com/docs/plugins).

## Choose between a skill and a plugin

Use a skill when you need reusable instructions for a focused task. Use a
plugin when you want an installable package that can combine instructions with
connected services or other tools.

You can also demonstrate a workflow with
[Record & Replay](https://learn.chatgpt.com/docs/extend/record-and-replay), which turns the recording into a
reusable skill. To package and distribute your own bundle, see
[Build plugins](https://learn.chatgpt.com/docs/build-plugins).

If your plugin needs to connect to a service or expose MCP tools, see
[Build an app](https://learn.chatgpt.com/docs/build-app). When your plugin is ready for public review,
see [Submit plugins](https://learn.chatgpt.com/docs/submit-plugins).

For more examples of reusable workflows, see [Using skills in OpenAI
Academy](https://openai.com/academy/skills/).