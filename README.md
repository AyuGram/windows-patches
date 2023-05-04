# AyuGram

![AyuGram Logo](.github/AyuGram.png)

This repo contains patches for the [64Gram](https://github.com/TDesktop-x64/tdesktop) - unofficial Telegram Desktop
fork.

## Features

**AyuGram** is built on top of 64Gram, which means we have all the features 64Gram has and some of ours:

- Disable read packets sending
- Disable online packets sending
- Disable typing & upload packets sending
- Offline packet autosending
- Messages history (+ deleted ones)
- Using scheduled messages to keep offline

Technically, we have the **Ghost mode** starter pack.

Also, we have cool **purple icon** and **custom day/night themes**.

## Downloads?

We have both **Windows** *(by me)* and **Linux** *(by my friend)* builds.

Follow our [Telegram channel](https://t.me/ayugram1338).

## May I get banned?

Well, *you* **can't**, because you're just an ordinary user.

But *me* - well, if I ever get a letter from a Telegram team and don't comply with ToS - **yes**. But that would be a
different story.

## Why patches? Why not the full source code?

It's very hard to merge changes for me as a person who mains C# and Python, even with the help of CLion's magic wand.

It's easier for me to maintain a set of patches—that way, if some of them fail to apply, others still will work.

Also, that way you can apply these patches to other tdesktop forks
(e.g. [Forkgram](https://github.com/forkgram/tdesktop)), with a bit of changes.

## Localization?

I don't have enough knowledge in C++, so if you're willing to localize settings, please make a PR!

## How to contribute

To set up dev environment, see `How to apply patches` section at the bottom.

## How to build

Follow [official guide](https://github.com/TDesktop-x64/tdesktop/blob/dev/docs/building-win-x64.md).

### Remarks

1. You have to clone 64Gram (`https://github.com/TDesktop-x64/tdesktop.git`), not official tdesktop.

2. Make sure you have these components installed with VS Build Tools:
    - C++ MFC latest (x86 & x64)
    - C++ ATL latest (x86 & x64)
    - latest Windows 11 SDK

### How to apply patches

IDK if there's any other way to apply IDEA patches with changelist saving, but that's how I'm doing it:

- Download CLion
- Open `out/CMakeCache.txt` as a project
- Wait for it to load
- For each patch, use `Git` -> `Patch` -> `Apply patch` and set changelist name like patch name

To build, edit CMake profile to `Release` and hit build button.