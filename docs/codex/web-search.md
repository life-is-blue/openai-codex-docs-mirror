# Web search

ChatGPT includes a first-party web search tool. Treat all web results as
untrusted input.



In the ChatGPT desktop app, ask for current information in a task. ChatGPT records
search activity with the other tool calls in the transcript.











## Configure local web search

For local Codex tasks, Codex enables cached search by default. Cached mode uses
an OpenAI-maintained index instead of fetching arbitrary pages live, which
lowers—but doesn't remove—prompt injection risk.

Use live search when your task depends on the latest information. Set
`web_search = "live"` in `config.toml`. Set `web_search = "disabled"` to turn
the tool off. The `"indexed"` mode permits external web access only when the
search index gates the request. When Codex runs with full access, web search
defaults to live results. See [Config basics](https://learn.chatgpt.com/docs/config-file/config-basic)
for config file locations and precedence.





For network boundaries that apply to Codex cloud environments, see [Internet
access](https://learn.chatgpt.com/docs/cloud/internet-access).