# VCV Bridge

Rack is a standalone DAW-like application and not a VST/AU plugin because of the major limitations of these formats.
It is common to think of physical modular synthesizers as entire self-contained DAWs, and many people use Rack as a complete DAW to compose music and build patches without other software.

However, *VCV Bridge* allows audio and MIDI to be transferred between Rack and your DAW through the included VST/AU Bridge plugin.
Currently VCV Bridge is only a VST/AU effect plugin (Mac and 32/64-bit Windows) for using Rack as a send/return on a DAW track.

*Note: VSTi/AU instrument plugins, MIDI, and DAW clock transport are coming soon in a later Rack 0.6.x update.*

The setup order between Rack and your DAW does not matter.

### Setting up Bridge in Rack

- Add an Audio or MIDI module to Rack from the [Core](Core.md) plugin, and select "Bridge" from the driver dropdown list.
- Open the device menu to select the Bridge port.

Up to 8 channels of audio entering the Bridge effect plugin are routed to the INPUT section of the Audio module in Rack and then back to the effect plugin.

The 16 automation parameters in the VST/AU Bridge plugin simply generate MIDI-CC messages 0-15, so you can use a [Core MIDI-CC](Core.md#midi-cc) interface to convert them to 0-10 V signals in Rack.

### Setting up Bridge in your DAW

- Make sure the VST or AU Bridge plugin is installed, and launch your DAW.
- Add the "VCV Bridge" effect plugin to an audio track.
- Open the plugin parameters (e.g. by clicking the plugin's triangle arrow in Ableton Live) to reveal the Bridge port setting and 16 automation parameters.

#### Ableton Live
TODO

#### Cubase
TODO

#### FL Studio
TODO

#### BandLab Sonar
TODO

#### Propellerhed Reason
TODO

#### Propellerhead Reason
TODO

#### REAPER
TODO
