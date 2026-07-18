# Deploy the Windows app

Choose a deployment path based on who controls installation and updates and
whether your network allows Microsoft's app-distribution services. The app is
Store-signed, but users don't need to open the Microsoft Store. Standard
installation and updates use Microsoft's app installation and Windows Update
services.

| Scenario                                                       | Deployment path                                                                                         |
| -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| Users install and update their own apps                        | Use the [web installer](https://get.microsoft.com/installer/download/9PLM9XGG6VKS?cid=website_cta_psi). |
| IT deploys the app and Microsoft update services are available | Deploy the Microsoft Store app through Intune or another management tool.                               |
| IT controls update timing or blocks Microsoft update services  | Redeploy each new version through your software-management process.                                     |
| Your network blocks Microsoft app-distribution services        | Deploy the Store-signed MSIX package for each device architecture.                                      |

## Let users install and update the app

If users can manage their own applications, direct them to the
[web installer](https://get.microsoft.com/installer/download/9PLM9XGG6VKS?cid=website_cta_psi).
The installer provides the standard installation and automatic-update
experience. Microsoft Store components may appear during installation or
updates, but users don't need to browse the Store themselves.

You can also install the app from the command line:

```powershell
winget install --id 9PLM9XGG6VKS -s msstore
```

## Deploy with an enterprise management tool

If your organization centrally manages software, deploy the Microsoft Store app
through Microsoft Intune or another compatible mobile device management (MDM)
or software-deployment platform. Search for ChatGPT from OpenAI in the
Microsoft Store app flow, or use this Store product ID:

```text
9PLM9XGG6VKS
```

This is the recommended enterprise deployment method when your environment
allows Microsoft Store app deployment and update endpoints. Users don't need to
open the Microsoft Store themselves.

For Intune setup details, see
[Add Microsoft Store apps to Microsoft Intune](https://learn.microsoft.com/en-us/intune/app-management/deployment/add-microsoft-store).

## Control update timing

If your organization blocks automatic app updates, Windows Update, or Microsoft
Store update endpoints, your IT team owns the update lifecycle. Codex can run in
this environment, but you must redeploy newer packages through your change
management process.

Redeploy the package with each Codex release when possible. If that cadence
isn't practical, check for a newer package at least weekly and redeploy when a
newer version is available. Users should restart the app after you deploy an
update.

Deferring updates is a security and reliability tradeoff because the app
includes browser and runtime components that receive regular updates.

## Deploy without Microsoft distribution services

If your environment can't use the standard Microsoft distribution services,
download the Store-signed MSIX package for each device architecture:

| Device architecture | Package                                                                                  |
| ------------------- | ---------------------------------------------------------------------------------------- |
| x64                 | [ChatGPT-x64.msix](https://persistent.oaistatic.com/codex-app-prod/ChatGPT-x64.msix)     |
| Arm64               | [ChatGPT-arm64.msix](https://persistent.oaistatic.com/codex-app-prod/ChatGPT-arm64.msix) |

These stable links point to the latest published Store package. For offline
deployment workflows that require a license file, also download the
[offline license (`ChatGPT-License.xml`)](https://persistent.oaistatic.com/codex-app-prod/ChatGPT-License.xml).
Ingest the appropriate MSIX and, when required, the license file into your MDM
or software-deployment platform.

This deployment path:

- Supports deployment in restricted environments.
- Supports x64 and Arm64 devices.
- Doesn't provide a standalone MSI or non-Store EXE.
- Doesn't let users update the app themselves.
- Requires your organization to deploy newer packages when updating the app.

## Related resources

- [ChatGPT desktop app for Windows](https://learn.chatgpt.com/docs/windows/windows-app)