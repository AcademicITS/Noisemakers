# Noisemakers
This repository contains all of the code we used to create the various projects for Noisemakers! Tracing the Origins of Modern Music in Italy, including our Max MSP patches and C++ Arduino code.

<b>The Basic Max Patch</b>
<br />
The Basic Max patch can be placed in a folder with an audio file. That file will then need to be added and named in the patch's buffer object (upper left) and the name will need to be added to the groove object at the bottom of the patch. Here is how it works:

<img src="http://web.colby.edu/noisemakers/files/2018/10/documentation1.png" alt="Playing the sound file">

<img src="http://web.colby.edu/noisemakers/files/2018/10/documentation2.png" alt="Adding frequency and pitch shift controls">

<img src="http://web.colby.edu/noisemakers/files/2018/10/documentation3.png" alt="Smoothing things out with a little math">

<img src="http://web.colby.edu/noisemakers/files/2018/10/FinalTouch.png" alt="Simplifying the MIDI setup">

<b>The Arduino Controller</b>
<br />
The Arduino controller should be wired so that the button is connected to digital input pin 2 and the pots are connected to analog input pins A0 and A1:

<img src="http://web.colby.edu/noisemakers/files/2018/10/IMG_1692.jpg">

Use <a href="http://projectgus.github.io/hairless-midiserial/">Hairless MIDI</a> as a bridge to get the MIDI output from the Arduino to Max via USB:

<img src="http://web.colby.edu/noisemakers/files/2018/10/Patch.png">

<b>The Waterville Map</b>
<br />
The Max patch is based on the basic patch above but adds reverb and panning to each loop.
