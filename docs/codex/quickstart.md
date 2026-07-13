# Quickstart

## Where to use ChatGPT

Use ChatGPT across different surfaces, including the
[ChatGPT desktop app](https://learn.chatgpt.com/docs/app) and [ChatGPT on the web](https://learn.chatgpt.com/docs/web). Choose
the option that fits your work.

<Illustration description="Cards compare the ChatGPT desktop app and ChatGPT on the web">
  <QuickstartSetupSelector />
</Illustration>

If you're a developer and want to use Codex in your terminal or code editor,
  try [Codex CLI](https://learn.chatgpt.com/docs/codex/cli) or the [Codex IDE extension](https://learn.chatgpt.com/docs/codex/ide).

## Setup

{/* prettier-ignore */}
<Tabs
  id="codex-quickstart-setup"
  param="setup"
  defaultTab="web"
  size="md"
  tabs={[
    { id: "app", label: "Desktop" },
    { id: "web", label: "Web" },
  ]}
>
  <div slot="app">
The ChatGPT desktop app is available for Windows and macOS. Use it for projects,
local files, longer tasks, and quick conversations.

<WorkflowSteps variant="headings">
1. <h3 id="setup-app-install">Install the ChatGPT desktop app</h3>

    Choose the version for your operating system:

    <CodexAppDownloadCta client:load className="mb-4" />

2.  <h3 id="setup-app-sign-in">Open the ChatGPT desktop app and sign in</h3>

    Open the app, then sign in with your ChatGPT account.

    You may also use Codex with an API key. [Some features might not be available](https://learn.chatgpt.com/docs/pricing#feature-availability).

3.  <h3 id="setup-app-select-workspace">Select where ChatGPT should work</h3>

    Start a task, create a project, or open a folder. ChatGPT can read and modify
    files in the folder you choose. [Learn more about tasks and projects](https://learn.chatgpt.com/docs/projects).

4.  <h3 id="setup-app-start-task">Start your task</h3>

            <div class="grid gap-5 md:grid-cols-[minmax(0,1fr)_minmax(17rem,20rem)] md:items-start">

          <div>

                - For research, analysis, or deliverables such as documents, presentations,
                  spreadsheets, and Sites, select **ChatGPT Work** from the ChatGPT dropdown.
                - For software development with codebase context and developer tools, select
                  **Codex** from the ChatGPT dropdown.
                - For a quick question or conversation, open **Chat** separately.

                Learn more about [using ChatGPT](https://learn.chatgpt.com/docs/use-chatgpt).

              </div>

          <ChatGPTModeDropdown client:load />

    </div>

5.  <h3 id="setup-app-send-message">Send your first message</h3>

    Describe your goal and add any files or context ChatGPT needs. Try an example:

    <CodexPromptComposer
      client:load
      id="first-message-example"
      promptOptions={[
        {
          label: "Prepare a decision",
          prompt:
            "Review the reports and notes in this project, compare the options, and create a one-page decision memo with a recommendation, risks, open questions, and source links.",
        },
        {
          label: "Analyze spreadsheets",
          prompt:
            "Combine the spreadsheets in this folder, clean inconsistent records, identify the most important trends, and create a concise report with charts and plain-English takeaways.",
        },
        {
          label: "Improve this app",
          prompt:
            "Inspect this app, identify one high-impact usability improvement, implement it, update the relevant tests, and verify the result on mobile and desktop.",
        },
      ]}
      className="!mt-3 !mb-10 w-full max-w-3xl min-w-0"
    />

    Explore more [use cases](https://learn.chatgpt.com/use-cases).

</WorkflowSteps>

  </div>

  <div slot="web">
ChatGPT is available on the web and includes Chat and ChatGPT Work.

<WorkflowSteps variant="headings">
1. <h3 id="setup-web-sign-in">Open ChatGPT and sign in</h3>

Go to [chatgpt.com](https://chatgpt.com) and sign in with your ChatGPT account.

2.  <h3 id="setup-web-start-task">Start your task</h3>

            <div class="grid gap-5 md:grid-cols-[minmax(0,1fr)_minmax(17rem,20rem)] md:items-stretch">

          <div>

                - Select **Chat** to ask questions, explore ideas, and work through a topic
                  conversationally.
                - Select **Work** to research, analyze information, and create documents,
                  presentations, spreadsheets, Sites, or other finished work.

                Learn more about [using ChatGPT](https://learn.chatgpt.com/docs/use-chatgpt).

              </div>

          <ChatWorkSegmentPicker client:load />

    </div>

3.  <h3 id="setup-web-select-workspace">Select where ChatGPT should work</h3>

    Start a chat or select a project. Projects can include chats, files, and instructions.

4.  <h3 id="setup-web-send-message">Send your first message</h3>

    Describe your goal and add any files or context ChatGPT needs. Try an example:

    <CodexPromptComposer
      client:load
      id="web-first-message-example"
      destination="web"
      placeholder="Message ChatGPT"
      promptOptions={[
        {
          label: "Make a decision",
          prompt:
            "Research whether I should [decision], compare the best options, explain the tradeoffs for my situation, and recommend one with citations.",
        },
        {
          label: "Daily briefing",
          prompt:
            "Every weekday at 8:00 a.m., review my connected calendar and recent messages, then send me a briefing with today’s priorities, meeting prep, replies I owe, and blockers.",
        },
        {
          label: "Plan an event",
          prompt:
            "Help me plan my event. Ask me about the occasion, guests, date, location, budget, and anything else you need. Then create a timeline, budget, invitation copy, and checklist, and publish a Site I can use to invite guests and collect RSVPs.",
        },
      ]}
      className="!mt-3 !mb-10 w-full max-w-3xl min-w-0"
    />

</WorkflowSteps>

  </div>

</Tabs>
<div class="h-6" aria-hidden="true"></div>
## Next steps
[<IconItem title="Learn more about the ChatGPT desktop app" className="mt-2">
    <span slot="icon">
      <OpenBook />
    </span>
    Use the ChatGPT desktop app to work with your local projects.
  </IconItem>](https://learn.chatgpt.com/docs/app)
[<IconItem title="Import your setup" className="mt-2">
    <span slot="icon">
      <CompareArrows />
    </span>
    Bring supported setup, projects, and recent work into ChatGPT.
  </IconItem>](https://learn.chatgpt.com/docs/import)