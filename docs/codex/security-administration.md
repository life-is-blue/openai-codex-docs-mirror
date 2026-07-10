# Security

<CodexDocsOverviewLanding
  title="Security"
  description="Control what ChatGPT and Codex developer tools can access, understand how work is isolated, and apply safeguards for security-sensitive tasks."
  intro="Security controls define what ChatGPT and Codex developer tools can access and how sensitive actions are reviewed. Permissions, sandboxing, approvals, and network access establish trust boundaries. Codex Security helps find and remediate vulnerabilities, and cyber safety guidance explains how security-sensitive work is handled."
  primaryCta={{
    label: "Explore permissions",
    href: "/codex/permissions",
  }}
  hero={{
    illustration: "security",
    backgroundImage: "/images/codex/codex-wallpaper-1.webp",
    alt: "ChatGPT approval options for default, automatic, full, and custom access",
  }}
  sections={[
    {
      title: "Permissions",
      description:
        "Control filesystem, network, command, approval, and review behavior.",
      pages: [
        {
          title: "Permissions",
          description:
            "Choose a profile for filesystem, command, and network access.",
          href: "/codex/permissions",
          icon: "lock",
        },
        {
          title: "Sandboxing",
          description:
            "Understand how Codex isolates commands and file changes.",
          href: "/codex/sandboxing",
          icon: "shieldCheck",
        },
        {
          title: "Auto-review",
          description:
            "Review actions automatically against your configured policy.",
          href: "/codex/sandboxing/auto-review",
          icon: "dataControls",
        },
        {
          title: "Agent approvals and security",
          description: "Decide when Codex must ask before taking an action.",
          href: "/codex/agent-approvals-security",
          icon: "userLock",
        },
        {
          title: "Internet access",
          description: "Control which domains cloud tasks can reach.",
          href: "/codex/cloud/internet-access",
          icon: "webSearch",
        },
      ],
    },
    {
      title: "Codex Security",
      description: "Find, understand, and remediate vulnerabilities.",
      pages: [
        {
          title: "Codex Security overview",
          description:
            "Assess code and turn reviewed findings into focused fixes.",
          href: "/codex/security",
          icon: "shieldCheck",
        },
        {
          title: "FAQ",
          description:
            "Get answers about scans, findings, privacy, and access.",
          href: "/codex/security/faq",
          icon: "chat",
        },
        {
          title: "Codex Security plugin",
          description:
            "Run security workflows from the ChatGPT desktop app and Codex CLI.",
          href: "/codex/security/plugin",
          icon: "plugin",
        },
        {
          title: "Codex Security cloud setup",
          description:
            "Connect repositories and configure cloud security scans.",
          href: "/codex/security/setup",
          icon: "storage",
        },
        {
          title: "Threat model",
          description: "Review and improve the threat model for your codebase.",
          href: "/codex/security/threat-model",
          icon: "webSearch",
        },
      ],
    },
    {
      title: "Safety",
      description: "Review policy and safeguards for cybersecurity tasks.",
      pages: [
        {
          title: "Cyber safety",
          description:
            "Understand how Codex handles security-sensitive requests.",
          href: "/codex/cyber-safety",
          icon: "userLock",
        },
      ],
    },
  ]}
/>