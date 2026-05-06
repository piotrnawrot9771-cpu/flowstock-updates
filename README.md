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
