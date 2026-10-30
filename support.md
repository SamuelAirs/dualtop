---
title: Dualtop support
---

# Support

Dualtop turns your iPhone, and especially the foldable iPhone Duo, into a little laptop: its own desktop, plus your PC and Mac a tap away. Here's how to connect each, and what to try when something doesn't work.

## Connect to a computer

Open **Remote** on Dualtop's desktop and choose **Add a computer**.

### Any Windows PC (Home or Pro): Dualtop for Windows

Dualtop's own connection, with smooth video, the PC's sound and game controllers.

1. On the PC, download **Dualtop for Windows** from [github.com/SamuelAirs/dualtop-windows](https://github.com/SamuelAirs/dualtop-windows/releases) and run it. If Windows says "Windows protected your PC", choose **More info**, then **Run anyway**: the installer isn't signed yet.
2. Click Dualtop's icon by the PC's clock and choose **Pair a phone**.
3. On the phone, choose **Dualtop for Windows**, then **Pair with your PC**, and scan the code the PC shows.

### Windows Pro: Remote Desktop

1. On the PC: **Settings > System > Remote Desktop**, turned on.
2. In Remote, choose **Windows PC** and enter the PC's address (for example 192.168.1.20), user name and password.
   - With a Microsoft account, use its email address and its password, not the PIN.
   - If Windows only lets you sign in with Windows Hello, turn off "Only allow Windows Hello sign-in for Microsoft accounts" (Settings > Accounts > Sign-in options).

### A Mac: Screen Sharing

1. On the Mac: **System Settings > General > Sharing > Screen Sharing**, turned on.
2. In Remote, Macs sharing their screens nearby are listed under **Nearby**. Pick yours and sign in with the Mac's own user name and password.

### Linux or a Raspberry Pi: VNC

Turn on its VNC server with a VNC password, then choose **Mac or VNC** in Remote and enter its address. Leave the user name empty.

## Using it

- **Clicking:** tap the trackpad. Right-click: tap with two fingers, or tap its bottom-right corner.
- **Dragging:** tap, then touch again and slide. Or rest a thumb on the bottom of the trackpad and slide another finger.
- **The ••• menu:** Ctrl+Alt+Del, paste from the phone, switching between open computers, the phone's own desktop, and disconnecting.
- **A bigger screen:** plug in a monitor or TV by cable (USB-C, or USB-C to HDMI). The picture moves there and the phone becomes its keyboard and trackpad. Screen Mirroring to an Apple TV shows a copy of the phone instead, because iOS doesn't hand that screen to apps.

## Moving files

**With Dualtop for Windows** (version 0.9.0 or later on the PC):

- **Phone to PC:** while connected, open the **•••** menu and choose **Send a file to the PC…**, then pick the file. The PC asks "Save it?" and puts it in Downloads, or in the folder chosen there.
- **PC to phone:** click Dualtop's icon by the PC's clock and choose **Send a file to the phone…**. It lands in **Files > Downloads** on Dualtop's desktop.

**Over Remote Desktop:**

1. In **Settings > Remote** on Dualtop's desktop, set "Files in Windows over Remote Desktop" to **Read only** or **Read and write**. It starts off.
2. Connect to the PC again.
3. In Windows, open File Explorer. Dualtop's Files folder is in **This PC** as **Dualtop on iPhone**, or at `\\tsclient\Dualtop`.

Copy and paste of text works with every kind of computer. VNC moves text only.

## When something doesn't work

- **"Can't be reached":** the phone and computer must be on the same network, or connected through your VPN. Check that iOS allowed Dualtop on the local network: **Settings > Privacy & Security > Local Network**.
- **Remote Desktop refuses the sign-in:** check the user name and password as above. Remote Desktop needs Windows Pro or higher. On Windows Home, use Dualtop for Windows.
- **"The certificate isn't the one it had before":** Windows renews its Remote Desktop certificate every few months. If that's all it is, edit the computer in Remote and choose **Trust its new certificate**.
- **Anything else:** open **Settings > Diagnostics** on Dualtop's desktop and choose **Copy all**, then send it along with what you tried. It contains connection steps only: no passwords, keys or account names.

## Contact

Open an issue at [github.com/SamuelAirs/dualtop/issues](https://github.com/SamuelAirs/dualtop/issues). Issues are public, so never include a password or anything private. The Diagnostics are fine to paste: they hold connection steps only.

## Privacy

Dualtop collects nothing about you. See the [privacy policy](privacy).
