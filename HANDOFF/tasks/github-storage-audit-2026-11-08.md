# GitHub Actions storage audit

8 November 2026, Bahrain. The founder asked why the NXTPAPER workflow failed and
asked to remove old APK build files from the Android repository.

The NXTPAPER workflow builds no APKs and has zero Actions artifacts. Its first
run hit an HTTP 504 downloading the APK. Run 42467846894 verified beta.2 and its
signer, then timed out waiting for the CoreFetch version and download URL. The
current live catalog still serves beta.1. Storage is unrelated to these failures.

The account shown in the browser owns `arazi-hash/com.analoganchor.app`. That
repository has one temporary testing artifact, ID 13305897013, 131,894,580 bytes,
and 41 APK release assets. The separate `anchorminimalism-del` repository has its
own artifacts. Cleanup targets only the named temporary build from `arazi-hash`.

Downloaded the archive to the ignored local folder
`dist/github-storage-audit-2026-11-08/`. Verified the exact byte count, digest,
ZIP contents and CRCs. Local archive `Analog-Anchor-testing-7635a504-actions.zip`
has SHA256 `e4ceacaacbc25a6d3a059e879384ecfef2a7f22f4f4b6ee9bfd7a7a6b5e1ce3f`.

GitHub confirmed deletion of Actions artifact 13305897013 with HTTP 204. A
fresh artifact listing shows zero remaining in `arazi-hash/com.analoganchor.app`.
Release assets, workflow runs and the separate owner were outside this cleanup.
No push or phone change. The CoreFetch indexing outcome remains external.
