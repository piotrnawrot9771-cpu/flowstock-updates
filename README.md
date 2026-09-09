# FlowStock Updates

This repository is intentionally public and contains only installable FlowStock update files.

It does not contain source code or backend code.

Files:
- `latest.json` - manifest consumed by the app update button
- `downloads/` - APK files published for installation

Update flow:
1. Build a new release APK from the private app repo.
2. Increase `versionCode` and `versionName` in the Android app first.
3. Copy the new APK into `downloads/`.
4. Update `latest.json` to point at the newest APK.
5. Commit and push.

## Testing channel

Experimental builds live under `testing/` and are never referenced by the
production `latest.json`. They can be downloaded and installed manually on a
home test device without offering them to warehouse devices.

- `testing/latest.json` - metadata and download URL for the current test build
- `testing/downloads/` - test APK files

Only promote a tested APK by copying it into the production `downloads/`
directory and deliberately updating the root `latest.json`.
