# Install & get started

[简体中文](INSTALL.md) | **English**

[English website](https://tickerval.com/apps/yuan/) · [Chinese website](https://tickerval.com/zh-cn/apps/yuan/)

[About Yuan](README.en.md) · [Download v0.5.2 DMG](https://github.com/JavaApes/yuan/releases/download/v0.5.2/Yuan-0.5.2-macOS-AppleSilicon.dmg) · [Changelog](CHANGELOG.en.md)

## Requirements

- An Apple Silicon Mac (M-series chip) running macOS 13 or later.
- Your own model-provider API key and an internet connection for AI conversations and web research.
- This package does not support Intel Macs, Windows, iOS or Android.

Yuan is free to download and use. Model and other third-party service charges, if any, are billed by their providers. No shared API keys or model credits are included.

## Download and install

1. Download [Yuan-0.5.2-macOS-AppleSilicon.dmg](https://github.com/JavaApes/yuan/releases/download/v0.5.2/Yuan-0.5.2-macOS-AppleSilicon.dmg) from the [v0.5.2 release](https://github.com/JavaApes/yuan/releases/tag/v0.5.2).
2. Open the DMG and drag `Yuan.app` into `Applications`.
3. Eject the installation disk.
4. Open Yuan from Applications.

You do not need to install Node.js, Electron or developer tools separately. GitHub's automatic **Source code (zip/tar.gz)** archives contain public documentation, not the app. Download the **DMG** to install Yuan.

## First launch and macOS security

The v0.5.2 package uses an **ad-hoc local signature**. It contains **no Developer ID certificate** and is **not notarized by Apple**.

If macOS says it cannot verify the developer, first confirm that the file came from this repository's release. After attempting to open Yuan, go to **System Settings → Privacy & Security**, find the message about the blocked app, and choose **Open Anyway** if you decide to proceed. Organization-managed Macs may prohibit this.

If macOS explicitly reports malware, the file appears damaged, or the checksum does not match, stop and report the issue. Do not disable system-wide security protections or run bypass commands from unknown sources.

See [Apple's official guidance](https://support.apple.com/en-us/102445).

## Select English and configure your model

1. Open **Agent settings → Interface language** and select **English**. If Yuan initially opens in Chinese, look for **Agent 设置 → 界面语言 / Language**.
2. The interface language changes immediately and persists after restarting. Existing documents, notes and conversations keep their original language.
3. In Agent settings, open the model settings, choose your provider and enter your own API key. In the Chinese interface this section is **模型与思考**.
4. Enable the models you want to use and choose the model and reasoning level for your conversation.

For OpenAI web research, use your own OpenAI key. External MCP tools, market-data services and other integrations require their own configuration and authorization; some connectors may need an additional runtime. Installing Yuan does not create service accounts or grant access to them.

## Start your first session

Create a new conversation and ask a specific question, for example:

> Explain the difference between earnings and cash flow using a small shop. Ask me one question to check my understanding.

You can also import your own documents, ask about a passage and save notes for later. Ask in English or explicitly request English replies. The interface language is the fallback when your language preference is unclear.

For company research, start with a company, a filing or a question. Check cited sources and distinguish facts from assumptions before drawing a conclusion.

Scheduled follow-ups need Yuan running, your Mac awake and the required services available. Closing the app or putting the Mac to sleep can miss a run; confirm a catch-up after returning.

## Data, upgrades and uninstalling

Local data is stored at:

```text
~/Library/Application Support/zhiben-desktop/
```

To upgrade, quit Yuan and replace `Yuan.app` in Applications. Keep the data directory to retain your documents and conversations. Removing the app does not automatically delete personal data.

Share the DMG or release link, not your personal data directory. API-key encryption is tied to the Mac's system secure storage; copying the data directory is not a key-migration method.

AI requests send the relevant conversation and material to your chosen model provider. Web research and external integrations contact their respective services. See [Data and privacy](README.en.md#data-and-privacy).

## Verify the download

Download both the DMG and its [SHA-256 file](https://github.com/JavaApes/yuan/releases/download/v0.5.2/Yuan-0.5.2-macOS-AppleSilicon.dmg.sha256) into the same folder. In Terminal, open that folder and run:

```sh
shasum -a 256 -c Yuan-0.5.2-macOS-AppleSilicon.dmg.sha256
```

Expected DMG SHA-256:

```text
660f9d8fadf4748c082edd40c4badc532befdd6058d36e1d5b3d74d785dda97e
```

An `OK` result confirms that the file matches the published checksum. It is not Apple notarization or a security audit.

## Validation scope

The release was checked on the developer's Apple Silicon Mac: mounting the image, copying the app, launching after ejecting the image, starting with fresh user data and restarting. Other devices and all external services still require real-world verification.

## Feedback

Use [GitHub Issues](https://github.com/JavaApes/yuan/issues) or email [haokami6688@buttondown.email](mailto:haokami6688@buttondown.email). Include your app version, macOS version, chip, reproduction steps and redacted screenshots. Do not send API keys, account credentials or unredacted financial information.
