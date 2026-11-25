# Changelog

## Missed Call Text-Back v3 (2026-11-24)

Tested against 15 real-world call cases; fixed forwarded-call status, voicemail answer, blocked caller ID, open vs quiet hours; optional emergency line.

- **Forwarded calls now work.** When your Twilio number forwards to your cell with `<Dial>`, Twilio reports the forwarded leg in `DialCallStatus` (while `CallStatus` is `in-progress`). v2 read `CallStatus` first, so these calls were never texted or logged. v3 reads `DialCallStatus` first and falls back to `CallStatus`.
- **Voicemail counts as missed.** If your cell's voicemail picks up a forwarded call (`AnsweredBy` = `machine_*` with Answering Machine Detection), the caller now gets the text. Nothing changes when `AnsweredBy` is absent.
- **Blocked caller ID.** Anonymous / restricted numbers (Twilio sends e.g. `+266696687`) can't receive texts: no text is attempted, and the call is logged with a call-back note.
- **Open hours always win over quiet hours.** If your quiet window overlapped your opening hours (e.g. open at 7, quiet until 8), v2 sent nothing to early callers. Fixed.
- **Optional emergency line.** New Config fields `emergencyLine` (default empty = off) and `emergencyText`. When set, after-hours texts include your on-call number, also during quiet hours.
- The webhook now replies with an empty TwiML `<Response></Response>` (text/xml), so a `<Dial action>` request ends the call cleanly instead of an "application error".
- Not included (paid add-on idea): Twilio Lookup Line Type Intelligence (~$0.008 per call) to skip landline callers, whose texts never arrive.

Upgrade: import the new `missed-call-textback.json`, copy your values from the old **Config** node into the new one (add `emergencyLine` if you want it), connect credentials, then deactivate the old workflow and activate the new one. The Calls sheet is unchanged.

## Missed Call Text-Back v2 (2026-11-21)

- No second text when the same caller redials within `dedupeMinutes`.
- Business hours in your own timezone with an after-hours message; no texts during quiet hours.
