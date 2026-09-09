# FlowStock Testing Channel

Builds in this folder are for manual testing only. The production FlowStock
update checker does not read this folder.

Download the APK referenced by `latest.json` on the test device and open it to
install over the existing FlowStock app. Android may require permission to
install apps from the browser or file manager.

The permanent test download address is represented by `test-download-qr.png`.
Display that image on another screen and scan it with the test device. The QR
code stays the same when a newer test APK replaces `flowstock-test-latest.apk`.

Test builds use the same application ID and signing key, so they update the
existing installation and retain its saved app data. Do not install them on a
live warehouse device until the build has been promoted to production.
