# My performance requires an audio software but no external sound card

Choose the case corresponding to your situation:

-   **macOS users**: refer to [Case 6: OBS + BlackHole (macOS only)](../audio/blackhole.md).

-   **Windows users**:

    -   If you use default **MME/DirectX drivers**, refer to [Case 2: OBS + Desktop Audio Source](../audio/desktopaudio.md)

    -   If you use **ASIO drivers** (such as [ASIO4ALL](http://www.asio4all.org/), [FL Studio ASIO](https://www.image-line.com/support/flstudio_online_manual/html/envsettings_audio.htm#FLStudioASIO) installed along with [FL Studio](https://www.image-line.com/downloads/flstudiodownload.html) but compatible with any audio software, or [ReaRoute](https://www.soundonsound.com/techniques/route-master) with [Reaper](https://www.reaper.fm/)), you have two solutions:

        -   The **ReaStream VST plugin** solution might be the simplest one as you keep your audio software configured as usual with your favorite ASIO drivers. Refer to [Case 3: OBS + ReaStream VST (Windows only)](../audio/reastream.md).
        -   You can also choose to keep your audio in an ASIO context using an additional **ASIO mixer** such as [VoiceMeeter Banana](https://www.vb-audio.com/Voicemeeter/banana.htm), [Asio Link Pro](https://discuss.cakewalk.com/index.php?/topic/3519-odeus-asio-link-now-available-free/) or [Jack Audio](https://jackaudio.org/downloads/) (all free). This is the most tricky way to go and can be hard to configure properly to get less latency than with MME/DirectX drivers or ReaStream. Because latency is why you use ASIO drivers I guess. You can refer to [Case 5: OBS + OBS-ASIO + ASIO mixer (Windows only)](../audio/asiomixer.md) if you want to give it a try, and go back to [Case 3](../audio/reastream.md) if you are unsuccessful.
