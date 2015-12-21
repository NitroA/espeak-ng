5. VOICES {.western}
---------

### 5.1 Voice Files {.western}

A Voice file specifies a language (and possibly a language variant or
dialect) together with various attributes that affect the
characteristics of the voice quality and how the language is spoken.

Voice files are placed in the `espeak-data/voices`{.western} directory,
or within subdirectories in there.

The available voice files can be listed by:

~~~~ {.western}
   espeak-ng --voices
or
   espeak-ng --voices=<language>
~~~~

also

~~~~ {.western style="margin-bottom: 0.5cm"}
   espeak-ng --voices=<variant>
~~~~

Lists voice variants which can be applied to eSpeak voices.

~~~~ {.western style="margin-bottom: 0.5cm"}
   espeak-ng --voices=<mbrola>
~~~~

Lists the Mbrola voices.

### 5.2 Contents of Voice Files {.western}

The **language** attribute is mandatory. All the other attributes are
optional.

#### Identification Attributes {.western}

**name  \<name\>**

A name given to this voice.

**language  \<language code\> [\<priority\>]**

This attribute should appear before the other attributes which are
listed below.

It selects the default behaviour and characteristics for the language,
and sets default values for "phonemes", "dictionary" and other
attributes. The \<language code\> should be a two-letter ISO 639-1
language code. One or more language variant codes may be appended,
separated by hyphens. (eg. en-uk-north).

The optional \<priority\> value gives the preference of this voice
compared with others for the specified language. A low value indicates a
more preferred voice. The default value is 5.

More than one **language** line may be present. A voice may be selected
for other related languages (variants which have the same initial 2
letter language code as the specified language), but it will be less
preferred for these. Different language variants may be specified by
additional **language** lines in order to indicate that this is a
preferred voice for them also. Eg.

~~~~ {.western}
   language en-uk-north
   language en
~~~~

indicates that this is voice is for the "en-uk-north" dialect, but it is
also a main choice when a general "en" language is specified. Without
the second **language** line, it would be disfavoured for "en" for being
a more specialised voice.

**gender  \<gender\> [\<age\>]**

This attribute is only a label for use in voice selection. It doesn't
change the sound of the voice.

\<gender\> may be male, female, or unknown.\
 \<age\> is optional and gives an age in years.

**pitch  \<base\> \<range\>**

Two integer values. The first gives a base pitch to the voice (value in
Hz) The second controls the range of pitches used by the voice. Setting
it equal to the base pitch will give a monotone. The default values are
82 118.

**formant  \<number\> \<frequency\> \<strength\> \<width\>
\<freq\_add\>**

Systematically adjusts the frequency, strength, and width of the
resonance peaks of the voice. Values are percentages of the default
values. Changing these affects the tone/quality of the voice.

**freq\_add**Adds a constant value (in Hz) to the frequency of the
formant peak. The value may be negative.

-   -   -   -   

**echo  \<delay\> \<amplitude\>**

Parameter 1 gives the delay in mS (0 to 250mS).\
 Parameter 2 gives the echo amplitude (0 to 100).\
 Adding some echo can give a clearer or more interesting sound,
especially when listening through a domestic stereo sound system, rather
than small computer speakers.

**tone**

Controls the tone of the sound.\
 **tone** is followed by up to 4 pairs of \<frequency\> \<amplitude\>
which define a frequency response graph. Frequency is in Hz and
amplitude is in the range 0 to 255. The default is:

`  `{.western}`tone 600         170  1200 135  2000 110`{.western}

This means that from frequency 0Hz to 600Hz the amplitude is 170. From
600Hz to 1200Hz the amplitude decreases from 170 to 135, then decreases
to 110 at 2000Hz and remains at 110 at higher frequencies. This
adjustment applies only to voiced sounds such as vowels and sonorant
consonants (such as [n] and [l]). Unvoiced sounds such as [s] are
unaffected.

This **tone** statement can also appear in
`espeak-data/config`{.western}, in which case it applies to all voices
which don't have their own **tone** statement.

**flutter  \<value\>**

Default value: 2.\
 Adds pitch fluctuations to give a wavering or older-sounding voice. A
large value (eg. 20) makes the voice sound "croaky".

**roughness  \<value\>**

Default value: 2. Range 0 - 7\
 Reduces the amplitude of alternate waveform cycles in order to make the
voice sound creaky.

**voicing  \<value\>**

Default value: 100.\
 Adjusts the strength of formant-synthesized sounds (vowels and sonorant
consonants).

**consonants  \<value\> \<value\>**

Default values: 100, 100.\
 Adjusts the strength of noise sounds which are used in consonants. The
first value is the strength of unvoiced consonants such as "s" and "t".
The second value is the strength of the noise component of voiced
consonants such as "z" and "d".

**breath  \<up to 8 integer values\>**

Default values: 0.\
 Adds noise which corresponds to the formant frequency peaks. The values
give the strength of noise for each formant peak (formants 1 to 8).

Use together with a low or zero value of the **voicing** attribute to
make a "wisper". For example:\

`breath           75 75 60 40 15 10 breathw  150 150 200 200 400         400 voicing  18 flutter  20 formant           0 100 0 100   // remove formant 0 `{.western}

**breathw  \<up to 8 integer values\>**

These values give bandwidths of the noise peaks of the **breath**
attribute. If **breathw** values are not given, then suitable default
values will be used.

**speed  \<value\>**

Default value 100.\
 Adjusts the speaking speed by a percentage of the default rate. This
can be used if a language voice seems faster or slower compared to other
voices.

**phonemes  \<name\>**

Specifies which set of phonemes to use from those contained in the
phontab, phonindex, and phondata data files. This is a **phonemetable**
name as given in the "phoneme" source file.

This parameter is usually not needed as it is set by default to the
first two letters of the "language" parameter. However, different voices
of the same language can use different phoneme sets, to give different
accents.

**dictionary  \<name\>**

Specifies which pair of dictionary files to use. eg. "english" indicates
that *speak-data/en\_dict* should be used to translate from words to
phonemes. This parameter is usually not needed as it is set by default
to the first two letters of "language" parameter.

**dictrules  \<list of rule numbers\>**

Gives a list of conditional dictionary rules which are applied for this
voice. Rule numbers are in the range 0 to 31 and are specific to a
language dictionary. They apply to rules in the language's **\_rules**
dictionary file and also its **\_list** exceptions list. See
[dictionary.html](dictionary.html).

**replace  \<flags\> \<phoneme\> \<replacement phoneme\>**

Replace a phoneme by another whenever it occurs.

\<replacement phoneme\> may be NULL.

Flags: bit 0: replacement only occurs on the final phoneme of a word.\
 Flags: bit 1: replacement doesn't occur in stressed syllables.\
 eg.

~~~~ {.western}
      replace  0  h  NULL      // drops h's
      replace  0  V  U         // replaces vowel in 'strut' by that in 'foot'
                               // as occurs in northern British English
      replace  3  N  n         // change 'fishing' to 'fishin' etc.
                               // (only the last phoneme of a word, only in unstressed syllables)
~~~~

The phoneme mnemonics can be defined for each language, but some are
listed in [phonemes.html](phonemes.html)

**stressLength  \<8 integer values\>**

Eight integer parameters. These control the relative lengths of the
vowels in stressed and unstressed syllables.

-   -   -   -   -   -   -   -   

**stressAdd  \<8 integer values\>**

Eight integer parameters. These are added to the voice's corresponding
stressLength values. They are used in the voice variant files in
`espeak-data/voices/!v`{.western} to give some variety. Negative values
may be used.

**stressAmp  \<8 integer values\>**

Eight integer parameters. These control the relative amplitudes of the
vowels in stressed and unstressed syllables (see stressLength above).
The general default values are: 16, 16, 20, 20, 20, 24, 24, 22, although
these defaults may be different for particular languages.

**intonation  \<param1\>**

-   -   -   -   

**charset  \<param1\>**

The ISO 8859 character set number. (not all are implemented).

**dictmin  \<value\>**

Used for some languages to detect if additional language data is
installed. If the size of the compiled dictionary data for the language
(the file `espeak-data/*_dict`{.western}) is less than this size then a
warning is given.

**alphabet2  \<alphabet\> \<language\>**

Used to specify a language to be used to speak words which are written
in a non-native alphabet. eg:

~~~~ {.western style="margin-bottom: 0.5cm"}
 alphabet2 cyr ru
~~~~

Alphabets names include: latin, cyr (cyrillic), ar (arabic). The default
language for latin alphabet is English.

**dictdialect  \<dialect\>**

Words can be marked in the \*\_list or \*\_rules file to be spoken using
a foreign voice. This **dictdialect** attribute can be used to specify
which dialect of the foreign language should be used, instead of the
default dialect. The currently available dialects are:\
 **en-us** (US English)\
 **es-la** (Latin American Spanish).\
 eg.

~~~~ {.western style="margin-bottom: 0.5cm"}
 dictdialect en-us
~~~~

This means that any words or rules which are maked with \_\^\_EN will be
spoken with the US English voice instead of the default UK English
voice.

Additional attributes are available to set various internal options
which control how language is processed. These would normally be set in
the program code rather than in a voice file.

A number of Voice files are provided in the
`espeak-data/voices`{.western} directory. You can select one of these
with the **-v \<voice filename\>** parameter to the speak command.

**default**

This voice is used if none is specified in the speak command. You can
copy your preferred voice to "default" so you can use the speak command
without the need to specify a voice.

For a list of voices provided for English and other languages see
[Languages](languages.html).
