Continuation of the Create a basic AudioMIDI plugin
    -PluginProcessor is best considered Parent aof the editor.  Make most changes for audio processing here.

PluginEditor .cpp/.h & PluginProcessor .cpp/.h are in the SharedCode > ("PluginName") > Source location

Slider call is juce::Slider ("variableName")
    juce:slider as a meriad of options including Setting ranges, values, sliderstyle.  
        TODO: Look into different options for sliders. 
PluginEditor modifications successful.
Was able to easily see the slider and manipulate it. 