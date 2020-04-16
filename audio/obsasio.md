# Case 4: OBS + OBS-ASIO (Windows only)

You are in case 4 if:
> You uses Windows with ASIO drivers, whether using or not an audio software and/or an external sound card.

1.  Check the version of OBS you are using: in OBS, click "Help" in the menu bar, then "About. The version number is just below the "OBS Studio" label.

2.  Close OBS, then download [OBS-ASIO](https://github.com/Andersama/obs-asio). Here are the direct download link depending on your OBS Studio version: [25.x.x](https://github.com/Andersama/obs-asio/releases/download/v2.0.2/obs-asio-installer_2.0.2.exe) and above (preferred), [24.x.x](https://github.com/Andersama/obs-asio/releases/download/2.0.0/obs-asio-installer_2.0.0_obs24.exe) or [23.x.x](https://github.com/Andersama/obs-asio/releases/download/2.0.0/obs-asio-installer_2.0.0_obs23.exe).

3.  Then install the plugin.

4.  Re-open OBS.

5.  Click the "+" in the Sources window, and select "ASIO" to create a new ASIO source. Give it the name you want and click OK.

6.  In the appearing window, choose your ASIO device:
    -   If you use an external sound card with a built-in loopback feature or if you physically hard-wired an audio input of your external sound car back into one of its inputs, then choose this external sound cards driver
    -   If you use two external sound cards, choose the secondary sound cards driver (the one in which you looped back your primary external sound cards output)
    -   If you created a virtual ASIO input device using VoiceMeeter Banana, Asio Link Pro or Jack Audio, ReaRoute, choose the corresponding ASIO driver.

7.  Choose "Stereo" in the Format field
8.  In OBS Channels 1 and 2 (stands for left and right channels), select the appropriate ASIO inputs you looped your audio back into.
9.  Click OK then in the OBS Audio Mixer you should see the VU-meter of the created ASIO source moving relatively to the sound your audio software is outputting. If so, you are good to go to part 3!
