# A guide to live stream musical performances from home

This guide is intended for people wanting to live stream a musical performance from home. It provides informations for most kind of setups, from purely acoustic performances to more complex cases implying a DAW, an external sound card with connected instruments and mics.

**It focuses mostly on audio configuration** as it seems to be where most people struggle, although it also includes walkthroughs for all the steps from installing a streaming software to actually start streaming.

## Prerequisites

- Knowing what you want to play and the involved equipment
- Basic knowledge about your DAW (how to access its settings, add a plugin, manage tracks inputs and outputs)
- The streaming platform you are going to use (Twitch, Facebook, Youtube...) and a link to its documentation
- A computer running **Windows** or **macOS**[^1]
- A bit of free time to read this guide carefully

We will use [OBS Studio](https://obsproject.com/) as our streaming software but you are not required to know how to use it.

## How to use this guide?
Simply follow the parts in the correct order! All parts can always be reached through the navigation side bar on the left.

Start by part [a super fast introduction to OBS (part 1)](obs.md) that will help you to install OBS and understand its basis.

You will then make OBS work with your camera in part [2. Video configuration](video.md)

Then come the main point of this guide: audio configuration. You will first follow part [3. Which audio setup do I use?](setup/README.md) which will lead you to the proper instructions in part [4. Audio configuration](audio/README.md) corresponding to your case.

You will then have to configure OBS to make it [stream to your favorite platform (part 5)](streaming.md)

There is also a [Troubleshooting](troubleshooting.md) part that should help you to solve most encountered problems.

## Why I wrote this guide?
It began during the COVID-19 lockdown. During this period we saw many initiatives (online festivals, groups, personal projects) aiming to live stream artists and musicians performing from their home.
I got somehow involved in some of these projects (especially the [Sottkvi festival](https://www.facebook.com/sottkvifestival/))and saw the lack of information regarding the audio configuration, which can differ A LOT depending on the musical project itself. So I tried to find a solution for most cases and sorting everything properly allowing people to find which case fit their needs and how to do it.

---

[^1]Sorry dear Linux user, I have no specific instructions for you, but you might still find this guide useful! Solution logics are the same but you will have to find compatible alternative softwares by yourself. Have a look at [Jack Audio](https://jackaudio.org/) or [Pulse Audio](https://www.freedesktop.org/wiki/Software/PulseAudio/).
