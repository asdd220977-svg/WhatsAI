---
name: whatsai
description: Summarize an exported WhatsApp chat into main points, decisions and dates, and transcribe and summarize its voice notes, each with its source.
---

# WhatsAI

## Get the export file

- Ask the user for a WhatsApp export file because Muse cannot read WhatsApp chats or groups directly and cannot join a group.

- Accept the file as an upload in the chat, as a file sent in the WhatsApp chat with Muse, or as a file already in Google Drive and read it read only from Drive.

- Tell the user Muse cannot reach files on their desktop directly and that an upload or a Drive copy is the route in.

- Expect a plain text export or a zip export and open the zip to find the text file plus media files.

- Check the text file first and record its line count, its first and last dates and its message count before you summarize anything.

- Treat a zip as the fuller export because it also holds images, video, contacts and voice notes named PTT and AUD with opus extensions.

## Summarize the text chat

- Read the whole text file in parts and do not summarize from the first few hundred lines alone.

- Group the discussion into eight to twelve main points and keep each point tied to what members actually said.

- Give every point a short verbatim quote with its date, time and sender so the user can find it again by searching the file.

- Explain that there are no web links into a local export file and that the quote with its date and sender is the link to the source.

- Pull decisions into their own list with the person who made each decision and the date it was made.

- Pull important dates into their own list with the event and the message that mentioned it.

- Pull numbers such as prices, advances, order numbers and counts into their own list and keep the source message beside each number.

- Say plainly when numbers disagree in the chat and present them as what members said rather than as verified facts outside the chat.

- Present decisions and dates in tables when the user asks for tables and keep each table row short.

- Build a web page for a long summary when the user asks for links per point and give each point an anchor link to a sources section that holds the verbatim quotes.

## Transcribe and summarize voice notes

- Start with one voice note and confirm the quality before you offer to transcribe many.

- Extract the chosen opus file from the zip and check its duration with ffprobe before you transcribe it.

- Transcribe locally with the bundled helper at /opt/muse/assets/audio/transcribe_chunks.py and the faster-whisper models already set up in the workspace venv.

- Use the small model for Arabic and the tiny model only as a quick check because tiny gives poor results for Egyptian dialect.

- Transcribe in Arabic and keep the language set to Arabic for the whole file.

- Save each transcript beside the audio name in a transcripts folder and keep the tiny and small versions apart when you run both.

- Mark every unclear word, name and number as unclear instead of guessing it.

- Summarize the voice note in points after transcription and mark each point as confirmed, partly confirmed or unclear.

- Use the text messages around the voice note in the chat to help decode unclear places and say when the surrounding context supplied the reading.

- Warn the user that a local small model gives the general meaning but stays unreliable for names and numbers and needs a human check before any number is used.

- Estimate the full job from the sample because transcribing hundreds of voice notes takes hours of compute on a small machine and is best done for selected messages only.

## Present the result

- Answer in the language the user is writing in and keep the reply short when the summary itself lives in a page or file.

- Lead with the main findings and then give the decisions and dates the user asked for.

- Attach the transcript file or the summary page in the same message that says it is ready.

- Say what the export did not contain such as media that was excluded from the export and messages that were deleted in the chat.

- Ask with multiple choice options when the next step is a bounded choice such as transcribing all voice notes, one day only or one message only.

## Available connectors

- [Google Drive](/opt/hatch/connectors/google_drive/CONNECTOR.md) for reading an export file the user placed in Drive.

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.

## Alternatives for better results

- Transcribe selected voice notes by day, sender or topic instead of the whole set when the set is large.

- Use a larger local model or a cloud transcription service when names and numbers must be exact and the small model is not accurate enough.

- Ask the user to correct the unclear words in a transcript when they know what was said because their correction beats another model run.
