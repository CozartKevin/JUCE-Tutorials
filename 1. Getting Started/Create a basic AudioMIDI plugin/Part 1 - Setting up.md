# Projucer Tutorials - Part 1: Setting Up a Basic Audio/MIDI Plugin

## Summary

This section documents the initial steps taken in "Part 1 - Setting Up a Basic Audio/MIDI Plugin." It emphasizes creating a new Projucer project, launching it in Visual Studio 2022, and exploring project files.

## Key Points

- **New Projucer Project:**
  - Followed tutorial instructions to create a new Projucer project.

- **Target IDE:**
  - Set the target IDE to Visual Studio 2022.

- **Project Launch:**
  - Successfully launched the project using the provided directions.

- **Opening via .jucer File:**
  - Opened the project using the .jucer file.

- **PIP File Creation:**
  - Created a generic PIP file to understand its structure, addressing the absence of PIP files.

- **Documentation Tracking:**
  - Established a "Terms" document in the main folder to track new information, especially concerning PIP files.

- **Understanding PIP Files:**
  - Referenced the website, clarifying that PIP files are header files with the .h extension. They provide metadata to the Projucer for automatic project creation with correct modules and exporters.

- **Project Continuation:**
  - Moved GUI_Project files to Part 2 for the tutorial's continuation. (Note: Continued in Part 2)

## Follow-up Actions

- **Build Issues:**
  - Encountered issues with the project build, needing adjustments in ProJucer Settings. VST3 & Standalone checkboxes needed to be enabled in Plugin Formats.

  - Set the "Startup Project" in VS22 to use StandalonePlugin instead of the default VST3. This resolved the "not a valid Win32 application" error.

    - To set the startup project in Visual Studio, right-click on the solution in the Solution Explorer, choose properties, and under Common Properties, select "ProjectName"_StandalonePlugin as the Single startup project.

  - Referenced solution: [Forum Discussion](https://forum.juce.com/t/error-message-is-not-a-valid-win32-application-on-audio-application-project/29272/7)

- **Plug-In Debugging Setup:**
  - Experienced confusion in locating the Plug-In Host mentioned in the tutorial. Found it in the default install location of JUCE.

- **Plug-In Host Debugging Issues:**
  - Encountered a breakpoint about JUCE_ASSERT_MESSAGE_THREAD when loading the VST3 in the PlugInHost.
  
    - Fix: Removing one of the default VST3 Plugin paths solved the crash. The original path assumed to be "C:\Program Files\Common Files\VST3" as discussed in the tutorial.

  - Adjusted project debug settings to resolve the crash, setting back to "Current Selection" and selecting the Plugin Host in the JUCE folder as the executable.

These adjustments ensure a smoother setup for developing a basic Audio/MIDI plugin with JUCE.
