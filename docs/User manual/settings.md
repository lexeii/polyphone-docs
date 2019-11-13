# Settings

The software preferences are accessible either from the [home screen] or from
the [menu]. They are divided into five sections:

  - [General]
  - [Interface]
  - [Sound]
  - [Virtual keyboard]
  - [Online repository]


<a name="doc_general"/>

## General

The “General” section allows the modification of the following parameters:

  - **Audio back-end**  
    Specifies the audio back-end used to play samples. Jack and Asio drivers
    (the latter for Windows only) may be chosen.
  - **Buffer size**  
    Specifies the buffer size used for Jack and Asio drivers. A small buffer
    results in a small latency, but the sound may become scratchy.
  - **Midi input**  
    Specifies the midi input controlling the virtual keyboard.

Moreover, it is possible to check the following options:

  - **Sample import: trim to loop**  
    When importing a sample, data located after the end of loop are
    automatically removed (same effect as the tool “[Trim to end of loop]”).
  - **Wav file import: remove blank at start**  
    When importing a sample, any blank area located before the beginning of the
    attack is automatically removed (same effect as the tool
    “[Remove blank at start]”).
  - **Stereo editing: change linked sample**  
    When editing one side of a stereo sample, the other side is automatically
    edited the same. The same applies when editing a stereo instrument division:
    the division corresponding to the other channel (with the same note and
    velocity ranges) is edited the same.

![settings, general]


<a name="doc_interface"/>

## Interface

This section shows options related to the interface of the software:

  - **Language**  
    The language may be changed here (a restart of the software is required).
  - **Key names**  
    Keys may be named depending on their number (according to MIDI
    specification), or depending on the name of middle C (C3, C4 or C5). Key
    names may comprise sharps or flats.
  - **Sort divisions**  
    The division order within an instrument or a preset can be changed here.
  - **Decorations**  
    Background decorations in some lists can be deactivated for readability.
  - **Color theme**  
    Different predefined color themes are available for customizing the
    appearance of Polyphone. A manual selection of colors is also possible.

![settings, interface]


<a name="doc_sound"/>

## Sound

The “Sound” section makes it possible to modify the chorus and reverb of the
synth, along with its global volume. The global volume may be changed with the
volume MIDI controller if an external keyboard is connected.

![settings, sound]


<a name="doc_keyboard"/>

## Keyboard

The keys of the computer keyboard used to control the [virtual keyboard] are
defined in the “Keyboard” section. The pitch may be increased or decreased
octave by octave.

![settings, keyboard]


<a name="doc_repository"/>

## Repository

Identifiers can be entered here to link Polyphone with an account, a Premium
account unlocking the [soundfont browser].

The download directory used by the [soundfont browser] can be changed here.

![settings, repository]



[General]:           #doc_general
[Interface]:         #doc_interface
[Sound]:             #doc_sound
[Virtual keyboard]:  #doc_keyboard
[Online repository]: #doc_repository

[home screen]:           /manual
[menu]:                  /manual/menu#doc_shortcuts
[Trim to end of loop]:   /manual/soundfont-editor/tools/sample-tools#doc_trimloop
[Remove blank at start]: /manual/soundfont-editor/tools/sample-tools#doc_removeblank
[virtual keyboard]:      /manual/soundfont-editor/toolbar#doc_keyboard
[soundfont browser]:     /manual/soundfont-browser

[settings, general]:    images/settings_general.png
[settings, interface]:  images/settings_interface.png
[settings, sound]:      images/settings_sound.png
[settings, keyboard]:   images/settings_keyboard.png
[settings, repository]: images/settings_repository.png
