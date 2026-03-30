# Privacy Policy for Lnr

Last updated: March 25, 2026

Artem Bear ("we", "our", or "us") is committed to protecting your privacy. This Privacy Policy explains how the Lnr plugin ("the Plugin") for JetBrains IDEs handles information when you use it.

## 1. Information Collection and Use

### 1.1 Local Storage
The Plugin is designed to work as a local tool within your IDE. It stores specific configuration and data locally on your device:
- **Linear API Key**: Encrypted and stored securely in your system's password manager (using the standard JetBrains `PasswordSafe` API).
- **Issue Templates**: Stored in a local configuration file on your machine (`lnr-templates.xml`).
- **AI API Keys**: If using the OpenAI-compatible provider, your API key is stored securely via `PasswordSafe`.
- **User Preferences**: Your last-selected view mode (Board or List) is stored in the local IDE settings.

### 1.2 AI Integration
If you enable the AI Description Generation feature:
- **JetBrains AI Assistant**: If you select this provider, the Plugin uses the JetBrains AI Assistant API. Your data is handled according to the [JetBrains AI Privacy Policy](https://www.jetbrains.com/legal/docs/privacy/ai-privacy/).
- **OpenAI-compatible (BYOK)**: If you select this provider, the Plugin sends the issue title and any provided context directly to the API endpoint you specify (e.g., `api.openai.com`). We do not intercept or store this data; it goes directly from your machine to the AI provider.

### 1.3 Linear.app Communication
The Plugin communicates directly with the Linear.app GraphQL API. All requests are authenticated using your personal API key. We do not have access to your Linear data, and no data is sent to our own servers.

### 1.4 Licensing and Marketplace
Since the Plugin is a paid product on the JetBrains Marketplace, it uses the standard JetBrains licensing service to verify your subscription or trial status. This process is managed by JetBrains according to the [JetBrains Marketplace Agreement](https://www.jetbrains.com/legal/docs/agreements/marketplace/marketplace-agreement/).

## 2. Third-Party Services
The Plugin depends on the following third-party services:
- **Linear.app** (for issue tracking)
- **JetBrains Marketplace** (for distribution and licensing)
- **AI Providers** (Optional, for AI description generation)

Please refer to their respective privacy policies for how they handle your data.

## 3. Data Retention
We do not collect or store any of your data on our own servers. All data managed by the Plugin is stored locally on your machine or processed by the third-party services you explicitly configure.

## 4. Changes to This Policy
We may update our Privacy Policy from time to time. We will notify you of any changes by posting the new Privacy Policy on this page and updating the "Last updated" date at the top.

## 5. Contact Us
If you have any questions or suggestions about our Privacy Policy, do not hesitate to contact us at:
**Email**: artem.tykhonuk@hotmail.com
**GitHub**: [https://github.com/ArtemTykhonuk/LnrPlugin-Public](https://github.com/ArtemTykhonuk/LnrPlugin-Public)
