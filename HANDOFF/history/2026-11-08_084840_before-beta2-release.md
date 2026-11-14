# Latest checkpoint — NXTPAPER beta.2 local candidate

Updated 8 November 2026, Bahrain. Local implementation and verification complete. Handset acceptance and publication pending.

The founder approved the tester-experience plan and its implementation while remote with the phone disconnected. Version 1.0.6-beta.2 / code 8 adds clearer EN/AR setup guidance, basic reports without Shizuku, sanitized cached observations, Copy / Share / Open GitHub report form, and updated support documentation. The [detailed task record](tasks/tester-experience-2026-11-07.md) is authoritative for this update.

## Verified results

- 276 Python tests passed in 249.937s and 56 Android tests passed.
- Final test/lint/debug/release build passed in 2m20s. Debug and release lint each have zero errors and 19 pre-existing warnings. An initial lint tool crash cleared in a fresh process; no check was disabled.
- GitHub form parses, EN/AR translatable resources and all string references pass, report layout has scrollable wrapping controls. Actual rendering/enlarged text and phone interactions remain pending because no emulator or handset was available.
- Signed APK version/code/package, public certificate, flags, permissions and bundled assets verified. Native script/adapter bytes equal the existing baseline. Wrong expected APK version is rejected. Published beta.1 metadata separately passes its recorded schema.

## Local deliverables

Folder `dist/tester-experience-1.0.6-beta.2/` contains `E-Ink-Precommitment-Mode-1.0.6-beta.2.apk`, its `.apk.sha256` sidecar, RELEASE_NOTES.md and VERIFICATION.json.

APK size 5,104,547 bytes. SHA256 `417e00fa1421746a2586cbd45633bf399a9614527107a41c96cdf992825a99cc`. Certificate SHA256 `434a6ec4f84e1720f8f05e826fe2ccc0d148c47df73e561eac02d1b6f0845202`.

This is the permanent public signer. The founder's historical phone installation uses a different signer and requires the coordinated procedure in [release instructions](../docs/RELEASE.md). No phone changes or private acceptance APK creation occurred in this task. Published beta.1 and its LIVE catalog remain recorded in tasks/public-beta-2026-11-05.md.

## Working tree and next step

Branch codex/nxtpaper-demo, HEAD 5450f34. Source changes are local, uncommitted and ready for review. Six pre-existing untracked historical handoffs and the new archives are preserved. Root owns all files. No build/test is running. All generated APKs, logs and local tooling are ignored.

When a handset is available, verify EN/AR and enlarged text, report copy/share/browser actions, unavailable/denied/restored Shizuku, cached results and guided-setup presentation. Follow the documented signing procedure while preserving data and any live controller. Record acceptance before publication. For the other PC, source needs a reviewed commit/push and ignored deliverables need explicit transfer.
