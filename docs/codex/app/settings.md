# Settings

Use the settings panel to personalize the app and manage everyday preferences.
Open [**Settings**](codex://settings) from the app menu or press

<kbd>Cmd</kbd>+<kbd>,</kbd> on macOS or <kbd>Ctrl</kbd>+<kbd>,</kbd> on Windows.

## General

Require <kbd>Cmd</kbd>+<kbd>Enter</kbd> for multiline prompts, or turn on
**Prevent sleep while running** so local tasks can continue while you step away.
Under **Follow-up behavior**, choose whether a message sent while ChatGPT works
should steer the current run or wait for the next run.

## Profile

Use **Profile** to review activity insights, lifetime tokens, peak tokens,
streaks, your longest task, and token activity. You can also update your profile
details, such as your picture, display name, and username, and save a profile
card with usage highlights. Sharing profile cards is available on consumer
ChatGPT plans.

Eligible users can also send Codex invitations from the profile menu. Choose
**Invite a friend** on an eligible personal plan or **Invite a coworker** in an
eligible Business workspace. See
[Invite friends and coworkers](https://learn.chatgpt.com/docs/pricing#invite-friends-and-coworkers) for
current rewards, limits, and eligibility.

## Keyboard shortcuts

Open **Keyboard Shortcuts** to review commands, change bindings, or reset custom
shortcuts to their defaults. Use the search field to find shortcuts by command
name, or switch to keystroke search and press a key combination to find the
command that uses it.

## Notifications

Choose when turn completion notifications appear, and whether the app should prompt for
notification permissions.

## Appearance

In **Settings**, you can change the app appearance by choosing a base theme,
adjusting accent, background, and foreground colors, and changing the UI and
code fonts. You can also share your custom theme with friends.

<CodexScreenshot
  alt="ChatGPT desktop app Appearance settings showing theme selection, color controls, and font options"
  lightSrc="/images/codex/app/theme-selection-light.webp"
  darkSrc="/images/codex/app/theme-selection-dark.webp"
  maxHeight="720px"
  class="mb-8"
/>

## Pets

<div class="grid gap-5 md:grid-cols-[minmax(0,1fr)_minmax(15rem,50%)] md:items-start xl:grid-cols-[minmax(0,1fr)_minmax(16rem,30%)]">
  <div>
    Pets are optional animated companions for the app. In **Settings > Pets**,
    choose a built-in or custom pet, then use `/pet`, **Wake Pet**, or
    **Tuck Away Pet** to control the floating overlay.

    See [Pets](https://learn.chatgpt.com/docs/pets?surface=app) to understand pet status, follow
    activity across tasks, or create your own pet.

  </div>

  <CodexPetsDemo client:load />
</div>

<a id="browser-use"></a>

## Browser

Use these settings to install or enable the bundled Browser plugin, set up the
[Chrome extension](https://learn.chatgpt.com/docs/chrome-extension), and manage allowed and blocked
websites. ChatGPT asks before using a website unless you've allowed it. Removing
a blocked site lets ChatGPT ask again before using it in the browser.

See [Built-in browser](https://learn.chatgpt.com/docs/browser?surface=app) for browser preview, comment, and
Computer Use workflows.

## Computer Use

Check your Computer Use settings to review desktop-app access and related
preferences after setup. On macOS, revoke system-level access by updating Screen
Recording or Accessibility permissions in macOS Privacy & Security settings.

## Personalization

Choose **Friendly**, **Pragmatic**, or **None** as your default personality. Use
**None** to disable personality instructions. You can update this at any time.

You can also add your own custom instructions. Editing custom instructions updates your
[personal instructions in `AGENTS.md`](https://learn.chatgpt.com/docs/agent-configuration/agents-md).

## Suggested prompts

Use context-aware suggestions to surface follow-ups and tasks you may want to resume when you
start or return to ChatGPT.

## Memories

Enable Memories, where available, to let ChatGPT carry useful context from past
chats and tasks into future work. See [Memories](https://learn.chatgpt.com/docs/customization/memories)
for setup, storage, and controls for individual chats and tasks.

## Archived tasks

The **Archived tasks** section lists archived tasks with dates and project
context. Use **Unarchive** to restore a task.

<a id="keep-an-app-chat-near-your-work"></a>

## Keep a task near your work

In the ChatGPT desktop app, pop out an active task into a separate window and place it
next to your browser, editor, or design preview. Turn on **Always on top** when
you want the task to remain visible while you work in another app.

<CodexScreenshot
  alt="ChatGPT desktop app task displayed in a floating pop-out window"
  lightSrc="/images/codex/app/popover-light.webp"
  darkSrc="/images/codex/app/popover-dark.webp"
  maxHeight="400px"
  class="my-8"
/>