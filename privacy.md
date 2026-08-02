---
layout: default
title: KlickBox Privacy Policy
---

# KlickBox — Privacy Policy

**Last updated:** 2026-08-02
**Operator:** Mohammad Soltaniehha ("we", "us")
**Contact:** soltaniehha.m@gmail.com

KlickBox is a personal task manager. We designed it to keep your data yours. This policy explains exactly what we collect, what we do with it, and how to delete it.

## Data we collect

| Data | Why | Where it's stored |
|---|---|---|
| Apple ID identifier | To authenticate you with Sign in with Apple and isolate your tasks from other users. | Supabase (US region). |
| Email address (only if you choose to share it via Sign in with Apple) | So we can contact you about your account if needed. | Supabase (US region). |
| Content you create — Tasks (titles, notes, tags, due dates, scores) and Ideas (notes, quotes, links, and the Projects you file them under) | This *is* the product — we cannot show you your tasks and ideas without storing them. | Supabase (US region). |
| Attachments you add to a task, a comment, or an idea (photos, audio recordings you make in the app, PDFs, files) | So your attachments persist across devices. | Supabase Storage (US region). |
| Debrief audio and transcripts (in transit only) | Your own AI agent records spoken Debriefs for you; our Mailbox carries them to your phone. | Supabase Storage (US region), as transport only — deleted once your phone confirms pickup, and swept after 30 days even if never collected. The durable copy lives on **your own iCloud Drive**, not our servers (see below). |
| Voice Replies (in transit only) | Voice notes you record in the app for your own AI agent to collect. | Supabase Storage (US region), as transport only — deleted once your agent confirms pickup, and swept after 30 days even if never collected. |
| API Key (hashed) | To authorize your own AI agent (OpenClaw, Claude Code, Claude Cowork, Codex, or any other agent you deploy) to read and write your tasks. | Supabase (US region). The plaintext key is shown to you once at creation and never stored in plaintext on our servers. We also record when a key was last used and how many requests it has made, so you can spot a key being used without your knowledge and so we can rate-limit it. |

**Reminders / notifications.** KlickBox uses **local notifications only** — the app schedules reminders on your device. We do not collect a push notification token and we do not run a remote push server. If we add server-side push in a future version, we will update this policy first.

## Audio Debriefs and Voice Replies

Your own AI agent can record spoken **Debriefs** for you, and you can answer with recorded **Voice Replies**. Both travel through a server-side **Mailbox** that is transport, never storage:

- **The Mailbox keeps nothing.** Debrief audio and transcripts are deleted from our servers as soon as your phone confirms it has collected them; Voice Replies are deleted as soon as your agent confirms pickup. Anything never collected is swept after 30 days.
- **The durable copy of your Debriefs is yours, not ours.** Once collected, Debrief audio and transcripts are archived to your own iCloud Drive (`KlickBox/Debriefs/`), on your iCloud quota, under Apple's iCloud terms. If iCloud Drive is off, they are kept in the app's private storage on your device instead. Neither copy is on our servers.
- **We never listen to, read, or transcribe your Voice Replies.** A Voice Reply carries audio only. You record it; your own AI agent transcribes and processes it. If your agent uses a third-party speech-to-text service, that is a service you chose and configured — it sits outside KlickBox's data flow and outside this policy.
- **Microphone.** KlickBox requests microphone access to record audio attachments for your tasks and Voice Replies you send to your own agent. Recording happens only when you start it; there is no background or passive listening.

## Data we do NOT collect

- **No analytics.** We do not run Google Analytics, Mixpanel, Amplitude, Firebase Analytics, or any equivalent in KlickBox.
- **No advertising identifiers.** We do not request `IDFA` or `App Tracking Transparency` permission. We do not advertise.
- **No third-party trackers.** No Facebook SDK, no TikTok SDK, no attribution SDKs.
- **No location data.** We do not request or use your location.
- **No contacts, calendar, or photos library scanning.** When you attach a photo, only that photo is uploaded — we do not enumerate your library.
- **No crash reporting that includes personal data.** (If we add crash reporting later, we will update this policy first.)

## Where data is stored

All KlickBox data is stored in **Supabase**, hosted in the **United States**. Supabase encrypts data at rest and in transit. We use Postgres Row-Level Security (RLS) so that every database query is constrained to your user ID at the database level — not just at the application level.

## Who can access it

- **You.** Only you, via the KlickBox app or via your own AI agent authorized with your API Key.
- **Us.** Operator personnel may access database backups for the purpose of resolving an incident you have reported. We do not browse user data.
- **Apple.** Sign in with Apple flows your Apple ID identifier through Apple's servers; their privacy terms apply to that step.
- **No one else.** We do not sell, rent, share, or syndicate your data to any third party.

## How long we keep it

We keep your data until **you** delete it. There is no automatic purge of completed tasks, deferred tasks, or archived attachments. The one exception is the **Mailbox**: Debriefs and Voice Replies in transit are deleted on pickup and swept at 30 days, as described above — that purge protects you, since nothing is meant to persist there. If you delete your account, all data tied to your user ID is removed within **30 days** from primary storage and within **90 days** from encrypted backups.

## Account deletion process

You can delete your account from inside KlickBox: **Settings → Account → Delete Account**. The deletion is processed immediately on the primary database; encrypted backup rotation completes within 90 days. After deletion you cannot recover your data.

If you cannot access the app, email soltaniehha.m@gmail.com from the email tied to your Apple ID and we will process the deletion manually within 7 business days.

## Children

KlickBox is not directed at children under 13. We do not knowingly collect data from children under 13. If you believe we have, contact soltaniehha.m@gmail.com and we will delete it.

## Security

We use industry-standard encryption in transit (TLS 1.2+) and at rest, Postgres RLS for authorization, and short-lived JWTs for app sessions. No system is perfectly secure — if you discover a vulnerability, please email soltaniehha.m@gmail.com.

## Changes to this policy

If we change this policy, we will update the **Last updated** date at the top, and (if the changes are material) notify you in-app on next launch.
