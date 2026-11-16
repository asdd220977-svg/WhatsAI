# WhatsAI ⭐

Summarize an exported WhatsApp chat into main points, decisions and dates, and transcribe and summarize its voice notes, each with its source.

لخّص أي شات واتساب مصدّر: النقاط الرئيسية، القرارات، والتواريخ المهمة، مع تفريغ وتلخيص الرسائل الصوتية، وكل نقطة بمصدرها من الشات نفسه.

If you have a long WhatsApp group that nobody can read to the end, this skill turns it into a short summary you can actually use.

## What it does

- Summarizes a WhatsApp export (text file or zip with media) into 8–12 main points.
- Extracts decisions with the person and date, and important dates with their source message.
- Transcribes selected voice notes locally with Whisper and summarizes each one in points, marking what is confirmed, partly confirmed or unclear.
- Gives every point a verbatim quote with its date, time and sender, so the source can be found again in the export file.
- Flags contradictory numbers as member statements, not verified facts.

## Who it is for

- Admins of long WhatsApp groups who need a quick recap.
- Anyone following a big topic in a group: land reservations, housing phases, project updates, family decisions.
- Arabic speakers: it handles Arabic chats and Egyptian dialect voice notes, with the limits of local transcription clearly marked.

## How to get the export file

Muse cannot read WhatsApp chats or groups directly and cannot join a group.

- Export the chat from WhatsApp (Export Chat) and upload the text file or zip in the chat.
- Or send the export file in the WhatsApp chat with Muse.
- Or place the export file in Google Drive and share its name.

## How to use it

1. Clone this repo or copy its files into your Muse custom skills folder as `whatsai`.
2. Send Muse a WhatsApp chat export.
3. Ask for a summary, the decisions, the important dates, or a voice note summary.

## Example

A 5,857-message group about Beit Al-Watan land phase 11 became 10 main points, a decisions list, a timeline of important dates, and a sources section with 30 verbatim quotes.

## Files

- `SKILL.md` — the skill instructions.
- `skill.yaml` — the skill metadata.

## Notes

- Numbers in a chat are what members said, not verified facts outside the chat. Check them before using them.
- Local Whisper transcription of Egyptian dialect gives the general meaning but stays unreliable for names and numbers. Review unclear parts before using them.

## Star it

If this saved you reading thousands of messages, give it a ⭐ — it helps others find it.
