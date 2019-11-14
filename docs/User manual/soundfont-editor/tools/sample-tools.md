# Sample tools

When one or more samples are selected in the [tree], the [tool menu] contains
several tools sorted in 4 categories:

  - [Analyze]
  - [Files]
  - [Sample processing]
  - [Stereo samples]

Using the tools simultaneously on several samples is possible (with a multi
selection).


<a name="doc_cat_analyze"/>

## Analyze


<a name="doc_peakfrequencies"/>

### Show peak frequencies

This tool gathers the information on the peak frequencies of all selected
samples, and the results can be exported in a .csv file. The peak frequencies
are visible in the editing page of [samples][sample frequency].

![show peak frequencies]


<a name="doc_cat_files"/>

## Files


<a name="doc_wavexport"/>

### Wav export

After having selected a destination directory, all selected samples will be
exported as .wav files.


<a name="doc_cat_processing"/>

## Sample processing


<a name="doc_autoloop"/>

### Auto loop

The software seeks a stable area of the sample and then artificially creates
a loop. A sound segment is copied with a cross-fade, so that the transition at
the join location is as smooth as possible.

To assign loop points automatically:

  - click in the [tree] on the sample to be looped,
  - in the editing page of [samples]:
    - position the start and end of the loop in the graphic (WAV display area)
      around a stable area, or
    - let the tool determine automatically a stable area by defining 0 as loop
      start and loop end,
  - in the “Tools” menu select “Sample”, “Auto loop”,
  - press the Play button with the loop option checked,
  - if the loop points found are not suitable you can [undo] the operation, try
    repositioning them manually around a stable area and then use the “Auto
    loop” function again.

The tool needs to find a stable area of more than 0.25 seconds. If it fails, a
warning message appears indicating that no loop can be found. In this case it is
possible to specify manually a stable area of more than 0.25 seconds and retry
the tool, or try to find the loop points manually.

**Warning:** This tool modifies the original sample. Modifications can be undone
via the “[undo]” function, but if the file is saved and Polyphone is closed
there is no way to step back.

**Note:** By default, the looping is disabled in an instrument. To hear it, you
must select ![loop on] in the Loop playback parameter row of either the Global
or individual notes columns in the Parameters Table. ![loop on] turns it On,
![loop off] turns it Off. ![loop on + end] turns the looping On and the sample
will play to the end after a key is released.


<a name="doc_volume"/>

### Change volume

You can change the volume in three different ways:

  - in adding a certain amount of dB (positive or negative amount),
  - in multiplying the signal by a number,
  - in normalizing the signal so that the maximum of this signal represents some
    percentage of the maximum intensity.

![Change volume tool]


<a name="doc_externalcommand"/>

### External command

This tool allows you to use an external command or program to edit a sample.
You don't need to export and re-import a sample into Polyphone anymore,
everything is done automatically:

  - download an editing software for wav files such as audacity or sweep
    (linux),
  - use the tool “External command” for one or more samples,
  - fill the command line in the right field to call the external software (you
    may need to read the documentation of this software),
  - edit the sample(s) with the external tool,
  - save the modified version of the wav file(s) with the external tool and
    close it,
  - the sample(s) will be automatically loaded into the soundfont.

![External command tool]

<a name="doc_filter"/>

### Filter frequencies

When you use this tool, a window will be displayed showing the frequencies
contained in the sample(s) you selected. You can then use the mouse to draw a
red area. Everything that is in this area will be removed: this means that you
can manually decrease of remove some frequencies.

![Filter frequency tool]

**Note:** this filter is not common since it cuts frequencies in a hard way.
This tool can be useful to design a brick-wall filter but in most cases you will
probably want to use the [equalizer].


<a name="doc_removeblank"/>

### Remove blank at start

Any blank area before the sample begins is eliminated. This reduces the time
before the sound is heard.

![Remove blank at start]

**Note:** this tool may be applied automatically each time a sample is imported,
according to the software [preferences][settings general].


<a name="doc_transpose"/>

### Transpose

The tool asks for a shift in semitones and then re-samples the sound to change
the pitch.

![Transpose tool]


<a name="doc_trimloop"/>

### Trim to end of loop

If a loop is defined for the selected sample, the software will cut the sound
after the end of the loop (leaving a small margin at the end).

![Trim to loop]

**Note:** this tool may be applied automatically each time a sample is imported,
according to the software [preferences][settings general].


<a name="doc_cat_stereo"/>

## Stereo samples


<a name="doc_balance"/>

### Balance adjustment

If the sample is linked to another one (stereo), the software can equalize the
mean intensity of the two samples to adjust the balance. This will then be
easier to accurately pan a sample in an [instrument].


<a name="doc_link"/>

### Link all stereo samples

Among the selected samples, samples whose names only differ by the last letter
(R / L) are automatically linked. For example, if in a soundfont two samples are
called `bassoon45L` and `bassoon45R`, `bassoon45L` will be recognized as the
left part of `bassoon45R` and `bassoon45R` will be recognized as the right part
of `bassoon45L`.

With this information the right panning will be used when these samples are
added in an instrument. You can also enjoy the simultaneous editing of left and
right parts in the instrument [table] if the stereo editing is activated in the
[settings][settings general].

**Warning:** this tool can break existing links if the names don't match the
rule above.


<a name="doc_unlink"/>

### Unlink all stereo samples

All selected samples that are linked (stereo) are unlinked.

Thus, all samples will be processed as mono sounds and they will all have the
same panning if they are added in an instrument. The stereo editing, if
activated in the [settings][settings general], will not be applicable anymore.



[Analyze]:           #doc_cat_analyze
[Files]:             #doc_cat_files
[Sample processing]: #doc_cat_processing
[Stereo samples]:    #doc_cat_stereo

[tree]:             ../tree.md
[tool menu]:        index.md
[samples]:          ../editing-pages/sample-editor.md
[sample frequency]: ../editing-pages/sample-editor.md#doc_freq
[equalizer]:        ../editing-pages/sample-editor.md#doc_eq
[instrument]:       ../editing-pages/instrument-editor.md
[table]:            ../editing-pages/instrument-editor.md#doc_table
[undo]:             ../toolbar.md#doc_edit
[settings general]: ../../settings.md#doc_general

[show peak frequencies]: ../../images/tool_show_peak_frequencies.png
[loop on]:               ../../images/loop_on.png
[loop off]:              ../../images/loop_off.png
[loop on + end]:         ../../images/loop_on_end.png
[Change volume tool]:    ../../images/tool_change_volume.png
[External command tool]: ../../images/tool_external_command.png
[Filter frequency tool]: ../../images/tool_filter_frequencies.png
[Remove blank at start]: ../../images/remove_blank.png
[Transpose tool]:        ../../images/tool_transpose_smpl.png
[Trim to loop]:          ../../images/trim_to_loop.png
