# Privacy Policy for Lnr

**Last Updated: March 25, 2026**

This Privacy Policy describes how the **Lnr** plugin ("the Plugin", "we", "us", or "our") handles your information when you use the Plugin within JetBrains IDEs.

### 1. Information We Collect

The Plugin is designed to operate locally within your IDE and communicates directly with the services you configure. We do not operate any middleman servers and do not collect your data on our own infrastructure.

*   **Authentication Credentials:** To connect to Linear, the Plugin requires a Linear API Key.
*   **Linear Data:** The Plugin fetches data from your Linear workspace (issues, teams, projects, cycles, members, labels, comments) to display it within the IDE.
*   **Issue Templates:** If you use the Issue Templates feature, the configurations you save are stored locally on your machine.
*   **AI Configuration:** If you enable AI features, the Plugin stores your AI provider settings (API keys, endpoints, models).

### 2. How Your Information is Used

We use the collected information solely to provide and improve the functionality of the Plugin:
*   To authenticate your requests to the Linear API.
*   To display and manage your Linear issues, boards, and cycles.
*   To automate Git branch creation and commit message prefixing.
*   To generate issue descriptions using your chosen AI provider.

### 3. Data Storage and Security

*   **Secure Credential Storage:** Sensitive information, such as your Linear API Key and AI API Keys, is stored using the JetBrains [PasswordSafe](https://plugins.jetbrains.com/docs/intellij/persisting-sensitive-data.html) API, which utilizes the native OS keychain (Windows Credential Manager, macOS Keychain, or Linux libsecret).
*   **Local Storage:** Non-sensitive settings (e.g., UI preferences, selected team) and Issue Templates are stored locally in your IDE's configuration directory as XML files.
*   **Encryption:** All communication between the Plugin and the Linear API or AI providers is conducted over encrypted HTTPS connections.

### 4. Third-Party Services

When you use the Plugin, data is exchanged with the following third-party services:

*   **Linear.app:** The Plugin communicates directly with Linear's GraphQL API to fetch and update your workspace data. This is governed by [Linear's Privacy Policy](https://linear.app/privacy).
*   **AI Providers (Optional):** If you opt-in to AI features, the Plugin sends the issue title and any provided context to your chosen provider:
    *   **JetBrains AI Assistant:** Governed by the [JetBrains Privacy Policy](https://www.jetbrains.com/legal/docs/privacy/privacy/).
    *   **OpenAI-compatible Providers:** Governed by the privacy policy of the provider you configure (e.g., OpenAI, Anthropic, etc.).

We do not share your data with any other third parties.

### 5. Tracking and Analytics

The Plugin **does not** include any tracking, telemetry, or analytics software. We do not track your usage patterns, IDE environment, or any other personal behavior.

### 6. Your Rights and Control

*   **Access and Deletion:** You can view all data stored by the Plugin within the IDE settings. You can delete your API keys and local data at any time by clearing the settings or uninstalling the Plugin.
*   **Opt-out:** AI features are entirely optional and disabled by default.

### 7. Changes to This Policy

We may update this Privacy Policy from time to time. Any changes will be reflected in the "Last Updated" date at the top of this page and included in the Plugin's changelog.

### 8. Contact Us

If you have any questions or concerns about this Privacy Policy, please contact us at:
*   **Email:** artem.tykhonuk@hotmail.com
*   **GitHub:** [ArtemTykhonuk/LnrPlugin-Public](https://github.com/ArtemTykhonuk/LnrPlugin-Public/issues)
