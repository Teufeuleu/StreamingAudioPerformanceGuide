# Case 2: OBS + Desktop Audio source

You are into Case 2 if:
> You use Windows with an audio software and MME/DirectX drivers, with or without external sound card.

---

It is as simple as case 1 but with a little variation.

1.  Open your audio software, make it play some sounds, and remember the audio output it's using

2.  Open OBS and go to its Preferences (Settings panel), then into the Audio tab.

3.  In the Devices / Desktop Audio drop-down list select the same output as your audio software.

4.  Click OK then in the OBS audio mixer you should see the VU-meter of the "Desktop Audio" source moving relatively to the sound your audio software is outputting. Sometimes it seems a big buggy and you need to click the gear ⚙️ of the Desktop Audio source, click Properties, then re-select the same output you just selected in the previous step. You can also try restarting OBS (don't worry, it will automatically save your session).

5.  Awesome, you are now ready to go to part [5. Streaming configuration](../streaming.md)!
