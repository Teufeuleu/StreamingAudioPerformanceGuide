# My performance requires an audio software and an external sound card

This might be the case for most of you. The idea is quite simple: we want to turn your main audio software output into an audio input in OBS. You can do that virtually, using your external sound card software (only for compatible models/drivers) or a 3^rd^ party virtual audio device, or you can do it physically, by wiring one of your external sound card's output to a physical audio input. Here are some details for all of these ways, each leading you to the **appropriate case shown in part 2 / Using a computer (OBS) / Audio setup**.

A virtual loopback might be preferred as it does not need extra piece of hardware, but depending on your case a hard-wired loopback can eventually be easier to achieve. Choose the option you feel the most comfortable with.


## Virtual loopback

-   Your sound card supports multi-initialization from multiple applications, and has a built-in **loopback feature**. It is the case of all 3^rd^ gen Focusrite Scarlett, 1^st^ gen 8i6 Focusrite Scarlett, most RME interfaces (using TotalMix), some Motu interfaces (using CueMix), the Roland Quad Capture, the Behringuer XR18, and some other devices I'm not aware of. This should be the best way to go as it is quite simple to configure and should add little to no additional latency. The loopback feature (generally accessible from your external sound card's mixer software) will allow you to route your audio output back into one of its (either virtual or physical) audio inputs. You can then easily select this input in OBS. First refer to your external sound cards owner manual to see how to use the loopack feature. Then, depending on your OS:

    -   macOS user: refer to **Case 1: OBS + Mic/Aux source**
    -   Windows: refer to **Case 4: OBS + OBS-ASIO** if your external sound card uses ASIO drivers, or **Case 1: OBS + Mic/Aux source** otherwise.

-   Whichever the external sound card you use, you can still create a virtual loopback using additional softwares (but it can increase your audio latency):

    -   macOS users: refer to **Case 6: OBS + BlackHole (macOS only)**

    -   Windows users:

        -   The ReaStream VST plugin solution might be the simplest one as it should work for any case and it allow you to keep your audio software configured as usual with your favorite sound card drivers (ASIO or other). Refer to **Case 3: OBS + ReaStream VST (Windows only)**
        -   If your external sound card uses MME/Direct drivers, you should be able to catch its output directly by selecting it as a "Desktop Audio" source in OBS. Refer to **Case 2: OBS + Desktop Audio source**
        -   If your external sound card uses ASIO drivers, you can try to use an additional ASIO mixer such as [VoiceMeeter Banana](https://www.vb-audio.com/Voicemeeter/banana.htm), [Asio Link Pro](https://discuss.cakewalk.com/index.php?/topic/3519-odeus-asio-link-now-available-free/) or [Jack Audio](https://jackaudio.org/downloads/) (all free). This is the most tricky way to go and can be hard to configure properly to get less latency than with MME/DirectX drivers or ReaStream. Complexity goes even higher if you need your external sound card to output/input audio to/from external audio effects, synths, mics involved in your performance... You can refer to **Case 5: OBS + OBS-ASIO + ASIO mixer** if you want to give it a try, and go back to **Case 3** (ReaStream) if you are unsuccessful.


## Physical (hard-wired) loopback

-   Your sound card does not provide a built-in loopback feature, but you have **two unused audio outputs** (or one stereo output) and possibly two unused audio inputs on your audio interface (can be an SPDIF in and out -- SPDIF is better for quality as the signal stays digital -- or two balanced jack/XLR outputs and two line inputs). If so, you can "manually" create a loopback with real cables from real life, by plugging your available output into your available input. The input can either be one of your external sound cards inputs, your computer built-in line mini-jack input (although not advised for quality reasons) or even a secondary external sound card (see next point). Notice that using an input from your only external sound card should only work if this sound card supports multiple initialization from multiple applications. As this feature is very rarely made explicit by sound card manufacturers, just try and see if it works. To proceed, in your audio software, find a way to double the output of your master (using a bus or return track, or an "External audio effect" in Ableton Live) so it can be sent to both your usual master/monitoring audio output, and the extra audio output available on your sound card. Then wire the selected secondary output back into an available input. Then:

    -   For macOS users, refer to **Case 1: OBS + Mic/Aux source**

    -   For Windows users:

        -   If you loop your audio back into your computer built-in line-input, refer to **Case 1: OBS + Mic/Aux source**
        -   If you use an available input on your external sound card, refer to **Case 4: OBS + OBS-ASIO** if your external sound card uses ASIO drivers, or **Case 1: OBS + Mic/Aux source** otherwise

-   You have **two external sound cards**, so you can use one with your audio software and the other one as an input for OBS. Your case is then similar to the previous one. You need to wire one of your main sound card output to the secondary audio interface input, then select this input in OBS. To do so:

    -   For macOS users, refer to **Case 1: OBS + Mic/Aux source**
    -   For Windows users: refer to **Case 4: OBS + OBS-ASIO** if your secondary external sound card uses ASIO drivers, or **Case 1: OBS + Mic/Aux source** otherwise
