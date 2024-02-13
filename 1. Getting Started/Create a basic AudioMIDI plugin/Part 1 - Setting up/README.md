Followed the initial tutorial and got the new project created.

Got the new project launched in VS22

Was unable to get the project to successfully build
    
    -Issues:

        ProJucer Settings needed to be set to have the tick box for VST3 & Standalone checked in Plugin Formats

        Once Standalone was added to the project you need to modify the "Startup Project" In vs22 to use StandalonePlugin and not the default VST3
            -To do this you right click on the Solution "ProjectName" at the top of the solution explorer and select properties
            -Select "ProjectName"_StandalonePlugin under Single startup project in the Startup Project section of the Common Properties 

Solution found here: https://forum.juce.com/t/error-message-is-not-a-valid-win32-application-on-audio-application-project/29272/7 

As mentioned by xenakios "The project needs to be set as the “startup project” in Visual Studio in that case but I think Projucer sets that automatically when the standalone application wrapper is added into the build configuration."


More confusion on the tutorial description.  In "Set up plug-in debugging (Optional) the "To access the host go to" means that the projucer project that contains the Plug-In Host is in the default install location where you have JUCE located.  for me it was in F:\Juce Library\JUCE
There was confusion as I didn't inference what they meant with just the pathing.

Next issue is when you run/debug the PlugInHost and select the vst3 from the tutorial project it loads to 7% and hits a breakpoint about JUCE_ASSERT_MESSAGE_THREAD 
    FIX: Seems removing one of the default VST3 Plugin paths solves the crash. 
        -Wanted to add the original path however I am unable to get the path to come back to run further tests after removing.   I am going to assume that the path was the "C:\Program Files\Common Files\VST3 as discussed in the tutorial. 

