# Video configuration

1. Once you opened OBS for the first time, you should see a scene called `Scene` in the Scenes window. You can see it is empty as it has no source attached to it.

3.  Now we need to add a video source in our scene. You can use both a webcam or a smartphone as a camera.

    -   Using your webcam:
        -   Click the ➕ in the Sources window, and choose `Video capture device`
        -   Select `Create new`, set whatever name you want and click OK. The properties window of the video capture device appears. Your webcam should then appear in the devices list. If not, refer to your webcam's manual.
        -   Depending on your webcam you should have several settings. Let's stay with defaults and click OK. If you need to re-open the properties windows, just double-click the created video capture device in the Sources window.

    -   Using a smartphone's camera.
        -   You have several solutions to use your phone's camera as a webcam in OBS, such as [EpocCam](http://www.kinoni.com/epoccam_support.html) (for iOS and Android, free version with low quality, paid version for full quality), [DroidCam](https://play.google.com/store/apps/details?id=com.dreamdroid.livedroid) (Android only, free) or [NDI HX Camera](https://apps.apple.com/us/app/ndi-hx-camera/id1477266080?ls=1​) (iOS only, free, you will also need the [OBS-NDI](https://github.com/Palakis/obs-ndi/releases) plugin to make it work)). The steps to get these apps working in OBS are quite simple and can be easily found on developers websites or on youtube. Notice that most of these apps require your phone to be Wifi connected to your home network, so you cannot use it as a 4G internet hotspot at the same time.
        -   Once you added your phone as a video source in OBS, you might see it also appear as an audio source in the OBS audio mixer with the "video capture device" name you set earlier. You most like want to disable this audio source as you will get your sound from a proper mic or your audio software as we will see.

4.  Once you created your video source, make sure it fill the whole area of your scene by stretching it to the correct dimension. To stretch it, select the source in the Sources window, then a red frame should appear around your view. Click a corner and stretch.

5.  Good, you can now go to the next part to [configure your audio](audio/README.md).
