# Telegram Text and Voice AI Agent

An n8n Telegram agent that handles text and voice messages in one workflow. Voice messages are downloaded and transcribed, then both input types are passed into the same AI conversation flow.

## Flow

`Telegram → Text/voice routing → Transcription when needed → AI Agent → Memory → Telegram response`

## Included

- Text and voice input routing
- Audio download and transcription path
- OpenAI-powered AI Agent
- Conversation memory
- Telegram response delivery

## Setup

Import `workflow.json` into n8n and connect your own Telegram, OpenAI, and transcription credentials. Configure the bot token, memory settings, and response behavior before activation.

This is a demo workflow and contains no credentials or client data.
