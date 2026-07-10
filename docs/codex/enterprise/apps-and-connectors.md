# Plugin controls

A plugin extends Codex by packaging skills and optional connectors so teams can
distribute workflows and knowledge. Learn more about [plugins](https://learn.chatgpt.com/docs/plugins),
[skills](https://learn.chatgpt.com/docs/skills-and-plugins), and
[apps and connectors](https://help.openai.com/en/articles/11487775).

ChatGPT presents connectors as apps. If a plugin includes a connector-backed
capability, workspace admins must enable the corresponding app and configure
its access before members can use that part of the plugin.

Plugins are available in ChatGPT Work on the web, in ChatGPT Work and Codex in
the ChatGPT desktop app, and through the Codex CLI plugin browser. Availability
on those surfaces doesn't make plugins available in Chat, the IDE extension,
or mobile.

For the complete administration model, see
[Roles and workspace permissions](https://learn.chatgpt.com/docs/enterprise/roles-and-workspace-permissions).

## Understand the capability chain

Each layer has a separate scope and control surface:

| Layer                                 | What it determines                                                     | Where to manage it                                                                                                              |
| ------------------------------------- | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| Plugin availability and installation  | Whether the plugin bundle is available to the user                     | [Workspace settings](https://chatgpt.com/admin/settings) for supported web and desktop surfaces; the CLI plugin browser for CLI |
| Bundled skills                        | Which reusable instructions the installed plugin contributes           | The plugin package and [Skill controls](https://learn.chatgpt.com/docs/enterprise/skills)                                                               |
| Connector access (Apps)               | Whether users can use a connector-backed capability                    | [Workspace apps](https://chatgpt.com/admin/ca) and [Permissions & roles](https://chatgpt.com/admin/settings)                    |
| Connector actions and app permissions | Which actions users can run and when ChatGPT asks before using the app | The app's Action control and App permissions in [Workspace apps](https://chatgpt.com/admin/ca)                                  |
| Source-system authorization           | Which external data and actions the authenticated identity can access  | The connected service and its identity provider                                                                                 |
| Runtime permissions                   | What an agent can do after it receives data or a tool                  | The runtime, sandbox, and approval controls for the active surface                                                              |

Depending on the workflow, admins can govern plugin availability, connector
access, app actions and permissions, provider authorization, and runtime policy
independently.

## Plugin availability controls

Workspace plugin controls determine whether a plugin is available or installed
for supported workspace roles. The Codex CLI plugin browser controls CLI
installation through its own path. See [Build plugins](https://learn.chatgpt.com/docs/build-plugins) for
packaging and distribution.

## Connector-backed capability controls

In ChatGPT, **Apps** is the product label for connected capabilities, including
connectors that search, retrieve, sync, or act on external systems. A plugin can
refer to an app so its workflows can use those connector capabilities.

Manage connector-backed capabilities from
[Workspace apps](https://chatgpt.com/admin/ca) and
[Permissions & roles](https://chatgpt.com/admin/settings). Available controls
let admins:

- Enable reviewed apps and assign access by workspace role.
- For apps that support Action control, allow read-only actions or an approved
  custom set, including how the workspace handles newly added actions.
- Set app permissions that determine when ChatGPT asks before using an app.
- Keep access within the scopes and permissions granted by each connected
  service and authenticated user.

For current availability and procedures, see
[Admin controls, security, and compliance in apps](https://help.openai.com/en/articles/11509118).

## Choose a starting set of apps

For a broad initial rollout, consider app categories teams use every day: email,
calendar, and file or document systems such as Google Drive or Notion. Use the
[ChatGPT app directory](https://chatgpt.com/apps) to confirm current
availability and capabilities.

Start with read actions. Enable write actions only after reviewing the app's
owner, requested scopes, data access, external effects, and recovery path.

## Understand data flow and security

When ChatGPT uses a connector-backed app, the app sends a request to the
connected service and returns data or action results allowed by the
authenticated user's provider permissions. Custom apps expose these operations
as tools through Model Context Protocol (MCP).

For non-synced app use, ChatGPT processes Chat and deep-research data
transiently and doesn't index it. Apps with sync index selected connected
content in advance. This indexing distinction doesn't replace normal
conversation-retention controls; conversations that use apps remain available
through the Compliance API.

OpenAI's current app guidance also documents encryption in transit and at rest,
per-user authorization, role and action controls, restricted network access for
app conversations, and no model training on information accessed from apps for
Business, Enterprise, and Edu customers. Review the connected service's scopes,
retention, and data-residency policies because those policies apply when a
request reaches that service.

See [app security and compliance](https://help.openai.com/en/articles/11509118)
and [apps with sync](https://help.openai.com/en/articles/10847137) for the
current data-handling details. For locally configured MCP servers in the
ChatGPT desktop app, Codex CLI, or IDE extension, see
[Codex MCP configuration](https://learn.chatgpt.com/docs/extend/mcp).

## Use current procedures

- [Admin controls, security, and compliance in apps](https://help.openai.com/en/articles/11509118)
- [Apps in ChatGPT](https://help.openai.com/en/articles/11487775)
- [Apps with sync](https://help.openai.com/en/articles/10847137)
- [Manage workspace settings](https://help.openai.com/en/articles/8411955)
- [Plugins](https://learn.chatgpt.com/docs/plugins)
- [Skills and plugins](https://learn.chatgpt.com/docs/skills-and-plugins)
- [Build plugins](https://learn.chatgpt.com/docs/build-plugins)
- [Admin rollout guide](https://learn.chatgpt.com/docs/enterprise/admin-setup)