# notes-Mahdi03

<h2>Final Project - Gimmel!!!</h2>
<em>Collaborated with @joeljaffesd</em> <br />
<strong>Portable, Lightweight, Header-only C++ Realtime Digital Audio Effects Library</strong>: <a href="https://github.com/Mahdi03/Gimmel">Gimmel</a>

<h2>Project 2 - Sound Design</h2>
<em>Collaborated with @joeljaffesd</em>
<p>&emsp;&emsp;For this project we built a Reverb effect using concepts from physical modeling. We controlled the shape, size, and material of the pretend room the sound was meant to reverbrate through. The Reverb effect is entirely customizeable, taking after a Schroeder Reverb design:</p>
<img src="https://github.com/allolib-s24/notes-Mahdi03/assets/25967114/33095b4f-776c-4287-b651-54635858c56d" />

<p>However, our design uses rare techniques such as tangential interpolation and slightly modified low-pass filter techniques to achieve the unique sound you hear in the video. Instead of using just 4 comb filters in parallel, you're hearing 20. Instead of just 2 all-pass filters in series at the tail-end, we've employed 4 nested all-pass reverbrator "circuits" (two on each side). Finally, the reverb effect is mixed in with the original ("dry") signal towards the end so that you can hear what it should actually sound like. The parameters you see in the video are:</p>
<ul>
	<li><strong>Time</strong> - The spacing of the comb filters in their impulse response (keep at a lower range if you don't want distant echoes)</li>
	<li><strong>Space</strong> - The side length of whatever shape we are modeling (grows at a cubic rate because volume)</li>
	<li><strong>"Regen"</strong> - The feedback in our special Low-Pass Filter implementation (keep at a lower range if you don't want distant echoes)</li>
	<li><strong>Damping</strong> - The feedback for the LPFs in the APFs, cancels higher-frequencies to make the bouncing of sound waves back to us more realistic. (increasing it too much will almost cancel all the audio as seen in the video)</li>
	<li><strong>Room Type</strong> - The shape of the simulated room, some options are currently hardcoded in but later will be user-editable</li>
 <li><strong>Absorption Coefficient</strong> - The average absorption of the materials that make up this simulated room, essentially how much we want the soud waves bouncing back to us or just being absorbed by the walls (0 means nothing is absorbed by the walls and 1 is completely absorbed by the walls)</li>
 <li><strong>Wet/Dry</strong> - How much of the original sound to mix with the reverb-modified sound (1 is completely "wet" and 0 is completely "dry")</li>
 
	
</ul>


<h2>Project 1 - Synthesis Piece</h2>
TODO:
