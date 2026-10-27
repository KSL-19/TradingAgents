# Download the TradingAgents dashboard

This branch contains a portable Windows/macOS/Linux dashboard package built around the unmodified official TradingAgents 0.7.1 source.

1. Open `TradingAgents-Dashboard.zip` in this folder on GitHub.
2. Click **Download raw file** (the down-arrow download button).
3. On Windows, open Downloads, right-click the ZIP, select **Extract All**, then **Extract**.
4. Open the extracted folder and double-click `Start Dashboard.bat`. Python 3.12 must be installed first.

The package contains a setup guide, full dashboard source, prebuilt frontend, and the upstream wheel with its license and checksum. First launch needs Internet access to install Python dependencies.

Demo mode uses synthetic prices and illustrative reports. OpenAI analysis needs your own API key. All orders are paper simulations; no broker orders are placed.

Validation:26backendtests passed, browser desktop/mobile workflows passed, and a fresh Linux ZIP installation passed. Windows/macOS launchers are included but were not executed in the Linux build environment.
