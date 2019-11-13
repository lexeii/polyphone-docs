# Command line

Polyphone can be run with a command line to convert soundfonts in the format
[.sf2], [.sf3] or [.sfz]. Supported file formats for the conversion are [sf2],
[sf3], [sfz] and [sfArk].


<a name="doc_sf2"/>

## Conversion to sf2

### Command line

```bash
polyphone -1 -i [file/to/convert] -d [output/directory] -o [output/file/name]
```

**Note:** with Windows you need to write the full path of Polyphone instead of
just `polyphone`, which is for example
`C:/Program files/Polyphone/polyphone.exe`.


### Arguments

  - `-1`  
    Mode “1” is “convert to sf2”.
  - `-d`  
    Output directory in which the input file will be converted. This argument
    is optional, by default this is the same directory than the input file.
  - `-o`  
    Output name of the converted file without the extension (the extension
    “.sf2” will be automatically added). This argument is optional, by default
    this is the same name than the input file.


### Example

```bash
polyphone -1 -i /path/to/file.sfArk
```


<a name="doc_sf3"/>

## Conversion to sf3


### Command line

```bash
polyphone -2 -i [file/to/convert] -d [output/directory] -o [output/file/name] -c [config]
```

**Note:** with Windows you need to write the full path of Polyphone instead of
just `polyphone`, which is for example
`C:/Program files/Polyphone/polyphone.exe`.


### Arguments

  - `-2`  
    Mode “2” is “convert to sf3”.
  - `-d`  
    Output directory in which the input file will be converted. This argument
    is optional, by default this is the same directory than the input file.
  - `-o`  
    Output name of the converted file without the extension (the extension
    “.sf3” will be automatically added). This argument is optional, by default
    this is the same name than the input file.
  - `-c`  
    Conversion configuration. It is possible to specify the compression quality:
    “0” is low, “1” is medium, “2” is high. This argument is optional, by
    default this is “1” (medium quality).


### Example

```bash
polyphone -2 -i /path/to/file.sf2 -c 2
```


<a name="doc_sfz"/>

## Conversion to sfz


### Command line

```bash
polyphone -3 -i [file/to/convert] -d [output/directory] -o [output/file/name] -c [config]
```

**Note:** with Windows you need to write the full path of Polyphone instead of
just `polyphone`, which is for example
`C:/Program files/Polyphone/polyphone.exe`.


### Arguments

  - `-3`  
    Mode “3” is “convert to sfz”.
  - `-d`  
    Output directory in which the input file will be converted. This argument
    is optional, by default this is the same directory than the input file.
  - `-o`  
    Output name of the converted file without the extension (the extension
    “.sfz” will be automatically added). This argument is optional, by default
    this is the same name than the input file.
  - `-c`  
    Conversion configuration made of 3 characters. The first character is “1” if
    each preset must be prefixed by its preset number, “0” otherwise. The second
    character is “1” if a directory per bank must be created, “0” otherwise.
    The third character is “1” if the general midi classification must be used
    to sort presets, “0” otherwise. This argument is optional, by default this
    is “000”.


### Example

```bash
polyphone -3 -i /path/to/file.sf3 -c 011
```



[.sf2]: #doc_sf2
[.sf3]: #doc_sf3
[.sfz]: #doc_sfz

[sf2]:   the-different-soundfont-formats.md#doc_sf2
[sf3]:   the-different-soundfont-formats.md#doc_sf3
[sfz]:   the-different-soundfont-formats.md#doc_sfz
[sfArk]: the-different-soundfont-formats.md#doc_sfark
