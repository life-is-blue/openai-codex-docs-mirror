# Pets

Pets are optional animated companions for following work. Where a pet appears
and what it shows depend on the interface you use. Choosing a pet changes its
appearance, not how ChatGPT completes tasks.

<div class="flow-root">
  <div class="w-full md:float-right md:ml-6 md:w-64 xl:w-72">
    <CodexPetsDemo client:load mobileAlignment="left" />
  </div>



## Use a floating pet

In the ChatGPT desktop app, a pet can float above other app windows and help
you follow activity across your tasks.

### Choose and wake a pet

1. Open the profile menu at the bottom of the app and select **Pets**. You can
   also open [**Settings**](codex://settings) and go to **Pets**.
2. Choose a built-in or custom pet.
3. Enter `/pet`, or open the command menu and select **Wake Pet**.

Select **Tuck Away Pet** in **Settings > Pets** or the command menu, or enter
`/pet` again, to hide the pet. Your selection and the pet's position persist
when you reopen the app.

When you select a custom pet, it also appears in your **Profile** view.

### Understand pet status

| Status          | Meaning                                                  |
| --------------- | -------------------------------------------------------- |
| **Running**     | A task is actively working.                              |
| **Needs input** | A task needs your approval, answer, or another decision. |
| **Ready**       | A task has completed and has unread activity.            |
| **Blocked**     | A task failed or encountered a system error.             |

When more than one task has activity, the pet prioritizes tasks that need
input, followed by blocked, ready, and running tasks. Open the activity tray to
choose a task.

Select the pet to return to ChatGPT, or select an activity to open its task.
The activity tray is separate from [system
notifications](https://learn.chatgpt.com/docs/notifications?surface=app).

### Follow Computer Use

On macOS, the [Computer Use](https://learn.chatgpt.com/docs/computer-use) picture-in-picture window can
attach to an awake pet. Move the pet, and the window follows.

### Create a custom pet

1. Open **Settings > Pets** and select **Create your own pet**.
2. The app installs the bundled `hatch-pet` skill, reloads skills, and opens a
   new task.
3. Describe the pet you want and send the prompt.
4. When the task finishes, return to **Settings > Pets**, select **Refresh**,
   and choose your new pet.

Custom pets created in the desktop app are stored locally on your computer.
They don't automatically sync to ChatGPT web.

### Reduce animation

Pets respect your operating system's reduced motion setting. When reduced
motion is enabled, the pet uses a still frame instead of sprite animation.









</div>

## Related docs

- [Notifications](https://learn.chatgpt.com/docs/notifications)
- [Long-running work](https://learn.chatgpt.com/docs/long-running-work)
- [ChatGPT desktop app settings](https://learn.chatgpt.com/docs/reference/settings#pets)