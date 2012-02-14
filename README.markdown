wavPlayerAsio - ASIO wave player for multiple simultanious outputs
==================================================================

The aim of this project is to provide a loadable DLL with a very simple interface.

The interface is intended to look like so:
    Player p1 = new Player();

    // play on channels 1 + 2 [1-based]
    p1.load("D:\\some_long_sound.wav", new UInt16[] {1, 2}); 
    p1.play()
    p1.xfade(millicesonds);
    p1.loop(true);

    // after some time:
    p1.loop(false);

    // or stop manually:
    p1.stop(false);

There should be any number of concurrent playing players possible.
Just make sure the output doesn't clip (>= 0 dB).
