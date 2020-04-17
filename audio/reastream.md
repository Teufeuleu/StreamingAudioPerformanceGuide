# Case 3: OBS + ReaStream VST (Windows only)

You are into Case 3 if:
> You use Windows with an audio software and ASIO drivers, with or without external sound card.

This case work for any kind of ASIO driver, regardless the use of an external sound card or not. It can actually work also with any other kind of driver (MME/DirectX/WASAPI) but you should rather refer to [Case 2: OBS + Desktop Audio Source](desktopaudio.md) if you use one of those.

---

The following instructions are based on ReaStream, a VST plugin made to send audio and midi in real time over a local network. Here we will use it on a same comuter as a bridge between your DAW and OBS.

1. ReaStream is included in a suite of free plugins called ReaPlugs VST FX Suite you can download [here](https://www.reaper.fm/reaplugs/). Choose the 32bit or 64bit version depending on your audio software (Ableton Live 10 is 64bit only, other might depend).

2. Run the installer. In the "Choose Components" screen, you only need ReaStream (stereo) but you can select other plugins if you want to try them.

3. In the "Destination Folder", make sure you are using one of the [following](https://github.com/obsproject/obs-studio/wiki/Filters-Guide#vst-plugin) (see list below), otherwise the VST wont be available in OBS. Click Install and you're done. If you usually use a custom folder for your VSTs, just re-install ReaStream to your custom folder once you got it installed in one recognized by OBS:
  - C:/Program Files/Steinberg/VstPlugins/
  - C:/Program Files/Common Files/Steinberg/Shared Components/
  - C:/Program Files/Common Files/VST2
  - C:/Program Files/Common Files/VSTPlugins/
  - C:/Program Files/VSTPlugins/

4. Open your audio software and add the **reastream-standalone** VST plugin on your master track. You should see a firewall alert saying that the plugin want to access your network. Just allow it on both private and public networks, just in case, and click OK. Now on the plug-ins interface, select "Send audio/MIDI" then choose/type `\*local broadcast` (without quotation marks) in the IP field.

5. Open OBS, click the ➕ in the Sources window and select "Audio **input** capture". Give it any name you want, and click OK.

6. As Device, choose an audio input you are NOT using. We actually don't care of the audio input itself, as we want the audio coming from the VST we will add in the next steps. So just use an unused audio input. If you can only select some used inputs (such as your default microphone), then is is still OK, we will figure it out later. Click OK.

7. Now right click on your newly created audio input capture source, and select "Filters".

8. If you had no unused audio input available, you want to turn down the volume of your used audio input without turning down the volume of the OBS audio source itself. To do so, add two "Gain" Filters and set them to -30dB.

9. Ad a new audio filter by clicking the +, and select "VST 2.x Plug-in". Give it the name you want and click OK.

10. In the VST 2.x Plug-in drop-down list, select "reastream-standalone", then click "Open Plug-in Interface". Windows should prompt you again the firewall security message. Just allow everything one more time.

11. Make sure the Identifier is the same as the one you set in Ableton ("default" by default), and you're done.

12. Now if you play some sound in your audio software you should get it into your OBS audio input capture device. If so, you're good to go to part [5. Streaming configuration](../streaming.md). If not, see below for some troubleshooting.

## What to do if ReaStream in OBS does not receive sound from my audio software?

- Make sure you are using the same sample rate (44.1Khz or 48KHz) in your audio software and OBS (Settings \> Audio tab)
- Right click the Audio input capture, open "Properties" then select another input device. For some reasons, it might not work with some devices (especially the "Default" one).
- In ReaStream in your audio software, replace `* local broadcast` by `127.0.0.1`. It is a special IP address saying "this very own computer".
- Try changing to another identifier in both OBS and your audio software. Sometimes, just clicking in the Identifier field and hitting "Enter" can re-instanciate the plugin an make it work.

What to do you it seem like there is some latency between the received audio in OBS and the captured video? Just check the related [troubleshooting part](troubleshooting.md#troubleshooting-audio-and-video-not-in-sync-in-obs) of this guide.
