# Troubleshooting

This page consists in a list of advices to solve most problems, split in three categories:
- [Troubleshooting OBS dropping frames](troubleshooting.md#troubleshooting-obs-dropping-frames)
- [Troubleshooting audio and video not in sync in OBS](troubleshooting.md#troubleshooting-audio-and-video-not-in-sync-in-obs)
- [Troubleshooting audio crackles and latency issue](troubleshooting.md#troubleshooting-audio-crackles-and-latency-issue)

---

## Troubleshooting OBS dropping frames

-   If you're using an audio software and that your sound is NOT crackling, then your dropped frames should come from an internet connection issue. You want to improve your internet connection and/or lower the bitrate of your stream:

  - Prefer a LAN (wired) connection rather than WIFI when using a computer

  - Lower the video bitrate of your stream

-   If you hear crackling while dropping frames, then your computer might not be powerful enough. You want to lower the CPU usage:

  - Close/kill all ongoing useless applications/process during the performance (web browser, Steam...).

  - In OBS Settings panel, go in the Video tab and set the Downscale Filter to `Bilinear`

  - In OBS Settings panel, go in the Output tab, tick "Enable Advanced Encoder Settings" and choose a faster "Encoder preset". Depending on your computer hardware, presets can be named from slower to faster or from quality to performance. Both mean the same: choosing a faster or more performant encoding preset will result in a lower video quality but in more available CPU resources

  - You want to make OBS and your audio software use less CPU ([see Troubleshooting audio crackles and latency issue]()).

-   See [this page](https://obsproject.com/wiki/Dropped-Frames-and-General-Connection-Issues) for more informations


## Troubleshooting audio and video not in sync in OBS

After a few minutes of streaming, you might notice a slight **delay between the video and the audio** in OBS. I noticed that sometimes, even if you see a delay between your VU-meter or monitored audio and your camera in OBS, your stream is still correctly synchronized. To be sure of that, just connect to your own stream using VLC or a web browser.

If you are experiencing a true delay between your video and audio in OBS, there are a few things you can do. Latency can be frequent especially if you use your smartphone as an external webcam for OBS. It can also happen many other cases for many different reasons.

-   Be sure that you are using the same audio sample rate (48KHz or 44.1KHz) in every involved software/hardware (external sound card, audio software, OBS...)

-   Click the gear ⚙️ corresponding to your audio source in the OBS Audio Mixer, and select Properties. If there is a box labeled "Use device timestamp", try to check or uncheck it and click OK.

-   If your audio is always in advance compared to your video, you can retard it by clicking a gear in the OBS Audio Mixer, select "Advanced Audio Properties", and increase the value of "Sync offset" corresponding to your audio source. A value of 1500ms means a retard of 1.5 seconds is applied to your audio.

-   If your video is always in advance compared to your audio, you can retard it by following these steps:

    -   Right click your camera source in the OBS Sources window, and select "Filters". Click the ➕ under "Audio/video filters" and select "Video delay (async)".
    -   Set the desired delay (a value of 1500ms means a retard of 1.5 seconds is applied to your video) and click OK.

## Troubleshooting audio crackles and latency issue

Here we are talking about the latency between you playing and what you hear back. We are not talking about latency in OBS.

-   Don't be afraid to restart your computer once you installed something new. Restarting OBS and/or your audio software can also help.

-   Mind to **use the same sample rate** everywhere in your audio software, external sound card and OBS settings. We will prefer 48KHz but 44.1KHz is fine too (and a bit lighter for your CPU).

-   You can improve the latency of your audio software by lowering your buffer size. A 128 samples buffer size will lead to two times less latency than a 256 samples buffer size. However it is more CPU intensive, so you might experience crackles.

-   Make your audio project as light as possible: disable unused inputs and outputs, delete unused tracks, VSTs and plugins, export to audio (or "freeze" in Ableton jargon) the tracks you don't play with during you performance\...

-   To improve CPU performance (allow more CPU resource to your audio software), you can go into OBS settings panel,
