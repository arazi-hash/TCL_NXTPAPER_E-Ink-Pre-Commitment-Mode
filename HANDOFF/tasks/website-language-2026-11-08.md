# Open the landing page in the app language

8 November 2026, Bahrain. The founder asked to identify the installed TCL
version and open the English or Arabic website from the matching app interface.
Read-only Android inspection found beta.2/code 8 installed in the owner profile,
English app locale, `QUALIFIED` setup and a stopped controller. The installed
APK matched the earlier private acceptance copy. Keep the existing setup and phone
state. Published beta.2 and its store metadata remain the release baseline.

The website button currently opens the bare host. The canonical landing page
accepts `?lang=en` and `?lang=ar`, which override saved and browser language
preferences. Add the current app locale to the website link and prepare a local
beta.3/code 9 candidate so the fix can be installed as an update.

## Completed checks

- The button now derives the website query from the app locale on tap. The live
  site selected the requested language over opposite saved and browser settings.
  Landing preference tests passed 40/40.
- Android tests passed 56/56. Release lint had zero errors and 18 existing
  warnings. The signed beta.3 release APK passed package, version, signature and
  asset verification. Native controller and compatibility bytes match beta.2.
- Public-key candidate under `dist/website-language-1.0.6-beta.3/` has SHA256
  `50421cf15038bcdfd4c42b1742f921c7ecd8b954ecad6eb57c3f37d01a30e294`.
- The handset-compatible private candidate is
  `dist/private-acceptance/1.0.6-beta.3-website-language-private-test.apk`, SHA256
  `4fc846cb64cc2aa3eb67c9cfeed34121d46f5a943244e8bd2c9f4e28d64505ca`. Its payload
  matches the public-key candidate and its signer matches the installed beta.2.

The handset remains on beta.2. A real beta.3 website-button tap awaits a handset
test.

## Publication requested

The founder asked to push beta.3 for the CoreFetch crawler. Publish the signed
public-key APK and its checksum and release notes on the new tag, verify the
anonymous download, then fast-forward the default branch with beta.3 metadata.
Reuse the existing beta.2 images because the website destination is the only
visible-flow change. Preserve the founder's store and GitHub descriptions.
Handset beta.3 installation and link-tap acceptance remain separate.

## Publication result

GitHub prerelease `v1.0.6-beta.3` and default branch `codex/nxtpaper-demo`
are both live at commit `82888aa51f2d2febb85589e186e3e28ca87c3abc`.
The signed APK, checksum and notes matched through GitHub's anonymous release
asset API. The direct GitHub download route returned intermittent HTTP 504
during verification. The published manifest links the canonical release APK.
The app identity, repository About, and all store descriptions were preserved.
Existing beta.2 images are tagged byte-for-byte as beta.3 because the website
destination is the only change to the user flow.

GitHub Actions run `42471030329` started verifying beta.3. The live CoreFetch
catalog still showed beta.1 at the end of publication. Store indexing remains
pending. The handset was not modified, and only the public-key APK was uploaded.
