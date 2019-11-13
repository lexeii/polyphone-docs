# Instrument tools

When an instrument or one of its divisions is selected in the [tree], the
[tool menu] contains several tools sorted in 4 categories:

  - [Analyze]
  - [Fast editing]
  - [Modulators]
  - [Transformation]

Using the tools simultaneously on several instruments is possible (with a multi
selection), except for creating chords, mixtures and for displaying parameters.


<a name="doc_cat_analyze"/>

## Analyze


<a name="doc_display"/>

### Display parameters

This tool displays the evolution of a parameter according to the key.
A logarithmic scale is available (take care of values equal to or less than 0!).

![display parameter tool]


<a name="doc_cat_fast"/>

## Fast editing


<a name="doc_attenuation"/>

### Change attenuations

The tool computes the minimum and the maximum attenuations in all selected
instruments, and gives you the possibility to safely add an offset to all
attenuation values.

For example, if the lowest attenuation of the divisions within the selected
instruments is 16 dB and if the desired minimal attenuation is 5 dB (to increase
the general volume), the attenuation of all divisions of all instruments can be
decreased by 11 dB.

![change attenuation tool]


<a name="doc_detune"/>

### Detune

This feature slightly detunes the instrument notes, so as to create
an undulating effect. The intensity of the effect is adjustable.

![detuning tool]


<a name="doc_global"/>

### Key-based configuration

This tool allows the editing of a parameter for all divisions of an instrument
simultaneously.

![key-based configuration tool]

The graph represents the modification intensity, the first value on the left
corresponding to the change applied to the division comprising the key 0, and
the last value on the right corresponding to the change applied to the division
comprising the key 127. By changing the pattern, it is possible to edit the
curve:

  - manually using the mouse,
  - by using a linear law,
  - by using an exponential law,
  - by using a random generation.

In the case where a linear or exponential law is used, a left click in the graph
defines the beginning of the linear or exponential area, a right click defines
the end.

The parameter to be modified is chosen in “Parameter”, and the modification type
is chosen in “Modification”:

  - **Addition:** the modifier is added to the value of the selected parameter.
  - **Multiplication:** the modifier is multiplied with the value of the
    selected parameter.
  - **Replacement:** the modifier replaces the value of the selected parameter.

It is possible to apply the changes only on divisions whose velocity range is
comprised in a specific range, useful for example in the case where a piano has
several velocity layers.


<a name="doc_release"/>

### Natural release

This tool creates automatically a release for each division of the instrument.
Release times are computed taking into account the first two parameters and a
pitch modification may be added by using the third one.

![natural release tool]


<a name="doc_position"/>

### Sample auto-positioning

The software automatically determines the key ranges of all divisions of an
instrument, in order to optimize their use all over the keyboard.


<a name="doc_spatialization"/>

### Sound spatialization

This feature spatializes sounds according to their pitch, which can be useful
for a piano for example (bass and treble left to right).

![sound spatialization tool]

The bars in the graph represent each a string or pipe, having a length in
relation to the pitch. The shortest bar corresponds to the highest note and the
longest bar corresponds to the lowest note.

Each note is positioned in the space, the far left corresponding to a sound
coming from the left and the extreme right corresponding to a sound coming from
the right. Several patterns can be selected:

  - **Ascending:** trebles are in the left side, basses are in the right side.
  - **Hollow:** basses are at both extremities, trebles are centered.
  - **Descending:** basses are in the left side, trebles are in the right side.
  - **Spike:** trebles are at both extremities, basses are centered.
  - **Random:** trebles and basses are positioned randomly.

Other options are available:

  - number of pattern repetitions (divisions number),
  - intensity of the effect (spreading),
  - filling of a division (filling),
  - offset left - right if the spreading is not 100% (offset),
  - inversions.

The graph is updated every time a setting changes for a better visualization.
On mouse over, the correspondence note number / balance is displayed.


<a name="doc_transpose"/>

### Transpose

The transposition tool allows the transposition of an entire instrument.
The sounds of the instrument are thus the same, but at a different position over
the keyboard.

As input, a shift in terms of semitones is required. For the pitch to be higher,
the shift must be positive. Conversely, for the pitch to be lower the shift must
be negative. The operations performed by the tool, for each division of the
instrument, are then as follows:

  - the root key is adjusted,
  - modification of the fine tuning if the transposition is performed by
    a number of semitones including decimals,
  - shift of the key range according to the number of semitones if “adapt key
    range” is checked.

![transposition tool]


<a name="doc_cat_mod"/>

## Modulators


<a name="doc_default_mod"/>

### Override a default modulator

Default modulators are automatically assigned to every instrument. This tool can
create modulators that will override or disable them.

![overriding tool]


<a name="doc_remove_mod"/>

### Remove modulators

All modulators of all selected instruments will be removed.

**Note:** default modulators will still apply. The only way to disable a default
modulator is to override it with the tool “[Override a default modulator]”.


<a name="doc_cat_transformation"/>

## Transformation


<a name="doc_chords"/>

### Create chords

Based on an instrument, this tool allows you to create all possible chords. This
could be interesting for example for the creation of a choir or pads.

![tool for creating chords]

Here is an example, [before][chord_base.mp3] and [after][chord_done.mp3]:

<audio controls src="../../sounds/chord_base.mp3" type="audio/mpeg"/></audio>
<audio controls src="../../sounds/chord_done.mp3" type="audio/mpeg"/></audio>


<a name="doc_division"/>

### Division duplication

This action has for effect the duplication of all divisions of an instrument.
For example, if a sample linked to an instrument has a key range of 36-38, the
software duplicates this division so as to have 3 times this linked sample for
the key ranges 36-36, 37-37 and 38-38. It makes then possible to thoroughly edit
each sample parameter for each different note, instead of editing whole
divisions with the same parameters.

It is also possible to duplicate the divisions according to velocity ranges.

![division duplication tool]


<a name="doc_mixture"/>

### Mixture creation

Specific to the organ, this tool allows the creation of a mixture from an
existing instrument. An interface appears for specifying the different mixture
divisions, and for each the list of the ranks. Types of possible ranks are very
diverse, ranging from the octave to the 27th harmonic.

![mixture creation tool]

To work, this tool relies on all samples associated to the selected instrument,
the range defined for each sample and the corresponding attenuation. Samples
have to be tuned regardless the definition of the instrument (via the
[sample editor]), and the root key specified must not take into account
membership in a stop (no transposition if the sound is a principal 4' for
example).

An option allows the automatic loop of created samples, another sets the
creation interval of samples. Finally, it is possible to choose the type of the
created sounds: mono or stereo.

Here is an example, [before][mixture_base.mp3] and [after][mixture_done.mp3]:

<audio controls src="../../sounds/mixture_base.mp3" type="audio/mpeg"/></audio>
<audio controls src="../../sounds/mixture_done.mp3" type="audio/mpeg"/></audio>



[Analyze]:                      #doc_cat_analyze
[Fast editing]:                 #doc_cat_fast
[Modulators]:                   #doc_cat_mod
[Transformation]:               #doc_cat_transformation
[Override a default modulator]: #doc_default_mod

[tree]:          /manual/soundfont-editor/tree
[tool menu]:     /manual/soundfont-editor/tools
[sample editor]: /manual/soundfont-editor/editing-pages/sample-editor

[display parameter tool]:       ../../images/tool_display_parameters.png
[change attenuation tool]:      ../../images/tool_change_attenuation.png
[detuning tool]:                ../../images/tool_detune.png
[key-based configuration tool]: ../../images/tool_keybased_configuration.png
[natural release tool]:         ../../images/tool_natural_release.png
[sound spatialization tool]:    ../../images/tool_sound_spatialization.png
[transposition tool]:           ../../images/tool_transpose_inst.png
[overriding tool]:              ../../images/tool_default_mod.png
[tool for creating chords]:     ../../images/tool_create_chords.png
[division duplication tool]:    ../../images/tool_division_duplication.png
[mixture creation tool]:        ../../images/tool_mixture.png

[chord_base.mp3]:               ../../sounds/chord_base.mp3
[chord_done.mp3]:               ../../sounds/chord_done.mp3
[mixture_base.mp3]:             ../../sounds/mixture_base.mp3
[mixture_done.mp3]:             ../../sounds/mixture_done.mp3
