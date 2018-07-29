# Bridge

Rack is a standalone DAW-like application and not a VST/AU plugin because of the major limitations of these formats.
It is common to think of physical modular synthesizers as entire self-contained DAWs, so many people use Rack as a complete DAW to compose music and build patches without other software.

However, *VCV Bridge* allows audio, MIDI, DAW transport, and DAW clocks to be transferred between Rack and your DAW through the included VST/AU instrument/effect Bridge plugins.

The setup order between Rack and your DAW does not matter.

## Setting up Bridge in Rack

- Add an Audio or MIDI module to Rack from the [Core](Core.html) plugin, and select "Bridge" from the driver dropdown list.
- Open the device menu to select the Bridge port.

Up to 8 channels of audio entering the Bridge effect plugin are routed to the INPUT section of the Audio module in Rack and then back to the effect plugin.

The 16 automation parameters in the VST/AU Bridge plugin simply generate MIDI-CC messages 0-15, so you can use a [Core MIDI-CC](Core.html#midi-cc) interface to convert them to 0-10 V signals in Rack.

## Setting up Bridge in your DAW

- Make sure the VST or AU Bridge plugin is installed, and launch your DAW.
- Add the "VCV Bridge" instrument or "VCV Bridge fx" effect plugin to a track.
	- The instrument plugin is easier for sending MIDI to Rack, although it also supports audio input if supported by your DAW.
	- The effect plugin is easier for sending audio to Rack, although it also supports MIDI input if supported by your DAW.
- Open the plugin parameters to reveal the Bridge port setting and 16 automation parameters.

### Ableton Live

Add a "VCV-Bridge" plugin to a MIDI track and open the automation parameters by clicking the triangle icon next to the plugin's name.
*Bridge* will send MIDI and receive audio from Rack.

To send audio to Rack, select the Bridge's track under the "Audio To" menu on another track, and optionally select the channel pair (1/2, 3/4, 5/6, or 6/7).

To record audio from Rack, create a new audio track and select the Bridge's track and optionally the channel pair under the "Audio From" menu.
Make sure "Monitor" is set to "In" on the Bridge's track to enable audio output even when it is not record-enabled.

![Ableton Live VCV Bridge](images/BridgeLive.png)

### Cubase
TODO

### FL Studio
TODO

### Propellerhead Reason
Launch VCV Rack first, switch its audio output device to Bridge, and then launch Reason and instantiate Bridge as a VST.

### REAPER
TODO
