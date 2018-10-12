# Noisemakers
This repository contains all of the code we used to create the various projects for Noisemakers! Tracing the Origins of Modern Music in Italy, including our Max MSP patches and C++ Arduino code.

<b>The Basic Max Patch</b>
<br />
The Basic Max patch was designed to work with a Novation Launch Control (it is mapped to the first column of the device). It can be placed in a folder with an audio file. That file will then need to be added and named in the patch's buffer object (upper left), and the name will need to be added to the groove object at the bottom of the patch. Here is how it works:

<i>Playing the sound file</i>
<img src="http://web.colby.edu/noisemakers/files/2018/10/documentation1.png" alt="Playing the sound file">

<i>Adding frequency and pitch shift control
<br />
N.B. Timeshifting (i.e., keeping the pitch from changing with speed) can also be applied to the Groove object via the Inspector.)</i>
<img src="http://web.colby.edu/noisemakers/files/2018/10/documentation2.png" alt="Adding frequency and pitch shift controls">

<i>Smoothing out the controller responses with a little math</i>
<img src="http://web.colby.edu/noisemakers/files/2018/10/documentation3.png" alt="Smoothing things out with a little math">

<i>Simplifying the MIDI setup</i>
<img src="http://web.colby.edu/noisemakers/files/2018/10/FinalTouch.png" alt="Simplifying the MIDI setup">

<b>The Arduino Controller</b>
<br />
The Arduino controller should be wired so that the button is connected to digital input pin 2 and the pots are connected to analog input pins A0 and A1 (the inputs for the basic Max patch should then be changed to 36 for the button and 1 and 2 for the pots):

<img src="http://web.colby.edu/noisemakers/files/2018/10/IMG_1692.jpg">

After downloading the Arduino program, place it in a folder with the same name as the file before opening it and loading it onto the controller.

Use <a href="http://projectgus.github.io/hairless-midiserial/">Hairless MIDI</a> as a bridge to get the MIDI output from the Arduino to Max via USB:

<img src="http://web.colby.edu/noisemakers/files/2018/10/Patch.png">

<b>The Waterville Map</b>
<br />
<img src="http://web.colby.edu/noisemakers/files/2018/10/IMG_1467.jpg">

The Max patch is based on the basic patch above but adds reverb and panning to each loop.

The basic Arduino program has been adapted so that we could use multiplexer (mux) boards to add additional input pins for the pots. These were then combined into a single output from the mux board and wired into a single input on the Arduino. We are fairly certain there are still some bugs in the code that need to be squashed.
