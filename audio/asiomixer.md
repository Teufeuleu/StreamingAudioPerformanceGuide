# Case 5: OBS + OBS-ASIO + ASIO mixer (Windows only)

You are in Case 5 if:
> You are desperate.

This is by far the hardest case of all, but also the most documented online. I honestly could not make one of the following solutions work properly. It always resulted in unplayable latency or audio crackles. I think it should work as expected (with very few extra latency) if you use an external sound card as an output only (your performance does not require external microphone or instruments), as you can see in some tutorials on Youtube, but otherwise it just did not worked for me. As I consider ReaStream (see Case 3) as a way more effective solution for now, I will simply list different solutions I found and I will let you look by yourself for some proper tutorials online.

-   [VoiceMeeter Banana](https://download.vb-audio.com/Download_CABLE/VoicemeeterProSetup.exe) (free) is maybe the most user friendly and most documented solution.
-   [Asio Link Pro](https://give.academy/posts/2018/03/02/AsioLinkPro/) (free) should be the most powerful and flexible solution, bu also the hardest to set up (thanks to a 20 years old GUI). [For the record](https://give.academy/posts/2018/03/02/AsioLinkPro/), it's an old piece of software which you had to pay for. The developer passed away a few years ago so nobody could buy it anymore. In 2019 his nephew decided to create a "legit" crack allowing anyone to use Asio Link Pro for free.
-   [Jack Audio](https://jackaudio.org/downloads/) (free, open source) should be actually simpler to configure even though it does not provide a GUI (graphical user interface). All is done with command lines, but you need very few to get your setup working properly.
- [Synchronous Audio Router](http://sar.audio/) (free, open source) might be another solution.

If all these solutions seem too hard to get through, just go with [Case 3](reastream.md).
