# Projucer Tutorials - Part 2: Coding Your Plug-in

## Summary

This section continues the "Create a Basic Audio/MIDI Plugin" tutorial, focusing on coding your plug-in. The primary emphasis is on modifying the `PluginProcessor` and `PluginEditor` files located in the SharedCode > ("PluginName") > Source directory.

## Key Points

- **PluginProcessor Considerations:**
  - `PluginProcessor` is best considered the parent of the editor, and most changes for audio processing are made here.

- **File Locations:**
  - `PluginEditor.cpp/.h` and `PluginProcessor.cpp/.h` are located in SharedCode > ("PluginName") > Source.

- **Slider Implementation:**
  - Implemented a slider using `juce::Slider ("variableName")`.
  - `juce::Slider` offers various options, including setting ranges, values, and slider styles.
  - TODO: Explore different options for sliders.

- **PluginEditor Modifications:**
  - Successfully modified `PluginEditor` to display and manipulate the slider easily.

- **MIDI Signal Changes:**
  - Uncertain about observing MIDI signal changes after setting up the "Modify MIDI notes" section of the tutorial.
    - Attempted running both the plug-in and standalone versions without success.
    - Toggled various values of the slider and clicked the piano keys on the plugin without visible changes.
    - Reread the tutorial section to verify correct implementation.
  
  - **FIX:** Modified the MIDI output device from SSL2+ Audio Interface to Microsoft GS Wavetable Synth. This adjustment allowed for sound changes based on the MIDI Volume slider in the plugin.

These notes highlight the key aspects of coding your plug-in, including modifications to the `PluginProcessor` and `PluginEditor` files, slider implementation, and addressing issues with MIDI signal changes.
