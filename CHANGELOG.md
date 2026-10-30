# Version history

**English** · [简体中文](CHANGELOG.zh-CN.md) · [繁體中文](CHANGELOG.zh-TW.md) · [日本語](CHANGELOG.ja.md) · [한국어](CHANGELOG.ko.md) · [Español](CHANGELOG.es.md) · [Français](CHANGELOG.fr.md)

## Linux 0.1.0 — 2026-10-30

Broomy comes to Linux, as one command for the terminal.
- **Finds** package manager caches (pip, uv, npm, pnpm, Yarn, Bun, Composer, Go, Cargo), Gradle and VS Code caches, old project build folders, thumbnails, app caches, installers in Downloads and on the Desktop, downloaded apt packages, old snap versions, the system journal and packages nothing needs. The Trash and Docker are measured, not touched.
- **Shows before it cleans**: `broomy show` lists every file with its path; `broomy clean --dry-run` says what would happen.
- **Cleans gently**: your files go to the Trash (the file manager can put them back); system items use apt, snap and journalctl themselves, asking for your password through sudo. Caches of running programs, links, other disks and anything git tracks are left alone.
- A single file for x86_64 and ARM, nothing else to install. Seven languages. No network code at all.

## 1.2 — 2026-10-29

- **Move**, a new page: apps you rarely use and big files you haven't opened in a month go to a “Moved by Broomy” folder on an external drive, only after you tick them and confirm. Each one is copied and checked against the original before the original goes to the Trash; an app leaves a link in its old place. If any step fails, nothing is moved. **Move back** brings them home the same way.
- Apps go only to solid-state drives, and when a drive doesn't say whether it's solid-state or a hard disk, you choose. Apps from the App Store or an installer, and apps that run things in the background, stay where they are, with the reason shown.
- An app moved to a drive that isn't attached still counts as installed, so its data is never offered as left behind.
- **Uninstall** sorts by how many days you used each app in the last 90.
- **Note which days you open each app** (Settings, off by default): kept on this Mac for a year, and you can clear it.

## 1.1 — 2026-10-27

- **More to clean up**: Xcode previews; the caches that apps built on web technology (such as VS Code, Slack and Discord) keep in their own folders, skipped while the app is open; Android emulator snapshots; command-line tool caches; data folders of apps that are no longer installed; disk images (.iso, .img) along with installers. The last four start unticked.
- **Empty the Trash** from Clean Up, the Overview or the menu bar. The Finder empties it, only when you click and confirm; nothing else in Broomy deletes anything for good.
- **Calmer pages**: secondary buttons are icons (their names show when you point at them), and each category's description sits behind an ⓘ.
- **Uninstall** can sort apps by how rarely you open them.
- **Photos syncing…** on the Overview shows how to pause iCloud Photos or turn it off on this Mac. Broomy only opens Photos; it never changes the setting itself.
- The menu bar panel's power button closes Broomy's windows and keeps it in the menu bar; right-click the menu bar icon to quit.
- Mail written from About starts its subject with [Broomy].

## 1.0 — 2026-10-21

First release.
- **One page per feature, side by side**: Overview, Clean Up, Uninstall, System, Disk Health and Devices. Swipe with two fingers, click the bar at the top, or press ⌘1…⌘6.
- **Clean Up**: developer leftovers (Xcode, simulators, Gradle, Homebrew, pip, npm, pnpm, Yarn, Bun, CocoaPods, Swift Package Manager, Go, Cargo, and old projects' build folders), app caches and logs, installers in Downloads and on the Desktop, and what deleted apps left behind. Everything goes to the Trash.
- **Uninstall** an app together with its container, caches, settings, saved state, web data and login items.
- **System and Disk Health**: CPU, memory, temperatures and fans; how much the built-in SSD has written and how worn it is.
- **Devices**: brightness and volume of your displays, with a reason and what to try when one can't be adjusted; sound output, a nicer mouse wheel, external drives, USB and Thunderbolt.
- In the menu bar if you like. Nine languages. No network code at all.
