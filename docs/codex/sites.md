# Sites

Sites is in public beta. Availability can depend on your plan, region, and
  workspace settings.

Sites lets ChatGPT create, host, refine, and share websites, web apps, and games.
Use Sites when you want to turn a prompt or compatible existing project into a
hosted experience without setting up a separate deployment workflow.



Open **Sites** in the ChatGPT desktop app. You can start a site from a prompt or
from a compatible local project, then return to the Sites view to manage it.









Every Sites deployment URL is a production deployment. If you want to review a
  build before it becomes live, ask ChatGPT to save a version without deploying
  it.

## Get started with Sites

<WorkflowSteps variant="headings">

1. Describe the Site

   Describe the audience, purpose, required behavior, and information the Site
   should use.

2. Review the Site

   Review the generated content and behavior. Check that the Site uses the
   intended information and handles data as expected.

3. Refine the Site

   Describe the changes you want. Add relevant files or visual context when
   they will help ChatGPT make the change.

4. Manage and share the Site

   Return to **Sites** to reopen or refine the Site. When it's ready, choose who
   can visit it and share the resulting link.

</WorkflowSteps>



## Prompt Sites for common tasks

For a new website, dashboard, or internal tool, include the audience, core
experience, and required information:

```text
Build a project request dashboard for my operations team. Let team members
submit requests, see who owns each one, update the status, and filter the list.
Require people to sign in with their workspace account, and keep the request
data saved between visits.
```



For an existing project, ask Sites to prepare and publish the current app:

```text
Deploy this project with Sites. Check whether it is compatible, make any
required changes, and give me the deployment URL.
```



When a site needs durable application data or uploaded files, say so in the
request:

```text
Add player scores and avatar uploads to this game. Keep the scores and uploaded
avatars between visits.
```

Browse the [Sites showcase](https://developers.openai.com/showcase) for deployed internal apps and the full
  prompts used to create them.

## Understand projects, versions, and deployments

A Site is a persistent hosted output that you can reopen, refine, configure,
and share from **Sites** in ChatGPT.



A Sites project links a local source project to hosting managed through Sites.
Sites stores that linkage and optional storage binding names in
`.openai/hosting.json`. A newly created local starter can begin without a
`project_id`; Sites adds one after it provisions the hosted project.

For example, a provisioned site that uses a relational database binding and no
file storage can contain:

```json
{
  "project_id": "<project-id>",
  "d1": "DB",
  "r2": null
}
```







Sites publishing has two separate stages:

1. **Save a version.** ChatGPT builds a deployable version. For a local source
   project, ChatGPT associates the version with the Git commit used for the
   build. Use this stage when you want a reviewable deployment candidate.
2. **Deploy a version.** ChatGPT publishes a saved version and reports the
   production URL when deployment succeeds. Use this only when you intend for
   the selected audience to access the site.

Ask ChatGPT to list or inspect saved versions when you need to identify a
previous deployment candidate.



## Choose a supported site shape

For new projects, the Sites workflow can start with its recommended Site
starter. For an existing project, ask ChatGPT to confirm that the project can
produce compatible deployment artifacts before you request a deployment.

Tell ChatGPT about the product behavior you need so it can select the appropriate
site shape:

| Site need                                                      | What to ask Sites for                                                         |
| -------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| Content-led website or landing page                            | A Site with no persistent application state unless the experience requires it |
| Saved records, user progress, or game scores                   | D1, a relational database for durable structured data                         |
| Images, documents, audio, video, or other uploads              | R2, object storage for files                                                  |
| Uploaded files with searchable metadata                        | D1 for metadata and R2 for file contents                                      |
| Internal site that needs the current workspace user's identity | Workspace-authenticated user identity                                         |
| Public sign-in or an external identity provider                | An authentication-enabled Site                                                |

Don't request durable storage for temporary presentation state, such as a
theme choice or a dismissed banner. Do request it for product data that people
expect the hosted site to remember.

## Control access and secrets

Hosting a Site doesn't automatically make it public. Keep access limited while
you review the content, data handling, and expected audience.

Depending on your account and workspace settings, sharing options can include:

- Only you or people you invite.
- Everyone in your workspace.
- Anyone with the link.

Sharing lets people visit the Site; it doesn't let them edit it. Workspace
admins can restrict whether members can share Sites publicly.

For example:

```text
Change this Site's access to everyone in my workspace after showing me the
current Site and confirming its URL.
```

### Configure runtime environment values

Open **Sites**, then open the Site's settings to add, update, or remove hosted
environment variables and secrets. Keep secret values out of prompts, attached
files, and Site content.





Don't store these values in `.openai/hosting.json`. Keep local `.env` and
`.env.example` files aligned with the keys needed for local development, and
don't commit secret values.

When you add, update, or remove hosted environment values, ask ChatGPT to
redeploy the approved saved version so the next deployment uses the updated
configuration.



## Review before you share

Before you share a Site:

- Review the Site's content and behavior in the preview.
- Check that the Site handles information and uploaded files as expected.
- Confirm that the Site doesn't expose confidential information or secret
  values.
- Choose the narrowest sharing option that fits the intended audience.
- Open the shared Site and confirm that the intended audience can visit it.



For a Site built from a local project, also review the source changes and any
database migrations in the Codex [review pane](https://learn.chatgpt.com/docs/code-review?surface=app).



## Related documentation



- [ChatGPT desktop app](https://learn.chatgpt.com/docs/app) introduces app navigation, projects, and tasks.
- [Review and ship changes](https://learn.chatgpt.com/docs/code-review?surface=app) explains how to inspect source
  changes before publishing them.