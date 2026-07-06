# Privacy Policy for ErrorToPrompt

Last updated: July 6, 2026

ErrorToPrompt is a Chrome browser extension that generates AI-ready debugging prompts from user-selected text. This privacy policy explains what data the extension accesses and how it is handled.

## Data Collection
ErrorToPrompt does not collect, transmit, or store any personal data. The extension does not make any network requests. All processing happens locally in your browser.

## Data Accessed
When you use ErrorToPrompt (via right-click menu, keyboard shortcut, or the popup paste box), the extension temporarily accesses:
- The text you have selected on the current page
- The page title of the active tab (if enabled in settings)
- The URL of the active tab (if enabled in settings)

This data is used solely to generate a debugging prompt, which is copied to your clipboard. The selected text, page title, and URL are not stored unless you explicitly enable the "Store Last Prompt for Copy Again" setting, in which case only the last generated prompt is stored locally in your browser.

## Data Storage
ErrorToPrompt stores the following data locally in your browser using Chrome's `chrome.storage.local` API:
- Your extension settings (prompt style, detection sensitivity, context toggles, menu preferences)
- A summary of the last classification result (category, confidence scores, matched signal labels — no raw text)
- The full last generated prompt text (only if you explicitly enable "Store Last Prompt for Copy Again")

All stored data remains in your browser. No data is transmitted to any server, API, or third party.

## Network Requests
ErrorToPrompt makes zero network requests. It does not connect to any server, API, or external service. It does not load external resources, fonts, or scripts.

## Third-Party Services
ErrorToPrompt does not integrate with any third-party service. It does not use analytics, telemetry, crash reporting, or advertising services.

## Permissions
The extension requests the following Chrome permissions:
- `contextMenus`: Creates the right-click menu item
- `activeTab`: Reads selected text from the active tab on user gesture
- `scripting`: Injects a script to retrieve text selection
- `storage`: Stores settings locally
- `offscreen`: Copies prompts to clipboard from background context

## Data Deletion
You can clear all stored data at any time:
- Click "Clear Last Result" in the extension settings page
- Click "Reset to Defaults" to restore all settings
- Uninstalling the extension removes all stored data

## Contact
For questions, support, or bug reports, please open an issue at:
https://github.com/nukabo/error-to-prompt-public/issues
