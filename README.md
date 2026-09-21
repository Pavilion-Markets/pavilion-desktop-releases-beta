# HarnessHQ downloads: beta channel

Prerelease installers of HarnessHQ, and the `latest.json` an installed copy on the beta channel
polls to update itself. Every stable release is published here too, so a copy on this channel is
never behind stable. Nothing else lives here. The app's source is in a private repository, and the
stable channel is [pavilion-desktop-releases](https://github.com/Pavilion-Markets/pavilion-desktop-releases).

**Who is on this channel:** an install whose signed-in account carries the `beta-channel` flag. The
app reads that flag from the hub at sign-in and polls this repository instead of the stable one;
there is nothing to install or configure on the machine, and the same build serves both channels.

**Install once:** open the newest release under Releases and run `HarnessHQ_<version>_x64-setup.exe`.
Windows SmartScreen says unrecognised app; choose More info, then Run anyway. The installer is not
code-signed with a Microsoft certificate; it is signed with Pavilion's own update key, which the
app checks before applying any update, from either channel.

**After that** the app updates itself: it checks here when it starts and every six hours, and
offers the new version as a card. Settings > About has Check for updates and says which channel the
install is on. The app never goes back to an older version: an install on a beta stays there until
a stable release is newer.
