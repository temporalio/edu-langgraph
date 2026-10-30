# edu-langgraph

The **LangGraph** example for the Temporal Cloud Quickstart Guide. Like
[`edu-standalone-activities`](https://github.com/temporalio/edu-standalone-activities),
it holds one example with a self-contained quickstart per SDK:

| SDK | Directory |
|---|---|
| Python | [`python/quickstart`](python/quickstart) |

The LangGraph plugin sample exists only in the Python samples today, so Python
is the only SDK here.

## Quickstart contract

Every `{sdk}/quickstart` directory:

- connects only through environment configuration (`TEMPORAL_PROFILE` + TOML),
  with no hardcoded address;
- reads `TEMPORAL_TASK_QUEUE`, falling back to a sample-specific default;
- uses a unique Workflow ID per run;
- has a Worker and a client, and the client waits for the result and prints a
  stable success line;
- completes in well under a minute, with no external infrastructure or API keys.
