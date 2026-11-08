Obtainium Link Converter
Turn a GitHub, IzzyOnDroid, or F-Droid source and app details into a shareable, one-tap Obtainium import link.
✨ Features
Quick Paste & Auto-Detect: Paste any supported app URL. The tool automatically detects the source, switches to the correct tab, and fetches the necessary details.
Metadata Fetching: Automatically extracts app names, authors, and package IDs directly from public repository metadata.
Multiple Output Formats: Generate both a standard Shareable HTTPS link and an Obtainium deep link.
100% Local Processing: Runs entirely in your browser. No data you type is uploaded to a server.
🚀 How to Use
Select your source (GitHub, IzzyOnDroid, or F-Droid) or use the Quick Paste feature.
Paste the URL or enter the details manually:
GitHub: Use the repository's main GitHub URL.
IzzyOnDroid: Paste the app's IzzyOnDroid page URL (the package ID is extracted automatically).
F-Droid: Paste the app's F-Droid package URL (e.g., https://f-droid.org/packages/com.example.app/) or just the package ID.
(Optional) Manual Overrides: If needed, you can manually input the Android Package ID, Author, and App display name. (Note: Use the actual Android package ID, not the app's display name).
Generate Links: Click "Generate links" to create your import URLs.
Share: Copy the HTTPS link to share with others, or copy the deep link to open directly in Obtainium.
🔒 Privacy & Security
This tool is designed with privacy in mind:
No Uploads: It runs locally in your browser and does not upload the details you type.
Direct API Lookups:
GitHub: Uses GitHub's official API and raw file host.
IzzyOnDroid: Reads the app's YAML file directly from its public repodata repository (fetching AuthorName and Name/AutoName) without scraping the app page or using third-party CORS proxies.
F-Droid: Reads Name/AutoName and AuthorName directly from F-Droid's fdroiddata metadata (mirrored on GitHub and GitLab).
⚠️ Important Notes
Installation Confirmation: The generated link only imports the source configuration into Obtainium. Obtainium/Android may still prompt you to confirm the actual installation.
Before Updating: Always double-check the Package ID, APK architecture, and signing certificate before updating an existing installation to avoid conflicts or security issues.