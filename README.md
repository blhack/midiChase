###Midi Chase

To use this, you'll need a way of interfacing a midi signal generator (a controller) with your arduino.  I am using a midi shield I bought on amazon, but a simple opto-coupler would work too.

This sketch assumes that you are using an arduino UNO/Duecmilblahblah or other non-mega arduino.  If you want to use a mega (and get more serial ports, like for debugging), change the line that says:

    MIDI_CREATE_INSTANCE(HardwareSerial, Serial, MIDI);

to

    MIDI_CREATE_INSTANCE(HardwareSerial, Serial1, MIDI);

And connect the appropriate pins together.  In my case, it meant connecting the pin (on the midi shield) that normally plugs into the RX on my arduino into RX1 on the mega.

Read through the code, it is well commented.
