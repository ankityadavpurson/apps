# App releases

Public home for the installable builds of apps whose source lives in private
repositories. A public repo's release assets can be downloaded by anyone without
a token, which is what lets each app's site link straight to its latest build.

**There is no source code here, and nothing is committed by hand.** Every release
on this repo is uploaded by the release workflow of the app it belongs to.

## What's published

| App | Build | Site |
| --- | ----- | ---- |
| Passwords | Android APK, 7.0 and up (`arm64-v8a`, `armeabi-v7a`) | [passwords-mobile.web.app](https://passwords-mobile.web.app) |

## Download

**Passwords, latest build:**

```
https://github.com/ankityadavpurson/apps/releases/download/passwords-latest/passwords.apk
```

That link always serves the newest build, so it is safe to bookmark or share.
For a specific version, pick it from the
[releases page](https://github.com/ankityadavpurson/apps/releases).

## How releases are named

Every app prefixes its tags with its own name, so several apps can share this
repo without colliding. Each release of an app publishes two tags:

| Tag | Asset | What it is |
| --- | ----- | ---------- |
| `passwords-v1.3.5` | `passwords-1.3.5.apk` | one tag per version, kept as the archive — the filename says which version you saved |
| `passwords-latest` | `passwords.apk` | a rolling pointer, replaced on every release |

> **GitHub's own "Latest release" badge does not mean much here.** It picks the
> newest release across the whole repo, whichever app that happens to be. Use
> the `<app>-latest` tag to get the current build of a particular app.

## Installing an APK

1. Download the file on the phone.
2. Open it. Android will ask once whether to allow installs from whichever app
   you downloaded it with — your browser or file manager.
3. Install as usual. That permission can be withdrawn again afterwards under
   **Settings → Apps → Special access**.

Builds published here are signed with a stable release key. Android refuses to
install a build signed with a different key over an existing one, so if you
previously installed a debug or development build, uninstall it first.

## Notes

- Only release builds reach this repo. Debug and development builds are signed
  with a shared debug key and are never published here.
- This repo stores files; it is not an issue tracker or a place for pull
  requests.
