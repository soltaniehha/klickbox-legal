---
layout: default
title: KlickBox Privacy Policy
---

# KlickBox — Privacy Policy

**Last updated:** 2026-05-09
**Operator:** Mohammad Soltaniehha ("we", "us")
**Contact:** soltaniehha.m@gmail.com

KlickBox is a personal task manager. We designed it to keep your data yours. This policy explains exactly what we collect, what we do with it, and how to delete it.

## Data we collect

| Data | Why | Where it's stored |
|---|---|---|
| Apple ID identifier | To authenticate you with Sign in with Apple and isolate your tasks from other users. | Supabase (US region). |
| Email address (only if you choose to share it via Sign in with Apple) | So we can contact you about your account if needed. | Supabase (US region). |
| Task content you create (titles, notes, tags, due dates, scores) | This *is* the product — we cannot show you your tasks without storing them. | Supabase (US region). |
| Attachments you add to tasks (photos, audio recordings, PDFs, files) | So your attachments persist across devices. | Supabase Storage (US region). |
| API Key (hashed) | To authorize your own OpenClaw deployment to read and write your tasks. | Supabase (US region). The plaintext key is shown to you once at creation and never stored in plaintext on our servers. |
| Push notification token (only if you enable notifications) | To deliver task reminders and completion celebrations to your device. | Supabase (US region). |

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

- **You.** Only you, via the KlickBox app or via your own OpenClaw deployment authorized with your API Key.
- **Us.** Operator personnel may access database backups for the purpose of resolving an incident you have reported. We do not browse user data.
- **Apple.** Sign in with Apple flows your Apple ID identifier through Apple's servers; their privacy terms apply to that step.
- **No one else.** We do not sell, rent, share, or syndicate your data to any third party.

## How long we keep it

We keep your data until **you** delete it. There is no automatic purge of completed tasks, deferred tasks, or archived attachments. If you delete your account, all data tied to your user ID is removed within **30 days** from primary storage and within **90 days** from encrypted backups.

## Account deletion process

You can delete your account from inside KlickBox: **Settings → Account → Delete Account**. The deletion is processed immediately on the primary database; encrypted backup rotation completes within 90 days. After deletion you cannot recover your data.

If you cannot access the app, email soltaniehha.m@gmail.com from the email tied to your Apple ID and we will process the deletion manually within 7 business days.

## Children

KlickBox is not directed at children under 13. We do not knowingly collect data from children under 13. If you believe we have, contact soltaniehha.m@gmail.com and we will delete it.

## Security

We use industry-standard encryption in transit (TLS 1.2+) and at rest, Postgres RLS for authorization, and short-lived JWTs for app sessions. No system is perfectly secure — if you discover a vulnerability, please email soltaniehha.m@gmail.com.

## Changes to this policy

If we change this policy, we will update the **Last updated** date at the top, and (if the changes are material) notify you in-app on next launch.
