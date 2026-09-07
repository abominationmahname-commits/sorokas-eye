# Soroka's Eye

A portable viewer for The Legend of Neverland's local data files: browse them as
tables, search across every file at once, translate Chinese labels and cell text,
see item names and icons in place of raw id numbers, and compare a folder against
an earlier snapshot to see what a patch changed.

Everything runs on your own machine, against your own installed client. Nothing
is uploaded.

## Install

Download `SorokasEye.exe` from the latest release and run it. That is the whole
install: one file, no setup, no Node, no admin rights. It opens in your browser
and prints a local address; the console window it starts from is the app, so
closing that window stops it.

It is portable — a USB stick is fine. Settings, caches and snapshots are written
to a `data` folder created beside the executable.

Windows SmartScreen will warn about an unsigned executable the first time.

## Updates

**Settings > Updates > Check now**, or the badge that appears in the top right
when a new version is published.

Where a small patch fits your build it downloads about 50 KB instead of the whole
55 MB program. Either way the download is checked against the checksum published
with the release before anything on disk is replaced, the app restarts itself,
and the page reloads on its own. **Undo last update** puts back the version built
into the executable, and a patch that fails to start is switched off
automatically the next time the app runs.

## Releases

Each release carries three files:

| file | what it is |
|---|---|
| `SorokasEye.exe` | the whole program |
| `patch-<version>.json.gz` | the same version as a small patch, for anyone already on the matching build |
| `update.json` | the feed the app reads, with a SHA-256 for each of the above |
