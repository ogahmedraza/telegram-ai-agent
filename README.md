# Telegram Text & Voice AI Agent

> One n8n Telegram agent for both typed messages and voice notes, with transcription only when it is needed.

## What makes this workflow different

Text and voice are handled as two input paths that converge into one AI conversation flow. A text message can go directly to the agent. A voice message is downloaded, transcribed, and then sent through the same response logic.

## Workflow map

```text
Telegram update
  ├─ text message ────────────────────────┐
  └─ voice note → download → transcription ┤
                                           ↓
                                  AI agent + memory
                                           ↓
                                  Telegram response
```

## Included behaviour

- Telegram text-message handling
- Voice-note routing and transcription path
- Shared AI response flow after input normalization
- Conversation-memory support
- Response delivery back to the originating Telegram chat

## Setup checklist

1. Import `workflow.json` into n8n.
2. Connect a Telegram bot and your AI/transcription provider credentials.
3. Set chat-access rules before exposing the bot publicly.
4. Decide the memory scope and retention period.
5. Test text, short voice, invalid audio, and long-audio cases.
6. Review response limits and error handling before activation.

## Practical limits

- Speech quality and language support depend on your transcription provider and source audio.
- Memory should not be used as a substitute for a customer-data policy.
- Add authentication, allowlists, rate limits, and escalation rules for a public-facing bot.
- This is a sanitized workflow template, not a hosted service or a claim of production deployment.

## Repository contents

| File | Purpose |
| --- | --- |
| `workflow.json` | Importable n8n agent workflow |
| `SECURITY.md` | Bot-token and data-handling guidance |
| `LICENSE` | MIT license |

## License

MIT — see [LICENSE](LICENSE).