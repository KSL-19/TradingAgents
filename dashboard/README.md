# TradingAgents Dashboard 1.1 — real daily/swing research

Open TradingAgents-Dashboard.zip in this folder and click Download raw file (the down-arrow download button).

## Windows update

1. Close the old dashboard command window.
2. Download the ZIP, then right-click it in Downloads and choose Extract All, then Extract. Use a new folder for this upgrade.
3. Open the extracted TradingAgents-Dashboard folder and double-click Start Dashboard.bat. Python 3.12 is required; the helper can ask the Python install manager to install it if missing.
4. The updated app opens in Real market data mode. Charts do not need an OpenAI key. Check Yahoo source, quote time and completed-session date against your broker.
5. Open Connections & settings. Create an OpenAI API key at https://platform.openai.com/api-keys, enable API billing if needed, then enter the key locally and click Save & test connection. Never post a key in chat or GitHub.
6. Run the AI analyst team with verified model IDs. ChatGPT subscriptions do not include API usage. For SEC fundamentals, add your real contact details.

The ZIP includes WINDOWS-START-HERE.md, full setup instructions, source, a prebuilt interface, the unchanged upstream TradingAgents wheel, and validation notes.

## What changed

- Real market data is now the default; prior demo preferences are ignored. Demo examples remain a separate opt-in and are explicitly fictional.
- A completed daily close/session date is separate from a newer regular-session quote and provider timestamp. Quote source, refresh and freshness are visible.
- Local provider setup, model-list connection checks, secret storage, and source-coverage limitations were added. Windows keys use user-scoped DPAPI.
- Real AI runs preflight market access before starting paid model calls. Real quote or source failures do not silently become synthetic output.

This is for research and manual broker execution. There is no trial expiry and no broker-order execution. Optional paper accounts use virtual money. Free Yahoo data may be delayed and is not a guaranteed executable broker feed.

## Validation and remaining setup

88 backend tests, isolated desktop/mobile browser checks, production build and a fresh Linux ZIP installation passed. Provider responses in tests were fixtures. Actual current prices and a paid OpenAI analysis were not verified in the cloud environment because applicable network access and a user key were unavailable. Complete the local price comparison, model-list check and actual research run before relying on real-service readiness. The user's reported NVDA close was not hardcoded. Native Windows DPAPI behavior still needs execution on Windows.

To preserve old reports and practice balances, stop both versions and copy only the old .data folder into the new extracted folder. Do not overwrite new code with old backend/frontend directories or copy the old virtual environment.
