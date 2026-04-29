# Troubleshooting Universal 3D Previewer

macOS sometimes keeps old Finder previews, thumbnails, or Quick Look extensions cached after installing or updating an app. If previews do not update right away, try the steps below.

## Restart Finder

Restarting Finder is usually the fastest first step.

1. Open **Terminal**.
2. Paste this command and press **Return**:

```sh
killall Finder
```

Finder will close and reopen automatically.

## Refresh the Quick Look Cache

If restarting Finder does not fix stale previews or thumbnails, refresh Quick Look's cache.

1. Open **Terminal**.
2. Paste these commands and press **Return**:

```sh
qlmanage -r
qlmanage -r cache
killall QuickLookUIService 2>/dev/null || true
killall Finder
```

If previews are still stale after that, reboot your Mac once. macOS can keep Quick Look extension processes alive longer than expected.

## Report a Bug or Request a Feature

If Universal 3D Previewer still does not work as expected, please open a public issue:

https://github.com/bj97301/universal-3d-previewer-app/issues/new

For bug reports, include:

- Your macOS version
- The file type you tried to preview, such as STEP, STL, OBJ, PLY, 3MF, or G-code
- What happened and what you expected to happen
- Whether restarting Finder or refreshing the Quick Look cache helped

For feature requests, describe the file type, workflow, or behavior you want supported.
