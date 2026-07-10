# Skill controls

Skills are reusable workflows made from instructions and supporting resources.
ChatGPT workspace Skills, filesystem skills used by covered local capabilities
in the ChatGPT desktop app, Codex CLI, or IDE extension, and plugins that
package skills have separate lifecycle and access controls.

For the complete administration model, see
[Roles and workspace permissions](https://learn.chatgpt.com/docs/enterprise/roles-and-workspace-permissions).

## Distinguish the distribution models

| Distribution model      | Use it for                                                                                       | Administration boundary                                                                       |
| ----------------------- | ------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------- |
| ChatGPT workspace Skill | Sharing or installing an approved workflow through supported ChatGPT workspace features          | ChatGPT workspace skill permissions and lifecycle controls                                    |
| Local filesystem skill  | Loading an installed workflow from a repository, user, administrator, or bundled system location | Filesystem distribution, local client configuration, and runtime permissions                  |
| Plugin                  | Packaging one or more skills with optional apps, MCP servers, hooks, and presentation metadata   | Plugin availability and installation, plus the separate controls for every bundled capability |

ChatGPT workspace skill distribution, local filesystem skill installation, and
surface-specific plugin installation are separate paths. Moving a skill doesn't
transfer ChatGPT workspace ownership, sharing, role assignments, plugin
installation state, or app authorization.

Plugins are available in ChatGPT Work on the web, in ChatGPT Work and Codex in
the ChatGPT desktop app, and through the Codex CLI plugin browser. They aren't
available in Chat, the IDE extension, or mobile.

## Owning controls

See [Build skills](https://learn.chatgpt.com/docs/build-skills) for filesystem locations and authoring,
[Skills in ChatGPT](https://help.openai.com/en/articles/20001066-skills-in-chatgpt)
for current workspace procedures, and [Build plugins](https://learn.chatgpt.com/docs/build-plugins) for
plugin packaging.

ChatGPT workspace controls don't install local filesystem skills or plugins.
Filesystem distribution doesn't assign ChatGPT workspace ownership or roles.
Plugin installation doesn't grant access to an app, MCP server, or connected
service. Configure each capability through the control surface that owns it.

## Related docs

- [Skills and plugins](https://learn.chatgpt.com/docs/skills-and-plugins)
- [Plugins](https://learn.chatgpt.com/docs/plugins)
- [Build skills](https://learn.chatgpt.com/docs/build-skills)
- [Build plugins](https://learn.chatgpt.com/docs/build-plugins)
- [Admin rollout guide](https://learn.chatgpt.com/docs/enterprise/admin-setup)
- [Plugin controls](https://learn.chatgpt.com/docs/enterprise/apps-and-connectors)