# Codex Security plugin quickstart

Codex Security is a security-review plugin for Codex that scans your code for
vulnerabilities, validates plausible findings, and presents evidence and
remediation guidance in a reviewable workspace. Use it to find security issues
in code you own or have authorization to assess before they reach production.

This quickstart takes you through one recommended first run: an ordinary,
read-only scan of a local repository in Codex.

This page covers the plugin that runs in a local Codex chat. To scan a
  connected GitHub repository in Codex cloud, see [Codex Security cloud
  setup](https://learn.chatgpt.com/docs/security/setup).

## Install the plugin



1. Open the repository you want to assess in Codex in the [ChatGPT desktop
   app](https://chatgpt.com/download/).
2. Go to **Plugins** and search for **Codex Security**, or select the button
   below:

   <div className="not-prose my-6">
     <ButtonLink
       href="codex://plugins/install/codex-security?marketplace=openai-curated"
       color="primary"
       variant="solid"
       size="lg"
       pill
     >
       Install the Codex Security plugin
     </ButtonLink>
   </div>

3. Start a new chat in Codex for that repository (don't continue in a chat that
   was already open).







## Run your first scan

For the best scan quality, use `gpt-5.6`
with `high` or `xhigh` reasoning effort.



<VideoPlayer
  src="/videos/codex/security/scan-setup-to-findings.mp4"
  poster="/videos/codex/security/scan-setup-to-findings-poster.webp"
/>

<WorkflowSteps variant="headings">

1. Ask for an ordinary scan

   Send this prompt in the new chat:

   ```text
   Run a Codex Security scan on this repository.
   ```

2. Confirm the setup

   Codex opens a setup workspace before it starts. For your first run, use these
   settings:
   - **Scan type:** `Codebase`
   - **Deep scan:** Off
   - **Scan area:** `Entire codebase`
   - **Threat model scoping guidance:** Leave blank unless you already know a
     specific attack vector or application area that deserves priority.

   Confirm that **Codebase**, **Current branch**, and **Last commit** identify
   the repository you intended to scan. Then select **Start scan**.

   <figure className="not-prose my-6">
     <div className="overflow-hidden rounded-xl border border-subtle bg-surface">
       <img
         src={scanSetup.src}
         alt="Codex Security setup workspace configured to scan an entire codebase"
         className="block h-auto w-full"
       />
     </div>
     <figcaption className="mt-3 text-sm text-secondary">
       Configure the scan target, scan area, branch, and optional threat model
       guidance before starting the scan.
     </figcaption>
   </figure>

3. Let the scan finish

   The scan can take time. Keep the scan running until the workspace reports
   completion. If Codex identifies a configuration limitation, review the exact
   limitation and proposed change before allowing it to update your
   configuration.

4. Review the result

   Use the UI to browse findings, or open `report.md` as the entry point to the
   complete scan directory.

   <figure className="not-prose my-6">
     <div className="overflow-hidden rounded-xl border border-subtle bg-surface">
       <img
         src={findingsWorkspace.src}
         alt="Completed Codex Security findings workspace for OWASP Juice Shop"
         className="block h-auto w-full"
       />
     </div>
     <figcaption className="mt-3 text-sm text-secondary">
       Browse findings by severity, category, directory, patch status, and
       review status.
     </figcaption>
   </figure>

</WorkflowSteps>







## What the scan creates



Every completed scan opens a findings workspace. Use it to review findings and
coverage without inspecting raw artifacts. The scan also creates the files
below.







- `report.md`, the primary readable entry point to the scan results.
- `findings/<slug>/`, with one detailed vulnerability report per reportable
  finding and supporting proof-of-concept files when available.
- `hardening/`, with a structural hardening portfolio and supporting proposals
  or diagrams when the scan has reportable findings.
- Structured scan data in `scan-manifest.json`, `findings.json`, and
  `coverage.json` for automation and integrations. You normally don't need to
  open these files yourself.

Keep the full scan directory together when sharing or archiving results so the
links from `report.md` continue to work.

## Choose your next workflow

- [Run a standard or scoped scan](https://learn.chatgpt.com/docs/security/plugin/scans) when you want
  to scan a repository or one folder with the default workflow.
- [Run a deep scan](https://learn.chatgpt.com/docs/security/plugin/deep-scans) when you need a more
  comprehensive scan and can wait longer for it to finish.
- [Review code changes](https://learn.chatgpt.com/docs/security/plugin/code-changes) when the target is
  a pull request, commit, branch range, or working-tree patch.
- [Triage a backlog](https://learn.chatgpt.com/docs/security/plugin/triage-backlog) when you have
  existing security findings to review.
- [Fix and verify a finding](https://learn.chatgpt.com/docs/security/plugin/fix-findings) after you
  accept one finding for remediation.
- [Export or track findings](https://learn.chatgpt.com/docs/security/plugin/export-findings) when you
  need JSON, CSV, SARIF, an approval-gated Linear, GitHub, or Jira issue, or a
  private draft GitHub Security Advisory.
- [Write vulnerability reports](https://learn.chatgpt.com/docs/security/plugin/vulnerability-reports)
  when you want to turn supplied findings, disclosure notes, source, and PoCs
  into polished, self-contained reports.
- [Propose security hardening](https://learn.chatgpt.com/docs/security/plugin/security-hardening) when
  you want structural or architectural options based on scan results or other
  security evidence.