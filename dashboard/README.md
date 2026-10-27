# TradingAgents Dashboard 1.2 — model selection and execution diagnostics

Open TradingAgents-Dashboard.zip and click Download raw file to download the Windows/macOS/Linux package.

## Upgrade on Windows

1. Stop the previous dashboard by closing its command window.
2. Download and extract this ZIP into a new folder.
3. To keep your existing key, settings and reports, copy the old folder's .data directory into the new extracted folder while both versions are stopped. Do not copy old backend/frontend or .venv directories over the update. Windows DPAPI keys remain bound to your Windows account.
4. Open Start Dashboard.bat. In Connections & settings, refresh the model list and choose Use recommended models, or select account-listed Sol/Astra models if available.
5. Optionally click Test AI execution (API charges apply). This explicitly performs up to two bounded model requests; it is distinct from the free model-list test.
6. Run AI analysis. If the provider blocks execution, the failed report now shows a safe code, action and diagnostic download instead of a generic failure.

## Changes

- Exact account-returned model choices replace fixed old defaults. Sol/Astra are preferred when actually listed; no model access is invented and known embeddings/audio/images are excluded.
- Expired model discovery refreshes during startup of an analysis. The UI explains missing or invalid selections instead of silently blocking a configured account.
- A free readiness check and separate optional billed tool-call/structured-output execution probe diagnose API billing, permissions and model compatibility.
- Reasoning output budget increased; requests and total analysis are bounded. Safe error codes distinguish quota, rate limit, authentication, model/parameter/output issues, timeouts and worker crashes.
- Failed runs support explicit retry and safe diagnostic copy/download. Real analyst tool callbacks improve data-coverage observations without storing tool bodies or secrets.

The user reported that model-list testing succeeded but analysis failed. The older worker discarded its underlying exception, so the original cause is still unconfirmed. A model's age alone does not explain an API failure. The execution test on the user's machine can reveal actual generation quota or access problems. API billing is separate from a ChatGPT subscription.

## Verification

165 backend tests, integrated browser smoke, desktop/mobile model UI checks, a production build and fresh Linux ZIP installation passed. The actual installed Sol/Astra adapters also serialized and parsed native Responses API fixture requests through a local HTTP mock. No actual paid model calls were made here; account access, billing and provider availability still require the user's local execution test.

See WINDOWS-START-HERE.md, TROUBLESHOOTING.md and VALIDATION.md inside the ZIP. Real market data remains the default, with source/session timestamps; Demo examples remain explicitly synthetic. The app does not execute broker orders. No secret or personal .data directory is included in the package.
