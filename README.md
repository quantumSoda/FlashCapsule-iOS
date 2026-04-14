# 🧠 FlashCapsule: Zero-Friction Cognitive Offloader

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![iOS: 16+](https://img.shields.io/badge/iOS-16%2B-blue.svg)]()
[![Privacy: Local First](https://img.shields.io/badge/Privacy-Local_First-success.svg)]()

*A hardware-triggered, local-first thought capture system designed to minimize cognitive load and protect psychological bandwidth.*

## ⚡ The Philosophy

Human working memory is highly volatile. Every second spent unlocking a device, locating an app, and manually typing introduces **cognitive friction** that degrades the original thought. 

FlashCapsule bypasses this completely. By mapping a complex automation workflow to a physical hardware trigger (iPhone Back Tap), it transforms the device into an instant extension of your brain. Thoughts are captured, transcribed locally, and archived securely with zero conscious effort.

## 🏗 System Architecture

The system operates entirely on-device, ensuring zero network latency and absolute privacy.

`Physical Back Tap` ➔ `Microphone Capture` ➔ `Local Whisper Decoding (Aiko)` ➔ `Data Assembly` ➔ `Apple Notes Integration`

1. **Existence Validation:** The script checks for today's designated "Capsule" note. If it doesn't exist, it instantiates one.
2. **Audio Capture:** Instantly records the user's voice memo.
3. **Dimensionality Reduction:** Passes the audio payload to the Aiko engine (powered by OpenAI's Whisper model running locally).
4. **Data Assembly:** Formats the transcribed text with an exact timestamp and appends both the text and the original audio file to the daily Capsule note.

## ⚙️ Prerequisites

To deploy this system, your environment must have:
* **iOS 16** or later.
* **Apple Notes** (Native app).
* **[Aiko](https://apps.apple.com/us/app/aiko/id1672085276)** (A free, high-quality local Whisper transcription app by Sindre Sorhus).

## 🚀 Deployment Guide

### Step 1: Initialize Storage
Open your Apple Notes app and create a new folder named exactly: `闪记胶囊` (or modify the Shortcut to match your preferred folder name).

### Step 2: Install the Logic Core
Download and install the pre-compiled iOS Shortcut:
👉 **[INSERT YOUR ICLOUD SHORTCUT LINK HERE]**

### Step 3: Hardware Mapping (The Magic)
Bind the software logic to the physical hardware:
1. Go to **Settings** > **Accessibility** > **Touch**.
2. Scroll down to **Back Tap**.
3. Select **Double Tap** (or Triple Tap).
4. Scroll to the bottom *Shortcuts* section and select **FlashCapsule** (or whatever you named the downloaded shortcut).

## 🔮 Future Roadmap

- [ ] Automatic extraction of actionable tasks (TODOs) from the transcript.
- [ ] Daily summary generation via LLM API integration.
- [ ] Auto-syncing capabilities to Obsidian/Notion via webhooks.

## 🛡 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details. Let's optimize human biological efficiency together.
