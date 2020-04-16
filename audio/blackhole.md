# Case 6: OBS + BlackHole (macOS only)

You are in Case 6 if:
> You use macOS and an audio software, and maybe an external sound card with no built-in loopback feature.

BlackHole is the new "virtual audio device for macOS" replacement for SoundFlower. It works the same but is likely more stable and still in development. If you still want SoundFlower, look [here](https://github.com/mattingalls/Soundflower), then instructions are the same than for BlackHole.

1.  Download and install BlackHole following [official instructions](https://github.com/ExistentialAudio/BlackHole/wiki/Installation) (easy)

2.  Then open "Audio Midi Setup" app located in Applications/Utility. Once opened, click "Window" in the menu bar, then "Show audio devices".

3.  Click the "+" in the bottom left, then "Add a multi-output device"

4.  Click on the multi-output device you just created, then, depending on your case:
  -   If you uses no external sound card, tick the "Use" box for **each** of the following devices:
      -   "BlackHole" (will be sent to OBS)
      -   The built-in output you will hear you back through.
  -   If you uses an external sound card, select it in the "Master device" (or "Main device") field at the top of the window, then tick the "Use" box for the following devices:
      -   "BlackHole" (will be sent to OBS)
      -   The desired device you will hear you back through (should be your external sound card)
      -   Even if you don't use it, tick your computer built-in output (normally not necessary but it's a workaround to face some issues, as stated [here](https://github.com/ExistentialAudio/BlackHole/wiki/Multi-Output-Device)).

5.  In your audio software, select the Multi-output device you just created as your audio output.
6.  In OBS, open the Preferences/Settings, panel, go to the Audio tab, and select BlackHole as your Desktop Audio device. Click OK.
7.  You should then see the corresponding VU-meter in the Audio mixer reacting to the audio sent by your audio software. You're done! Ready for part 3.
