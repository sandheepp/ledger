# Ledger

A private spending tracker for your phone. It reads your bank SMS **on the phone**,
categorises them with the rules in this repo, and shows where the money goes — entirely
offline.

## Privacy, plainly

- Your SMS never leave your phone. There is no server, no account, no analytics.
- This repo only ever sends data **to** the app: `users_rules.json` is the table of bank
  SMS formats and category rules. The app checks it daily so a bank changing its wording
  is fixed for everyone without an app update.
- The rules file is generated with an automated check that fails if anything personal
  would ship.

## Install

Download the newest APK from [Releases](../../releases) and open it on your Android phone
(you'll be asked to allow installing from unknown sources — that's what sideloading is).
Grant SMS access when prompted; the first scan builds your last 35 days.

## My bank isn't read

The app shows "N bank messages couldn't be read" when it meets a format it doesn't know.
Tap it — it opens a share sheet with **masked** samples (all digits removed). Send that to
me and the format gets added to `users_rules.json`; your phone picks it up within a day
and the missed transactions backfill on their own.
