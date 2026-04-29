# Restart Finder and Refresh Preview Caches

If Universal 3D Previewer is installed but Finder still shows old previews, blank thumbnails, or no Quick Look preview, macOS may be using cached preview data.

Try these steps in order.

## Step 1: Restart Finder

1. Open **Terminal**.
   - You can find Terminal in **Applications > Utilities > Terminal**.
   - You can also press **Command + Space**, type **Terminal**, and press **Return**.
2. Copy and paste this command:

```sh
killall Finder
```

3. Press **Return**.

Finder will close and reopen automatically. Check your file preview again.

## Step 2: Refresh Quick Look's Cache

If restarting Finder did not help, run these commands in Terminal:

```sh
qlmanage -r
qlmanage -r cache
killall QuickLookUIService 2>/dev/null || true
killall Finder
```

After the commands finish, try the Finder preview again.

## Step 3: Reboot Your Mac

If Finder still shows stale previews, restart your Mac. macOS can keep old Quick Look extension processes alive longer than expected.

## Still Need Help?

Go back to the main help page:

[Universal 3D Previewer Help](README.md)

To report a bug or request a feature, open a public issue:

[Open an issue](https://github.com/bj97301/universal-3d-previewer-app/issues/new)
