# Midi Mute&Route

## What does it do?

A Reaktor Plugin which lets all incoming Audio pass through unless it receives a Midi Note, in which case it mutes the Sound on the main Output Bus of this plugin. Primarily made for Maschine, but it can still be used in any other project.

As a secondary function, it can mute and then route the muted audio onto Output Bus 2 of the plugin, where it can be used, for example, for fast and glitchy performance FX chains.

## Basic Usage on Maschine

Load Midi Mute&Route onto a pad and route audio to it from any other sound or group. You can then play the pad with the plugin to mute the routed audio.

Mutes can easily be recorded onto a midi pattern or a clip just like any other instrument.

## Settings

Choose the Midi Note which triggers the Mute function. The default note is 60, or C3, which is the default Note sent by any Pad in Pads mode on Maschine. (Default: 60 / C3)

The Attack time of the mute and unmute can be set in milliseconds. Turn lower for a faster reaction time and higher if clicks are audible. (Default: 3 ms)

The Mute function can be turned into a Gate with the Invert switch. (Default: Off)

A second input note can be specified, which triggers the Mute&Route function. This could be sent from a second pad in the group. More on that under the next heading. (Default: 61 / C#3)

## FX Routing

When the Mute&Route note is triggered, the basic mute is activated and the audio is also temporarily routed to the plugin's Output Bus 2. There are a number of creative use cases for this. Try these steps as an example on how to get creative with it:

1. Load Midi Mute&Route as Sound 1 in a Group and route Audio from a source Group or Sound through it. This step is still part of the basic setup.
2. Load a few FX plugins onto Sound 2 of the Group. For example, A Lofi and a Beat Delay.
3. In the channel Audio Input settings of Sound 2, set 'Audio In' to 'Output Bus 2' of Midi Mute&Route on Sound 1.
4. In the channel Midi Output settings of Sound 2, set 'Midi Out' to Sound 1 and set Transpose to 1, to send Note 61 on a pad press, instead of the default Note 60.
5. Now play! The pad with Midi Mute&Route still has the muting function and the pad with the FX chain mutes and applies its effects. Yay!!

Maybe take it further and chain the output of both Sound 1 and 2 into Sound 3, where you could place another instance of Midi Mute&Route. Sound 4 could hold another FX chain, and so on...

As an alternative to Automation and Lock States, you could create a whole setup of instant FX pads, which are easily performable and recordable.

## Maschine +

Maschine Plus standalone compatible. Just copy to the SD card to this folder:

/Native Instruments/User Content/Reaktor/Ensembles/

## Feedback and Development

Feedback is appreciated. I am happy to add useful functions and fix bugs. I am still working on the optimal workflow for this plugin and I may change the available routing options in future releases.

Email me at anzbert@gmail.com

## Change Log

- 0.6 - Added an optional Midi note input that ONLY mutes without routing the sound. Updated the UI Style
- 0.5.2 - Set input Midi to Omni by default. Fixed plugin not loading anymore because of Reaktor version mismatch
- 0.5 - Connected Output Bus 2 for optional use of the currently muted signal
- 0.4 - Added an Attack time selector
- 0.3 - Added Invert Button
- 0.2 - First Release
