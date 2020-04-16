# Case 1: OBS + Mic/Aux Source

You are into Case 1 if:
> -   You just want to you a mic to capture you performance
>     -   You use a USB mic, a built-in mic, the webcam's built-in mic or the line input of your computer.
>     -   Your mic is connected to an external sound card
>         -   You use macOS
>         -   You use Windows and the MME/DirextX drivers for your sound card
> -   You use macOS with an audio software and
>     -   An external sound card with multiple initialization from multiple applications and a built-in loop-back feature
>     -   An external sound card compatible with multiple initialization from multiple application, and enough available outputs and inputs
>     -   Two external sound cards
> -   You use Windows with an audio software and
>     -   a secondary external sound card with MME/DirectX drivers as a looback input, or
>     -   an external sound card with ASIO drivers and you loop your audio back into your built-in computer line-input.

If your whole audio come from a microphone, it may be already
automatically selected as Mic/Aux source in the audio mixer.

If not, you should be able to select it or any appropriate (non ASIO)
audio input into OBS Preferences \> "Audio" tab \> "Mic/auxiliary Audio"
drop-down list.

You can also click the gear near-by the Mic/Aux source in the Audio
Mixer, then click properties and select your correct or audio input in
the "Device" drop-down list.

You should then see the Mix/Aux VU-meter reacting to the captured audio.
If so your audio is properly configured, good! You are now ready for
part 3.
