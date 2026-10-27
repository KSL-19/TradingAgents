# When a key connects but analysis fails

Version 1.2 distinguishes three steps:

1. **Connection test:** OpenAI accepts the key and returns model IDs. No model is asked to generate output.
2. **Test AI execution:** your explicit button click makes up to two bounded, billable requests using the selected models: a tool-call check and a structured-output check.
3. **AI analysis:** the actual research workflow uses market tools and the selected models. It has separate API usage and data requirements.

Use **Use recommended models** after refreshing the account model list. Sol/Astra appear only when exact matching IDs are returned by your API account. Changing a model's label or release year cannot supply missing generation credits or project permissions.

| Error code | What to do |
| --- | --- |
| `credential_missing` | Carry over your old `.data` folder or enter your existing API key locally in Connections & settings. |
| `authentication_failed` | Check or replace the API key in your OpenAI project, then save/test it again. |
| `billing_quota_exceeded` | Check API billing, credits and project usage limits. ChatGPT subscription billing is separate. |
| `rate_limited` | Wait before retrying; use fewer analysts or check the model's rate limits. |
| `model_not_available` / `permission_denied` | Refresh the list and choose a model your key can access. The execution test can reveal generation restrictions not established by listing. |
| `unsupported_model_parameter` / `tool_call_unavailable` / `structured_output_unavailable` | Choose a model supporting the analyst's tools or the decision model's structured output, then test execution. |
| `output_limit_exceeded` / `context_limit_exceeded` | Try one analyst and one round, or another supported model. |
| `market_data_unavailable` | Refresh the ticker's real data and verify its source/date before analysis. |
| `provider_connection_failed` / `provider_timeout` | Check Internet/proxy/firewall access and provider availability. |
| `worker_crashed` / `analysis_failed` | Restart and retry a focused run. If it repeats, copy or download the safe diagnostics from the failed report. |

Diagnostics include fixed error codes/actions, stage and selected model IDs. They exclude API keys, raw provider responses, tool contents and authentication headers. Share these diagnostics if you need help; never share the key or raw logs.

The app does not automatically retry a completed failed job or run billable execution checks during startup or key saving. Explicit retries can create new API charges. Expired model-list checks can refresh when you start analysis.
