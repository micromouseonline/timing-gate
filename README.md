# timing-gate
Thoughts about a contest timing gate

Nothing to see here yet. Just collecting thoughts.

Typical timing gates for micromouse and line follower contests or other racing type events are break-beam systems. There are (expensive) commercial sensors for this but it is better to make a bespoke device.

Break-beam systems normally require a transmitter and receiver on either side of the gate. That means they must either have a wire connection between them or both parts must be independently powered. Wiring between the parts is not always convenient in a maze. Independant power means looking after twice as many batteries.

Single-sided systems may use a mirror or may measure the reflectance from the opposite wal/post and detect changes.

If battery powered, the batteries need to be able to last throughout a day's contest so a design life of 12 hours is not too much.

Sensors will be optical. 

They should not interfere with the sensors on the robots and vice-versa. This may require one or more of the following::
* the transmitter power is low.
* transmitter wavelength is outside the range used by typical robots.
* frequencies of pulsed systems are distinct from typical robot sensor frequencies.
* narrow beams are used to minimise direct observation of or by the robot sensors.

It is likely that the gate emitter will be low-power and pulsed to try and mitigate interference effects.

Synchronous detection should eliminate effects of ambient light. Choice of frequency could be arranged to be relatively asynchronous with most robot systems. Robot builders are likely to employ simple frequencies that are based on the control loop timing and that is likely to be a multiple of 500Hz.

Possily, a pseudo-random emitter pulse might help avoid any interference from robot sensors.

Fixed frequency emitters in the timing gate could use high-sensitivity, narrow-band tone detection to look for occlusion of a break beam sensor.

DSP techniques could remove DC bias from a reflected signal and then perform envelope or edge detection to identify crossings by the robot.

Gate timing resolution should be better than +/- 0.5ms given that run times can differ by only a few milliseconds.

References:

*  [Goertzel Tone detection](https://www.embedded.com/design/configurable-systems/4024443/The-Goertzel-Algorithm)
*  [Arduino Goertzel Library](https://github.com/jacobrosenthal/Goertzel)
*  [Arduino DTMF Decoder](https://www.hackster.io/MM_Shoaib/dtmf-decoder-using-only-arduino-872502)
*  [Frequency Detection with IIR Filter](http://sam-koblenski.blogspot.com/2015/11/everyday-dsp-for-programmers-frequency.html)
*  [DC and Impulsive Noise Removal](http://sam-koblenski.blogspot.com/2015/11/everyday-dsp-for-programmers-dc-and.html)
*  [Frequency Measurement](http://sam-koblenski.blogspot.com/2015/10/everyday-dsp-for-programmers-frequency.html)
*  [Envelope Detection](http://sam-koblenski.blogspot.com/2015/10/everyday-dsp-for-programmers-signal.html)








