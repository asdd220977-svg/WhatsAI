# WhatsAI

Summarize an exported WhatsApp chat into main points, decisions and dates, and transcribe and summarize its voice notes, each with its source.

## What it does

- Summarizes a WhatsApp export (text file or zip with media) into main points.
- Extracts decisions with the person and date, and important dates with their source message.
- Transcribes selected voice notes locally with Whisper and summarizes each one in points, marking what is confirmed, partly confirmed or unclear.
- Gives every point a verbatim quote with its date, time and sender, so the source can be found again in the export file.

## How to get the export file

Muse cannot read WhatsApp chats or groups directly and cannot join a group.

- Export the chat from WhatsApp (Export Chat) and upload the text file or zip in the chat.
- Or send the export file in the WhatsApp chat with Muse.
- Or place the export file in Google Drive and share its name.

## Files

- `SKILL.md` — the skill instructions.
- `skill.yaml` — the skill metadata.

## Notes

- Numbers in a chat are what members said, not verified facts outside the chat. Check them before using them.
- Local Whisper transcription of Egyptian dialect gives the general meaning but stays unreliable for names and numbers. Review unclear parts before using them.
