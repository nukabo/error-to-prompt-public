# ErrorToPrompt

**Turn any error into an AI-ready debugging prompt. One click.**

ErrorToPrompt is a privacy-first Chrome extension that simplifies your AI-assisted debugging workflow. Instead of manually copying raw, messy errors and spending time writing the right prompt context, ErrorToPrompt does the heavy lifting for you. When you select an error, log, or stack trace on any webpage and right-click to copy, the extension instantly constructs a structured, formatted prompt with the appropriate professional role, page context, and targeted debugging instructions, ready to be pasted directly into ChatGPT, Claude, Gemini, or any other AI model.

## Why?

Pasting raw error messages into AI assistants often results in generic, unhelpful responses because the AI lacks critical context. Without proper framing, you waste valuable time writing follow-up questions to explain what technology stack you are using or what the error implies. ErrorToPrompt bridges this gap by automatically enriching the selected error with context-aware metadata and specialized roles before you copy it.

* **Expert Role Allocation:** Automatically assigns a tailored persona (e.g., Database Administrator, DevOps Engineer, Senior React Developer) based on the classified technology stack to ensure specialized answers.
* **Structured Framing:** Encloses the error in clean, safe Markdown code blocks and formats the prompt so the AI immediately understands the core issue and goals.
* **Context-Specific Hints:** Generates target-specific debugging checklist items (such as inspecting specific configuration files, environment variables, or request headers) related to the detected error pattern.

## How It Works

1. Select any error text on any web page
2. Right-click → **Copy AI Debug Prompt**
3. Paste into ChatGPT, Claude, Gemini, Copilot, or any AI assistant

## What It Detects

ErrorToPrompt features a smart signal-weighted classifier with 24 specializations to detect and route errors across various stacks:

* **Languages:** JavaScript, TypeScript, Python, Java, Go, Rust, C#, C++, Ruby, PHP, and more.
* **Frameworks:** React, Next.js, Vite, Django, FastAPI, Spring Boot, Laravel, Ruby on Rails, etc.
* **Infrastructure:** Docker, Kubernetes, Terraform, Git, GitHub Actions, and Azure DevOps Pipelines.
* **Databases:** PostgreSQL, MySQL, MongoDB, Redis, SQLite, and Prisma ORM.
* **Cloud/SaaS:** AWS, Azure, Google Cloud Platform (GCP), Firebase, Supabase, Vercel, Heroku, Netlify, Stripe, Salesforce, and Shopify.
* **Microsoft Ecosystem:** Microsoft Graph API, Dynamics 365 Dataverse WebAPI, Dynamics 365 Business Central, and Power Platform Custom Connectors.
* **Security/Auth:** CORS policy blocks, JWT/OAuth authentication errors, SSL/TLS handshake failures, and Linux file permission issues.

## Prompt Styles

| Style | Description |
|---|---|
| Fast | Shortest useful prompt — role + error |
| Balanced | Role + error + context hints (default) |
| Deep | Hypotheses + missing-context checklist |

## Privacy

* 🔒 **100% Local:** All classification and prompt generation happens entirely within your browser.
* 🔑 **No API Key:** Works out of the box with zero configuration or external accounts.
* 👤 **No Account:** No registration, login, or subscriptions required.
* 🚫 **No Telemetry:** We do not collect, store, or transmit any analytics, logs, or usage statistics.
* 🌐 **No Network Requests:** The extension operates completely offline and never communicates with external servers.
* 🛡️ **Minimal Permissions:** Only requests necessary browser permissions (`contextMenus`, `activeTab`, `scripting`, `storage`, and `offscreen`) with no background network access.
* 📄 **Privacy Policy:** Read our complete [Privacy Policy](PRIVACY_POLICY.md).

## Install

Install ErrorToPrompt from the [Chrome Web Store](https://chrome.google.com/webstore) (link coming soon).

## Keyboard Shortcut

* Windows/Linux: `Ctrl+Shift+E`
* macOS: `Cmd+Shift+E`

## Settings

ErrorToPrompt provides a dedicated settings page allowing you to configure:
* **Default Mode:** Set static prompts for specific technologies or let the extension auto-detect the technology stack using its smart classifier.
* **Prompt Style:** Choose between *Fast*, *Balanced*, or *Deep* depending on the detail level you want.
* **Context Metadata:** Opt-in or opt-out of including the source page title, URL, or execution timestamp.
* **Routing Details:** Configure whether to hide or show the classification confidence percentages and detected specialization in the generated prompt.
* **Last Prompt Storage:** Choose whether the extension stores the last generated prompt text locally for inspector access or keeps it privacy-first (metadata-only).

## Contributing

Contributions are welcome! Please check the [CONTRIBUTING.md](CONTRIBUTING.md) (coming soon) for guidelines on how to submit code changes, bug reports, or feature requests.

## License

MIT
