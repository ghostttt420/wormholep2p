# 🌐 NETLINK 95

> **Secure. Serverless. Peer-to-Peer Data Tunnel.**
> *No Clouds. No Logs. Just Physics.*

![License](https://img.shields.io/badge/license-MIT-008080) ![Status](https://img.shields.io/badge/status-operational-00ff00) ![Style](https://img.shields.io/badge/style-retro_95-333)

**NetLink 95** is a lightweight, single-file web application that enables secure, direct file transfer between devices without uploading data to a central server. It uses **WebRTC** technology to create an encrypted pipe directly from Browser A to Browser B.

## 💾 The "Grey Hat" Philosophy
Unlike DropBox or WeTransfer, **NetLink 95** does not store your files.
* **0% Retention:** The file streams from your RAM directly to the recipient's RAM.
* **0% Intermediaries:** Once the connection is established, the server steps aside.
* **100% Ephemeral:** If you close the tab, the data tunnel vanishes forever.

## ⚡ Features

* **Serverless Architecture:** Files never touch a database or cloud bucket.
* **End-to-End Encryption:** Data is encrypted in transit using standard WebRTC protocols.
* **Cross-Device Pairing:**
    * **PC to Mobile:** Instant QR Code pairing.
    * **Mobile to Mobile:** "Copy Link" deep-linking for easy sharing via text/Signal.
* **Local Network Optimization:** If devices are on the same WiFi, data routes locally (LAN) for maximum speed and offline privacy.
* **Retro 95 UI:** A dark-mode, high-contrast aesthetic optimized for readability and nostalgia.

## 🛠️ Tech Stack

* **Frontend:** HTML5, CSS3 (Retro Brutalist Design)
* **Networking:** [PeerJS](https://peerjs.com/) (WebRTC Wrapper)
* **Utilities:** `QRCode.js` (Mobile Pairing)
* **Deployment:** Single-file static site (Vercel/Netlify compatible)

## 🚀 Quick Deployment (Vercel)

This project is designed to be a "Zero Config" deployment.

1.  **Clone the Repo:**
    ```bash
    git clone [https://github.com/YOUR_USERNAME/netlink-95.git](https://github.com/YOUR_USERNAME/netlink-95.git)
    cd netlink-95
    ```

2.  **Deploy:**
    * Push to GitHub.
    * Import the repo to **Vercel**.
    * Hit **Deploy**. (No build settings or environment variables needed).

## 📖 How to Use

### 1. The Host (Sender)
* Open the website on your primary device (PC or Phone).
* Wait for **"WAITING FOR CONNECTION..."** to appear.
* **Option A:** Have the recipient scan the QR Code.
* **Option B:** Click **"COPY"** and send the link to the recipient via a secure messenger.

### 2. The Client (Receiver)
* Open the link (or scan the QR).
* Wait for the status to turn **GREEN** ("SECURE TUNNEL ACTIVE").

### 3. The Transfer
* **Host:** Click the drop zone to select a file (or drag and drop).
* **Client:** Watch the progress bar. The file will automatically download and save when complete.

## ⚠️ Privacy & Limitations

* **Connectivity:** You must have an active internet connection to perform the initial "Handshake" (finding the other peer).
* **Keep Awake:** Because the transfer is P2P (running in your browser's memory), **do not close the tab or lock your phone screen** during a transfer, or the pipe will break.
* **File Size:** Recommended for files under **500MB** due to browser memory limits.

## 📄 License

This project is open-source and available under the **MIT License**. You are free to fork, modify, and distribute it.
# wormholep2p