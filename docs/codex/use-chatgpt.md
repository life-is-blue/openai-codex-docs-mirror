# Use ChatGPT

{/* vale alex.Condescending = NO */}

## Go from idea to useful result

ChatGPT is an AI agent that you communicate with in natural language:

<WorkflowSteps>
1. Start with a question, an idea, rough notes, a file, or a task you need to
   complete.

2. Ask ChatGPT to explain information, develop ideas, draft content, research a
   topic, analyze materials, or create something new.

3. Add the context and tools it needs, such as files, web search, projects, or
   plugins.

4. Review the result, correct the direction, and ask for changes. You don't need
   a perfect first prompt or special commands.

</WorkflowSteps>

## Choose how you want to work

Open Quick Chat to start an ordinary ChatGPT chat for a question or
conversation. Use ChatGPT Work when you want to carry a larger task through to
a reviewable result. For software development and technical tasks, use Codex.

| Choose       | When you want to                              | Examples                                                                     |
| ------------ | --------------------------------------------- | ---------------------------------------------------------------------------- |
| Chat         | Work through something with ChatGPT           | Ask a question, search the web, brainstorm, draft a message, compare options |
| ChatGPT Work | Define an outcome and get a reviewable result | Create a deck, analyze files, draft a report, build a project plan           |
| Codex        | Work on software or technical tasks           | Debug code, run tests, review a PR, implement a feature                      |

Quick Chat is a good place to begin when you want to:

- Ask a question, search the web, or learn about a topic.
- Get an unfamiliar idea explained in simpler language.
- Brainstorm possibilities.
- Draft a message, outline, or piece of content.
- Rewrite something for a different tone or audience.
- Summarize notes, text, or a file.
- Compare options or think through a decision.
- Clarify what you need before starting a larger task.

When you need a substantial, reviewable result, switch to Work and describe the
outcome you need. See [Get started with Work](https://learn.chatgpt.com/docs/get-started-with-work) for
example tasks, prompts, and best practices.

### Talk to ChatGPT naturally

Write as if you were explaining the request to a helpful colleague. State what
you want to accomplish, add the details that change the answer, and describe the
format you need. Your first prompt is only a starting point—you can add context
or refine the result with follow-up messages.

<CodexPromptComposer
  client:load
  id="natural-chatgpt-prompt-example"
  destination="web"
  placeholder="Message ChatGPT"
  promptOptions={[
    {
      label: "Start simple",
      prompt:
        "Help me plan a 30-minute team meeting about our new customer feedback process.",
    },
    {
      label: "Add context",
      prompt:
        "Help me plan a 30-minute team meeting about our new customer feedback process. The audience is a customer support team that hasn't seen the process before. Include five minutes for questions and end with clear next steps.",
    },
    {
      label: "Choose a format",
      prompt:
        "Create a 30-minute agenda for a customer support team that hasn't seen our new customer feedback process before. Include five minutes for questions, end with clear next steps, and format it so I can paste it into a calendar invitation.",
    },
  ]}
  className="!mt-4 !mb-8 w-full max-w-3xl min-w-0"
/>

You can continue with simple directions such as:

- “Make this shorter.”
- “Give me three different approaches.”
- “What assumptions are you making?”
- “Ask me questions before you continue.”

Learn more about [prompting](https://learn.chatgpt.com/docs/prompting), or take the
[AI Foundations course](https://academy.openai.com/home/courses/ai-foundations-juzjs)
for guided practice.

## Bring the right context into ChatGPT

Give ChatGPT the information, tools, and instructions that matter to the task.
You don't need to provide everything—include the context that changes what a
good result looks like.

### Keep related work in a project

Projects help you organize ChatGPT around a topic, goal, or ongoing body of
work. Keep related conversations, tasks, files, and instructions in one project
when the work will continue over time or depend on the same context. [Learn more
about projects.](https://learn.chatgpt.com/docs/projects)

### Attach files

You can upload or attach documents, presentations, spreadsheets, PDF files, images,
and data exports. Use them when you want ChatGPT to:

- Summarize or compare them.
- Find patterns or inconsistencies.
- Extract, clean, or reorganize information.
- Use them as source material for a new file.

When ChatGPT creates a file, open the preview and check its contents. You can
then ask for changes without starting over. Learn more about
[working with files](https://learn.chatgpt.com/docs/artifacts-viewer).

### Connect tools with plugins

Plugins can connect ChatGPT to the tools and information you use for work, such
as Google Drive, SharePoint, Salesforce, or Gong. Use them when a task depends
on information outside the conversation, actions in another system, or a
repeatable workflow.

Plugin availability depends on your plan, workspace settings, and the plugin
itself. Learn more about [skills and plugins](https://learn.chatgpt.com/docs/skills-and-plugins).

## Make the result ready to use

Treat the first result as a draft you can inspect, challenge, and improve. A
polished response can still be incomplete or wrong, so review the details that
matter before you use or share it.

**Check the work:**

- Verify important numbers, names, dates, quotes, and claims.
- Open generated files and inspect every section, tab, slide, or page.
- Confirm that ChatGPT used the correct and most current source material.
- Look for missing information and unsupported assumptions.
- Ask for focused revisions when the result misses the goal.

Then ask ChatGPT to pressure-test the result:

- “What sources did you use for this?”
- “Cite the source for each major claim.”
- “What assumptions did you make?”
- “What information were you unable to access?”
- “What would change your recommendation?”
- “Check this result against the original files.”

If ChatGPT couldn't access a source or complete part of the task, ask it to say
so plainly. An explicit gap is easier to address than a confident guess.

Legal, financial, medical, security, and other high-stakes decisions require
  appropriate expert review. Use ChatGPT to support informed judgment, not
  replace it.

## Next steps

<div class="not-prose flex flex-col gap-4 pt-4 [&_.icon-item-right]:min-w-0 [&>a]:min-w-0 [&>a]:no-underline">
  [<IconItem title="Open the quickstart">
      <span slot="icon">
        <OpenBook />
      </span>
      Start using ChatGPT with a guided first task.
    </IconItem>](https://learn.chatgpt.com/docs/quickstart)

[<IconItem title="Learn about prompting">
    <span slot="icon">
      <Chat />
    </span>
    Write useful prompts for questions, finished work, and coding tasks.
  </IconItem>](https://learn.chatgpt.com/docs/prompting)

  [<IconItem title="Personalize ChatGPT">
      <span slot="icon">
        <Settings />
      </span>
      Set preferences and carry useful context across chats and tasks.
    </IconItem>](https://learn.chatgpt.com/docs/personalize)
</div>