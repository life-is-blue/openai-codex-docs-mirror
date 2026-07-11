# Build an app

Apps are one part of the plugin model. A plugin is the package users discover,
install, submit, and publish. An app is the MCP-backed capability inside that
package.

The [Apps SDK](https://developers.openai.com/apps-sdk) is the ChatGPT app development framework for
MCP-backed apps. It builds on MCP: your server exposes tools and returns
structured data, and, when you need UI, Apps SDK conventions let you register
MCP UI resources and connect them to those tools inside ChatGPT.

Build an app when your plugin needs to connect to a service, expose tools,
authenticate users, or take action through an MCP server.

## App building model

An app can include:

- **An MCP server:** the server defines tools, handles authentication, returns
  structured data, and enforces the integration's real behavior. See
  [Build your MCP server](https://developers.openai.com/apps-sdk/build/mcp-server).
- **Tool metadata and annotations:** required for reliable model behavior,
  discovery, and review. Tool names, descriptions, schemas, `readOnlyHint`,
  `openWorldHint`, and `destructiveHint` should match what the tool actually
  does. See the [Apps SDK reference](https://developers.openai.com/apps-sdk/reference#tool-descriptor-parameters)
  for the descriptor fields and annotation details.
- **Optional MCP UI:** useful when users need to inspect, compare, edit,
  confirm, or navigate structured information inside ChatGPT. If your app can
  complete its job through tool calls and model responses, you do not need
  custom UI. Build this with [Apps SDK](https://developers.openai.com/apps-sdk) UI resources when tool calls
  and model responses are not enough.

## Build MCP-first

Define the app's capabilities before designing UI:

1. Identify the user workflows the app should support.
2. [Define the MCP tools](https://developers.openai.com/apps-sdk/plan/tools) needed for those workflows.
3. Write clear tool names, descriptions, input schemas, and output schemas.
   Use the [metadata optimization guide](https://developers.openai.com/apps-sdk/guides/optimize-metadata)
   to improve discovery and model selection.
4. Mark every tool with accurate safety annotations, then review the
   [security and privacy guidance](https://developers.openai.com/apps-sdk/guides/security-privacy) for write
   actions, data handling, and network access.
5. Add [authentication](https://developers.openai.com/apps-sdk/build/auth) only for data or actions that
   require it.
6. Test the app from ChatGPT developer mode before packaging it into a plugin.

## Add UI if it materially improves the app experience

The [Apps SDK quickstart](https://developers.openai.com/apps-sdk/quickstart) shows how to build a simple
MCP-backed app with an optional UI component. The [Apps SDK](https://developers.openai.com/apps-sdk) helps
you build [MCP UI](https://developers.openai.com/apps-sdk/mcp-apps-in-chatgpt) for an MCP-backed app. It is
optional: use it when the app needs an embedded component, modal, fullscreen
view, or other custom interaction in ChatGPT. See
[Build your MCP UI](https://developers.openai.com/apps-sdk/build/chatgpt-ui) for UI-specific patterns.

Do not add UI just to show a banner ad or brand placement. The UI should
materially improve the user's workflow by making the app easier to inspect,
edit, compare, confirm, or navigate.

Even when you add UI, keep the tools decoupled from the rendering layer. Tools
should still return useful structured data and model-readable results, while UI
components focus on presentation and interaction. See
[Separate data processing from UI rendering](https://developers.openai.com/apps-sdk/build/chatgpt-ui#separate-data-processing-from-ui-rendering).

## Package the app as a plugin

After the app works in developer mode, package it into a plugin so users can
install it.

1. Create or scaffold the plugin folder. See
   [Build plugins](https://learn.chatgpt.com/docs/build-plugins#create-and-test-a-plugin-locally-that-points-to-an-mcp-server-backed-dev-mode-app).
2. Add the app reference to the plugin manifest.
3. Add bundled skills if ChatGPT should follow repeatable workflows alongside
   the app.
4. Test the plugin locally.
5. Review the Apps SDK
   [app guidelines](https://developers.openai.com/apps-sdk/app-guidelines), then
   submit it for review as part of a plugin when it is ready for public
   distribution. See [Submit plugins](https://learn.chatgpt.com/docs/submit-plugins).