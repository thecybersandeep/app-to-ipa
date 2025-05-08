# app-to-ipa

A  guide to convert an iOS `.app` bundle into a portable `.ipa` file for sideloading via TrollStore.

Thought for a couple of seconds


If you want an .ipa for easier distribution or sideloading, here’s a generic wrap:

---

### 1. Create the Payload structure

```bash
mkdir -p Payload
cp -R "YourApp.app" Payload/
```

### 2. Zip and rename

```bash
zip -r YourApp.ipa Payload
mv YourApp.zip YourApp.ipa 
```

### 3. Install via TrollStore

1. Transfer `YourApp.ipa` to your iPhone (AirDrop, iCloud, etc.).
2. Open **TrollStore**, tap **Install IPA**, select `YourApp.ipa`, then confirm.

No respring needed—your app will show up on the Home screen right away.
