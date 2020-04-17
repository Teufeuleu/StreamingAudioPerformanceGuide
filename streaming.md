# 5. Streaming configuration

## Testing your internet connection

First of all, you need to know how good is your internet connection, to know if it is suitable or not for video live streaming. You have to make sure it is **fast** enough **stable** enough.

To know if it is fast enough, you can test it using [Speedtest](https://www.speedtest.net/) on the computer or smartphone you will use for your stream. Mind that for the best results, you should close all your opened websites, disconnect all your devices but the one you will test the connection with, and use a wired (LAN/ethernet) connection when possible.

Here we're interested in your **upload speed**, so the amount of data your device can send to the internet every seconds. In many cases it is much slower than the download speed (and people generally just remember their download speed) so it's important to test it.

In order to live stream audio an video at a decent quality, the bare minimum required upload speed is about **2Mbps**. It can still work below but in low quality and with possible drop outs. Also, be careful: a fast connection does NOT mean a stable connection.

If your connection sometimes randomly drops off, or get super slow for a few minutes or this kind of problem, that would mean that your internet connection may not be stable enough for a live stream and you should consider pre-record your performance, and make the resulting video streamed from another computer or video platform, which is out of the scope of this guide. I found now way of testing stability easily other than your personal experience, so it's really up to you.

## WTF is a bitrate and how do I choose one ?

The other critical part here is the **video bitrate** of your stream. A bitrate is the amount of data a stream needs for each second. The higher the bitrate is, the better the stream's quality is supposed to be, but the higher your internet connection speed need to be. If you dont want to go further in explanation, just remember to use a video bitrate of **850Kbps**. It's quite low in term of quality but it should be okay for most internet connection.

Now let's get a bit more technical. Remind your upload speed [you just tested](#testing-your-internet-connection). If your internet connection upload speed is 2Mbps, you should be able to stream with a maximum bitrate of 2Mbps (including both video and sound). But for security reasons, and because both an internet connection and a video bitrate are never perfectly stable, we will limit our bitrate to the half of your upload speed. So if your measured upload speed was 2Mbps, your total stream bitrate should not exceed 1Mbs including both video and audio.

As we want to keep the best possible audio quality, we will stay with a 160Kbps audio bitrate. The rest can be used for the video. So in our example of a maximum 1Mbps (=1000Kbps) stream bitrate, we have 1000-160=840Kbps available for the video bitrate. about the same 850Kbps value I gave earlier.

Let's write a global formula to calculate a safe video bitrate:

$$\Large {\text{Video bitrate} = {\text{Measured upload speed} \over 2} - \text{audio bitrate}}$$

with "audio bitrate" = 160Kbps for a better audio quality.

**Please don't use a video bitrate above 4000Kbps** even if your internet connection can handle it! There will be no real benefits in term of quality for a video stream of 1280x720 at 30 fps, so a higher bitrate basically means waisted bandwidth and energy. You can have further precisions about which bitrate to choose on [this page](https://support.video.ibm.com/hc/en-us/articles/207852117-Internet-connection-and-recommended-encoding-settings).


## Configuring OBS

1. Open OBS, then go to Settings panel, and set the configuration as follow:

    1. In the Stream tab,:
        - Service: select the streaming platform of your choice.
        - Other settings: please refer to your platforms documentation or some online tutorials. Generally speaking, the streaming platform will give you a unique link you have to copy in OBS, as well as entering your platforms credentials.

    - Output tab:
        - Video bitrate: set the calculated bitrate as seen [above](#wtf-is-a-bitrate-and-how-do-i-choose-one-). If you don't know what to use, set it to 850Kpbs.
        - Encoder: if available, choose "Hardware" (might need an Nvidia graphic card). Otherwise choose "Software (x264)"
        - Audio Bitrate: 160 (we always want the best quality here)

    - Video tab
        - Output (Scaled) Resolution: **1280x720** (OK for most people)
        - Downscale filter: Bicubic
        - Common FPS Value: 30fps

2. Hit OK to save your preferences.

3. Check one last time in the audio mixer if your audio is working, then start streaming!

4. To monitor how your stream is going, refer to the bottom bar, showing the number of dropped frames and a colored square indicating the connections status. Your amount of dropped frames should be near 0%. If it is not the case, then you might have some internet connection issues or your computer is too slow. See the [Troubleshooting](troubleshooting.md) part for some advices.
