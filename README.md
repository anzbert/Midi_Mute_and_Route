<a href='https://ko-fi.com/S6S8SP865' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/kofi4.png?v=3' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>

# Midi Mute&Route

## What does it do?

A Reaktor Plugin which lets all incoming Audio pass through unless it receives a Midi Note, in which case it mutes the Sound on the main Output Bus of this plugin. Primarily made for Maschine, but it can still be used in any other project.

As a secondary function, it can mute and then route the muted audio to the Output Buses 2 to 8 of the plugin, where it can be used, for example, for fast and glitchy performance FX chains.

## Basic Usage on Maschine

Load Midi Mute&Route onto a Pad and route audio to it from any other sound or group. You can then play the pad with the plugin to mute the routed audio.

Mutes can easily be recorded onto a midi pattern or a clip just like any other instrument.

## Settings

Choose the Midi Note which triggers the Mute function. The default note is 60, which is the default Note sent by any Pad on Maschine. (Default: 60 / C3)

The Attack time of the mute and unmute can be set in milliseconds. Turn lower for a faster reaction time and higher if clicks are audible. (Default: 3 ms)

The plugin function can be reversed with the Invert switch. This has somewhat of a latching effect. (Default: Off)

## FX Routing

When the plugin receives a note between 1 and 7 semitones above the configured Mute Note, the basic mute is activated and the audio is temporarily routed to the plugin's Output Bus corresponding to that note. For example, if the Mute trigger note is the default note of 60, 61 would route the Audio to Output Bus 2 and 62 would route it to Output Bus 3, etc...

There are a number of creative use cases for this. Try these steps as an example on how to have fun with it:

1. Load Midi Mute&Route as Sound 1 in a Group and route Audio from one or multiple source Groups or Sounds through it. This step is still part of the basic setup.
2. Load a few FX plugins onto Sound 2 of the Group. For example something severe, like a Lofi and a Frequency Shifter.
3. In the channel Audio Input settings of Sound 2, set 'Audio In' to 'Output Bus 2' of Midi Mute&Route on Sound 1.
4. In the channel Midi Output settings of Sound 2, set 'Midi Out' to Sound 1 and set Transpose to 1, to send Note 61 on a pad press (instead of the default Note 60).
5. Now play! The pad with Midi Mute&Route still has the muting function and the pad with the FX chain mutes and applies its effects. Yay!!

When the Maschine is set to show the current Sound plugin you can even tweak the knobs as you play an effect chain.

Maybe take it further and add different effects on different Sound Pads in this Group. Make sure each Pad has its Audio input configured to a different Output Bus of Midi Mute&Route and its Midi Output set to send the corresponding Midi Note. This setup can serve as an alternative to Automation and Lock States. You could create a whole setup of instant FX pads, with the performance being easily recordable.

Other configurations are also conceivable. For example, you could route FX pads and versions of this plugin in Series, combine this plugin with Perform FX and Automation, use invert to latch FX and Mute on and off, try playing the pads with Note Repeat while playing with the Arp Gate and Timing, etc....

## Maschine +

Maschine Plus standalone compatible. Just copy to the SD card to this folder:

/Native Instruments/User Content/Reaktor/Ensembles/

## Example Template

A routing example template is available in the Github Repo here: https://github.com/anzbert/Midi_Mute_and_Route

Just copy the content of MidiMuteTemplate.zip to your Maschine folder. For example on the Maschine Plus SD card that would be:

/Native Instruments/Maschine 2/

Make sure the latest Midi Mute&Route is installed into the Reaktor Ensemble folder, as described above.

All the routings should be done for you in this template. The example contains one mute button and 7 routes to be filled fith FX. There is also a Reverb and Delay Send, just to have a nice global FX group available.

This template can also be used on desktop, but since the absolute path to the Reaktor Ensembles folder is different there, you will just have to double click on the Midi Mute&Route plugin once and locate the ensemble on your device. Just save the template afterwards for future use.

## Feedback and Development

Feedback is appreciated. I am happy to add useful functions and fix bugs. I am still working on the optimal workflow for this plugin and I may change the available routing options in future releases.

Email me at anzbert@gmail.com

[Source](https://github.com/anzbert/Midi_Mute_and_Route)

And join the discussion in the Maschine forum [here](https://community.native-instruments.com/discussion/comment/126507).

## Change Log

- 0.8 - Fixed Maschine Knob Assignments / Removed unassigned and reserved controls
- 0.7 - This is the first Release out of the Test stage. Enabled all 8 Output Buses and made them responsive to different notes. Updated the UI to show all current Midi trigger inputs with corresponding Buses.
- 0.6 - Updated the UI Style.
- 0.5.2 - Set input Midi to Omni by default. Fixed plugin not loading anymore because of Reaktor version mismatch
- 0.5 - Connected Output Bus 2 for optional use of the currently muted signal
- 0.4 - Added an Attack time selector
- 0.3 - Added Invert Button
- 0.2 - First Release
