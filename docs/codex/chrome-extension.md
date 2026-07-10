# Chrome extension

Use ChatGPT with Chrome for browser tasks that need your signed-in browser
state. Use it when ChatGPT needs to read or act on sites such as LinkedIn,
Salesforce, Gmail, or internal tools.

For local development servers, file-backed previews, and public pages that do
not require sign-in, use the [built-in browser](https://learn.chatgpt.com/docs/browser?surface=app) first. The
built-in browser keeps preview and verification work inside ChatGPT without using
your Chrome profile.

ChatGPT can also switch between tools as a task requires, using plugins when a
dedicated integration is available, Chrome when it needs logged-in browser
context, and the built-in browser for localhost.

<div className="not-prose my-4">
  <Alert
    client:load
    color="warning"
    variant="soft"
    description="Treat page content as untrusted context, and review the website before allowing ChatGPT to continue."
  />
</div>

## Set up Chrome from Plugins

Install the Chrome plugin to start setup:

1. Open the ChatGPT desktop app, select ChatGPT Work or Codex, and go to **Plugins**.
2. Add the **Chrome** plugin.
3. Follow the setup flow. It guides you through installing the [Chrome
   extension](https://chromewebstore.google.com/detail/codex/hehggadaopoacecdllhhajmbjkdcmajg)
   and approving Chrome's permission prompts.
4. Open Chrome and confirm the extension shows **Connected**.

After the plugin setup is complete, start a new task in Work or Codex. ChatGPT
can suggest Chrome when a task needs a signed-in website. You can also invoke it
directly in a prompt:

```text
@Chrome open Salesforce and update the account from these call notes.
```

If Chrome isn't already open, ChatGPT can open it. Chrome browser tasks run in
Chrome tab groups so the work for a task stays grouped together.

## Control website access

By default, ChatGPT asks before it interacts with each new website. ChatGPT bases
the prompt on the website host, such as `example.com`.

When ChatGPT asks to use a website, you can choose the option that matches the
task and your risk tolerance:

- Allow the website for the current task.
- Always allow the host so ChatGPT can use that website again without asking.
- Decline the website.

### Manage the allowlist and blocklist

In Computer Use settings, you can manage an allowlist and blocklist for
domains. The allowlist contains domains ChatGPT can use without asking again. The
blocklist contains domains ChatGPT shouldn't use.

Removing a domain from the allowlist means ChatGPT asks again before using it.
Removing a domain from the blocklist means ChatGPT can ask again instead of
treating the domain as blocked.

#### Always allow browser content <ElevatedRiskBadge class="ml-2" />

If you turn on always allow browser content, ChatGPT no longer asks for
confirmation before using websites.

#### Browser history <ElevatedRiskBadge class="ml-2" />

Browser history can include sensitive telemetry, internal URLs, search terms,
and activity from Chrome sessions on signed-in devices. If you allow ChatGPT to
access browser history, relevant history entries can become part of the context
ChatGPT uses for the task. Malicious or misleading page content can increase the
risk that ChatGPT copies this data somewhere unintended.

ChatGPT asks when it wants to use browser history. ChatGPT scopes history access to
the request, and history doesn't have an always-allow option.

## Data and security

### Chrome extension permissions

Chrome asks you to accept extension permissions when you install the extension.
The permission prompt may include:

- Access the page debugger
- Read and change all your data on all websites
- Read and change your browsing history on all your signed-in devices
- Display notifications
- Read and change your bookmarks
- Manage your downloads
- Communicate with cooperating native applications
- View and manage your tab groups

These Chrome permissions make the extension capable of operating browser
workflows. ChatGPT still uses its own confirmations, settings, allowlists, and
blocklists before using websites or browser history during a task.

### Memories

Computer Use follows your Memories setting. If Memories is on, ChatGPT can
use relevant saved memories while working in Chrome. If Memories is off, browser
control doesn't use memories.

### What OpenAI stores from browsing

OpenAI doesn't store a separate complete record of your Chrome actions from the
extension. OpenAI stores browser activity only when it becomes part of the ChatGPT
context, such as text ChatGPT reads from a page, screenshots, tool calls,
summaries, messages, or other content included in the task.

Your ChatGPT data controls apply to content processed in context.
Avoid sending secrets or highly sensitive data through browser tasks unless
they're required and you are present to review each prompt.

## Troubleshooting

If ChatGPT can't connect to Chrome, first confirm the website ChatGPT is trying to
access isn't in the blocklist in Settings. If the website isn't blocked, work
through these checks:

1. Open the extension from the Chrome toolbar or Chrome's extensions
   menu. Make sure it shows **Connected**. If it shows disconnected or mentions
   a missing native host, remove and re-add the Chrome plugin from **Plugins**
   in Work or Codex in the ChatGPT desktop app, then follow the setup flow
   again.
2. In the app, select Work or Codex, open **Plugins**, and confirm that the
   Chrome plugin is on. If the plugin is off, turn it on and
   try the task again.
3. Make sure you are using the same Chrome profile where the extension is
   installed. If you use more than one Chrome profile, install and enable the
   extension in the active profile.
4. Start a new task in Work or Codex and try the Chrome task again. This can
   clear task-specific connection state.
5. Restart Chrome and the app, then try again. If the extension
   still doesn't connect, uninstall the Chrome extension, remove and re-add the Chrome
   plugin from **Plugins**, and follow the setup flow again.
6. If the extension shows **Connected** but ChatGPT still can't use Chrome, run
   `/feedback` in the app and include the task ID when you contact
   support.

<CodexScreenshot
  alt="Chrome extension showing connected status"
  lightSrc="/images/codex/app/chrome-connected-light.png"
  darkSrc="/images/codex/app/chrome-connected-dark.png"
  maxHeight="300px"
  class="mt-4"
/>

### Upload files

If a Chrome task needs to upload a file from your computer, allow the Chrome
extension to access file URLs in Chrome:

1. In Chrome, open the extensions icon in the toolbar, then click **Manage
   Extensions**.
2. On the extension card, click **Details**.
3. Turn on **Allow access to file URLs**.

After you change the setting, start the Chrome task again.

<CodexScreenshot
  alt="Chrome extension settings showing Allow access to file URLs enabled for ChatGPT"
  lightSrc="/images/codex/app/chrome-file-url-access-light.webp"
  darkSrc="/images/codex/app/chrome-file-url-access-dark.webp"
  maxHeight="420px"
  class="mt-4"
/>