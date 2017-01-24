# Phonemes

- [Consonants](#consonants)
  - [Other Symbols](#other-symbols)
  - [Gemination](#gemination)
  - [Manner of Articulation](#manner-of-articulation)
  - [Place of Articulation](#place-of-articulation)
  - [Voice](#voice)
- [Vowels](#vowels)
  - [Rounding](#rounding)
  - [Height](#height)
  - [Backness](#backness)
- [Diacritics](#diacritics)
  - [Articulation](#articulation)
  - [Air Flow](#air-flow)
  - [Phonation](#phonation)
  - [Rounding and Labialization](#rounding-and-labialization)
  - [Syllabicity](#syllabicity)
  - [Consonant Release](#consonant-release)
  - [Co-articulation](#co-articulation)
  - [Tongue Root](#tongue-root)
  - [Fortis and Lenis](#fortis-and-lenis)
- [Suprasegmentals](#suprasegmentals)
  - [Stress](#stress)
  - [Length](#length)
  - [Rhythm](#rhythm)
  - [Intonation](#intonation)
  - [Tone Stepping](#tone-stepping)
  - [Tones](#tones)
- [References](#references)

----------

Evan Kirshenbaum created an ASCII transcription of the International Phonetic
Alphabet (IPA)<sup>\[<a href="#ref1">1</a>\], \[<a href="#ref2">2</a>\]</sup>.
As well as using ASCII characters for specific IPA phonemes, this transcription
provides a set of 3-letter feature abbreviations allowing a phoneme to be
described as a sequence of features.

This document extends Evan Kirshenbaum's feature set to be able to describe the
different phonemes in the IPA and as are used in the various languages of the
world.

The goal of this document is not to provide a detailed guide on phonetics. Nor
is it intended to be able to accurately record differences in IPA diacritics.
Instead, it is designed to be a transcription guide for authors of espeak-ng
languages and voices on how to specify phonemes so that the IPA and feature
transcriptions are consistent.

__NOTE:__ This model is in the process of being implemented. As such, the
current implementation does not reflect this document.

## Consonants

<table>
  <tr>
    <td></td>
    <th colspan="2"><code>blb</code></th>
    <th colspan="2"><code>lbd</code></th>
    <th colspan="2"><code>dnt</code></th>
    <th colspan="2"><code>alv</code></th>
    <th colspan="2"><code>pla</code></th>
    <th colspan="2"><code>rfx</code></th>
    <th colspan="2"><code>alp</code></th>
    <th colspan="2"><code>pal</code></th>
    <th colspan="2"><code>vel</code></th>
    <th colspan="2"><code>uvl</code></th>
    <th colspan="2"><code>phr</code></th>
    <th colspan="2"><code>glt</code></th>
  </tr>
  <tr>
    <th align="right"><code>nas</code></th>
    <td>m̥</td><td>m</td>
    <td> </td><td>ɱ</td>
    <td> </td><td> </td>
    <td>n̥</td><td>n</td>
    <td> </td><td> </td>
    <td>ɳ̊</td><td>ɳ</td>
    <td>ɲ̟̊</td><td>ɲ̟</td>
    <td>ɲ̊</td><td>ɲ</td>
    <td>ŋ̊</td><td>ŋ</td>
    <td>ɴ̥</td><td>ɴ</td>
    <td> </td><td> </td>
    <td> </td><td> </td>
  </tr>
  <tr>
    <th align="right"><code>stp</code></th>
    <td>p</td><td>b</td>
    <td>p̪</td><td>b̪</td>
    <td> </td><td> </td>
    <td>t</td><td>d</td>
    <td> </td><td> </td>
    <td>ʈ</td><td>ɖ</td>
    <td> </td><td> </td>
    <td>c</td><td>ɟ</td>
    <td>k</td><td>ɡ</td>
    <td>q</td><td>ɢ</td>
    <td>ʡ</td><td> </td>
    <td>ʔ</td><td> </td>
  </tr>
  <tr>
    <th align="right"><code>sib</code>&#xA0;<code>afr</code></th>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td>t͡s</td><td>d͡z</td>
    <td>t͡ʃ</td><td>d͡ʒ</td>
    <td>ʈ͡ʂ</td><td>ɖ͡ʐ</td>
    <td>t͡ɕ</td><td>d͡ʑ</td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
  </tr>
  <tr>
    <th align="right"><code>afr</code></th>
    <td>p͡ɸ</td><td>b͡β</td>
    <td>p̪͡f</td><td>b̪͡v</td>
    <td>t͡θ</td><td>d͡ð</td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td>c͡ç</td><td>ɟ͡ʝ</td>
    <td>k͡x</td><td>ɡ͡ɣ</td>
    <td>q͡χ</td><td>ɢ͡ʁ</td>
    <td>ʡ͡ħ</td><td>ʡ͡ʕ</td>
    <td>ʔ͡h</td><td></td>
  </tr>
  <tr>
    <th align="right"><code>lat</code>&#xA0;<code>afr</code></th>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td>t͡ɬ</td><td>d͡ɮ</td>
    <td> </td><td> </td>
    <td>ʈ͡ɭ̊˔</td><td> </td>
    <td> </td><td> </td>
    <td>c͡ʎ̥˔</td><td> </td>
    <td>k͡ʟ̝̊</td><td>ɡ͡ʟ̝</td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
  </tr>
  <tr>
    <th align="right"><code>sib</code>&#xA0;<code>frc</code></th>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td>s</td><td>z</td>
    <td>ʃ</td><td>ʒ</td>
    <td>ʂ</td><td>ʐ</td>
    <td>ɕ</td><td>ʑ</td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
  </tr>
  <tr>
    <th align="right"><code>frc</code></th>
    <td>ɸ</td><td>β</td>
    <td>f</td><td>v</td>
    <td>θ</td><td>ð</td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td>ç</td><td>ʝ</td>
    <td>x</td><td>ɣ</td>
    <td>χ</td><td>ʁ</td>
    <td>ħ</td><td>ʕ</td>
    <td>h</td><td>ɦ</td>
  </tr>
  <tr>
    <th align="right"><code>lat</code>&#xA0;<code>frc</code></th>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td>ɬ</td><td>ɮ</td>
    <td> </td><td> </td>
    <td>ɭ̊˔</td><td> </td>
    <td> </td><td> </td>
    <td>ʎ̥˔</td><td>ʎ̝</td>
    <td>ʟ̝̊</td><td>ʟ̝</td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
  </tr>
  <tr>
    <th align="right"><code>apr</code></th>
    <td> </td><td> </td>
    <td>ʋ̥</td><td>ʋ</td>
    <td> </td><td> </td>
    <td>ɹ̥</td><td>ɹ</td>
    <td> </td><td> </td>
    <td>ɻ̊</td><td>ɻ</td>
    <td> </td><td> </td>
    <td>j̊</td><td>j</td>
    <td>ɰ̊</td><td>ɰ</td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
  </tr>
  <tr>
    <th align="right"><code>lat</code>&#xA0;<code>apr</code></th>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td>l̥</td><td>l</td>
    <td> </td><td> </td>
    <td>ɭ̊</td><td>ɭ</td>
    <td> </td><td> </td>
    <td>ʎ̥</td><td>ʎ</td>
    <td>ʟ̥</td><td>ʟ</td>
    <td> </td><td>ʟ̠</td>
    <td> </td><td> </td>
    <td> </td><td> </td>
  </tr>
  <tr>
    <th align="right"><code>flp</code></th>
    <td> </td><td>ⱱ̟</td>
    <td> </td><td>ⱱ</td>
    <td> </td><td> </td>
    <td>ɾ̥</td><td>ɾ</td>
    <td> </td><td> </td>
    <td>ɽ̊</td><td>ɽ</td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td>ɢ̆</td>
    <td> </td><td>ʡ̮</td>
    <td> </td><td> </td>
  </tr>
  <tr>
    <th align="right"><code>lat</code>&#xA0;<code>flp</code></th>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td>ɺ</td>
    <td> </td><td> </td>
    <td> </td><td>ɭ̆</td>
    <td> </td><td> </td>
    <td> </td><td>ʎ̮</td>
    <td> </td><td>ʟ̆</td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
  </tr>
  <tr>
    <th align="right"><code>trl</code></th>
    <td> </td><td>ʙ</td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td>r̥</td><td>r</td>
    <td> </td><td> </td>
    <td>ɽ͡r̥</td><td>ɽ͡r</td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td>ʀ̥</td><td>ʀ</td>
    <td>ʜ</td><td>ʢ</td>
    <td> </td><td> </td>
  </tr>
  <tr>
    <th align="right"><code>clk</code></th>
    <td>ʘ</td><td> </td>
    <td> </td><td> </td>
    <td>ǀ</td><td> </td>
    <td>ǃ</td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td>ǂ</td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
  </tr>
  <tr>
    <th align="right"><code>lat</code>&#xA0;<code>clk</code></th>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td>ǁ</td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
  </tr>
  <tr>
    <th align="right"><code>imp</code></th>
    <td> </td><td>ɓ</td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td>ɗ</td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td>ʄ</td>
    <td> </td><td>ɠ</td>
    <td> </td><td>ʛ</td>
    <td> </td><td> </td>
    <td> </td><td> </td>
  </tr>
  <tr>
    <th align="right"><code>ejc</code></th>
    <td>pʼ</td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td>tʼ</td><td> </td>
    <td> </td><td> </td>
    <td>ʈʼ</td><td> </td>
    <td> </td><td> </td>
    <td>cʼ</td><td> </td>
    <td>kʼ</td><td> </td>
    <td>qʼ</td><td> </td>
    <td>ʡʼ</td><td> </td>
    <td> </td><td> </td>
  </tr>
  <tr>
    <th align="right"><code>ejc</code>&#xA0;<code>frc</code></th>
    <td>fʼ</td><td> </td>
    <td> </td><td> </td>
    <td>θʼ</td><td> </td>
    <td>sʼ</td><td> </td>
    <td>ʃʼ</td><td> </td>
    <td>ʂʼ</td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td>xʼ</td><td> </td>
    <td>χʼ</td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
  </tr>
  <tr>
    <th align="right"><code>lat</code>&#xA0;<code>ejc</code>&#xA0;<code>frc</code></th>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td>ɬʼ</td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
    <td> </td><td> </td>
  </tr>
</table>

Symbols to the left are `vls`, and to the right are `vcd`.

### Other Symbols

| Symbol | Alternative | Features                |
|--------|-------------|-------------------------|
| ʍ      | ɰ̊ʷ           | `vls` `vel` `ptr` `apr` |
| w      | ɰʷ          | `vcd` `vel` `ptr` `apr` |
| ɥ      | jʷ          | `vcd` `pal` `ptr` `apr` |
| ɧ      |             | `vls` `vzd` `pla` `frc` |
| ɫ      |             | `vcd` `fzd` `alv` `lat` `apr` |
| ɚ      |             | `unr` `mid` `cnt` `rzd` `vwl` |
| ɝ      |             | `unr` `lmd` `cnt` `rzd` `vwl` |
| k͡p    |             | `vls` `lbv` `stp`       |
| ɡ͡b    |             | `vcd` `lbv` `stp`       |
| ŋ͡m    |             | `vcd` `lbv` `stp`       |
| p͡f    |             | `vls` `bld` `afr`       |
| b͡v    |             | `vcd` `bld` `afr`       |

### Gemination

Gemination is found in several languages including Italian and Japanese.
It is also present in the suprasegmental phonology between words such as
"lamppost" and "evenness".

Some linguists use the [long](#length) suprasegmental for geminate consonants.
The eSpeak NG convention is to use consonant length for [phonation](#phonation)
when consonant length is distinct without gemination occurring.

The way gemination is represented in eSpeak NG is to duplicate the phonemes,
with the first phoneme using the `unx` feature. For example, n̚.n for a
geminated n. This describes how with the `stp` and `nas` consonants, the
mouth remains closed (`unx`) for the first of the geminated consonants.

### Manner of Articulation

| Feature   | Symbol | Name           |
|-----------|--------|----------------|
| `nas`     |        | nasal          |
| `stp`     |        | plosive (stop) |
| `afr`     |        | affricate      |
| `frc`     |        | fricative      |
| `flp`     |        | tap/flap       |
| `trl`     |        | trill          |
| `apr`     |        | approximant    |
| `clk`     |        | click          |
| `ejc`     |        | ejective       |
| `imp`     | ◌ʼ     | implosive      |
| `vwl`     |        | vowel          |

The `vwl` phonemes are described using vowel height and backness features,
while consonants (the other manners of articulation) are described using
place of articulation features.

Additionally, the manner of articulation can be refined using the following
features:

| Feature | Name     |
|---------|----------|
| `lat`   | lateral  |
| `sib`   | sibilant |

### Place of Articulation

| Feature | Name                  |
|---------|-----------------------|
| `blb`   | bilabial              |
| `lbd`   | labiodental           |
| `bld`   | bilabial-labiodental  |
| `dnt`   | dental                |
| `alv`   | alveolar              |
| `pla`   | palato-alveolar       |
| `rfx`   | retroflex             |
| `alp`   | alveolo-palatal       |
| `pal`   | palatal               |
| `vel`   | velar                 |
| `lbv`   | labio-velar           |
| `uvl`   | uvular                |
| `phr`   | pharyngeal            |
| `glt`   | glottal               |

The `bld` place of articulation is used for `afr` consonants that have a `blb`
onset and a `lbd` release, e.g. in the German p͡f consonant.

__NOTE:__ The IPA charts make a distinction between pharyngeal and epiglottal
consonants, but Wikipedia does not. This model uses the Wikipedia descriptions.

### Voice

| Feature | Name      |
|---------|-----------|
| `vls`   | voiceless |
| `vcd`   | voiced    |

## Vowels

<table>
  <tr>
    <td></td>
    <th colspan="2"><code>fnt</code></th>
    <th colspan="2"><code>cnt</code></th>
    <th colspan="2"><code>bck</code></th>
  </tr>
  <tr>
    <th align="right"><code>hgh</code></th>
    <td>i</td><td>y</td>
    <td>ɨ</td><td>ʉ</td>
    <td>ɯ</td><td>u</td>
  </tr>
  <tr>
    <th align="right"><code>smh</code></th>
    <td>ɪ</td><td>ʏ</td>
    <td> </td><td> </td>
    <td> </td><td>ʊ</td>
  </tr>
  <tr>
    <th align="right"><code>umd</code></th>
    <td>e</td><td>ø</td>
    <td>ɘ</td><td>ɵ</td>
    <td>ɤ</td><td>o</td>
  </tr>
  <tr>
    <th align="right"><code>mid</code></th>
    <td> </td><td> </td>
    <td>ə</td><td> </td>
    <td> </td><td> </td>
  </tr>
  <tr>
    <th align="right"><code>lmd</code></th>
    <td>ɛ</td><td>œ</td>
    <td>ɜ</td><td>ɞ</td>
    <td>ʌ</td><td>ɔ</td>
  </tr>
  <tr>
    <th align="right"><code>sml</code></th>
    <td>æ</td><td> </td>
    <td>ɐ</td><td> </td>
    <td> </td><td> </td>
  </tr>
  <tr>
    <th align="right"><code>low</code></th>
    <td>a</td><td>ɶ</td>
    <td> </td><td> </td>
    <td>ɑ</td><td>ɒ</td>
  </tr>
</table>

Symbols to the left are `unr`, and to the right are `rnd`.

__NOTE:__ The `smh` vowels are more `cnt` than the other vowels. However, this
distinction is not needed to classify these vowels, so is not included in the
above table.

### Height

| Feature | Name                   |
|---------|------------------------|
| `hgh`   | close (high)           |
| `smh`   | near-close (semi-high) |
| `umd`   | close-mid (upper-mid)  |
| `mid`   | mid                    |
| `lmd`   | open-mid (lower-mid)   |
| `sml`   | near-open (semi-low)   |
| `low`   | open (low)             |

### Backness

| Feature | Name            |
|---------|-----------------|
| `fnt`   | front           |
| `cnt`   | center          |
| `bck`   | back            |

### Rounding

| Feature | Name      |
|---------|-----------|
| `unr`   | unrounded |
| `rnd`   | rounded   |

## Diacritics

### Articulation

| Feature | Symbol | Name            |
|---------|--------|-----------------|
| `lgl`   | ◌̼      | linguolabial    |
| `idt`   | ◌̪͆      | interdental     |
|         | ◌̪      | dental          |
| `apc`   | ◌̺      | apical          |
| `lmn`   | ◌̻      | laminal         |
|         | ◌̟      | advanced        |
|         | ◌̠      | retracted       |
|         | ◌̈      | centralized     |
|         | ◌̽      | mid-centralized |
|         | ◌̝      | raised          |
|         | ◌̞      | lowered         |

The articulations that do not have a corresponding feature name are recorded
using the features of their new location in the consonant or vowel charts, not
using the features of the base phoneme.

### Air Flow

| Feature | Symbol | Name       |
|---------|--------|------------|
| `egs`   | ↑      | egressive  |
| `igs`   | ↓      | ingressive |

The ↑ and ↓ symbols are from the extended IPA<sup>\[<a href="#ref7">7</a>\]</sup>.
They only need to be used when the air flow is different to the base IPA
phoneme (e.g. using ↓ on pulmonic consonants).

### Phonation

| Feature | Symbol | Name            |
|---------|--------|-----------------|
| `brv`   | ◌̤      | breathy voice   |
| `slv`   | ◌̥      | slack voice     |
| `stv`   | ◌̬      | stiff voice     |
| `crv`   | ◌̰      | creaky voice    |
| `glc`   | ʔ͡◌    | glottal closure |

The IPA ◌̥ diacritic is also used to fill the `vls` spaces in the IPA consonant
charts. Thus, when ◌̥ is used with a `vcd` consonant that does not have an
equivalent `vls` consonant, the resulting consonant is `vls`, not `slv`.

### Rounding and Labialization

| Feature | Symbol | Name       |
|---------|--------|------------|
| `ptr`   | ◌ʷ, ◌ᶣ | protruded  |
| `cmp`   | ◌ᵝ     | compressed |

The degree of rounding/labialization can be specified using the following
features:

| Feature | Symbol | Name         |
|---------|--------|--------------|
| `mrd`   | ◌̹      | more rounded |
| `lrd`   | ◌̜      | less rounded |

### Syllabicity

| Feature | Symbol | Name            |
|---------|--------|-----------------|
| `syl`   | ◌̩      | syllabic        |
| `nsy`   | ◌̯      | non-syllabic    |

### Consonant Release

| Feature | Symbol | Name                            |
|---------|--------|---------------------------------|
| `asp`   | ◌ʰ     | aspirated                       |
| `nrs`   | ◌ⁿ     | nasal release                   |
| `lrs`   | ◌ˡ     | lateral release                 |
| `unx`   | ◌̚      | no audible release (unexploded) |

### Co-articulation

| Feature | Symbol | Name           |
|---------|--------|----------------|
| `pzd`   | ◌ʲ     | palatalized    |
| `vzd`   | ◌ˠ     | velarized      |
| `fzd`   | ◌ˤ     | pharyngealized |
| `nzd`   | ◌̃      | nasalized      |
| `rzd`   | ◌˞     | rhoticized     |

### Tongue Root

The tongue root position can be specified using the following features:

| Feature | Symbol | Name                  |
|---------|--------|-----------------------|
| `atr`   | ◌̘      | advanced tongue root  |
| `rtr`   | ◌̙      | retracted tongue root |

### Fortis and Lenis

| Feature |Symbol | Name   |
|---------|-------|--------|
| `fts`   | ◌͈     | fortis |
| `lns`   | ◌͉     | lenis  |

The extended IPA<sup>\[<a href="#ref7">7</a>\]</sup> ◌͈ and ◌͉ diacritics
are used to specify lesser (`lns`) and greater (`fts`) oral pressure than
the unmodified voiced or voiceless phoneme. This distinction is made by
the Ewe, Tabasaran, Archi, and other languages<sup>\[<a href="#ref8">8</a>\]</sup>.

Where fortis and lenis are used to contrast consonant durations (e.g. in
the Jawoyn, Ojibwe, and Zurich German languages<sup>\[<a href="#ref8">8</a>\]</sup>),
the [length](#length) suprasegmentals are used instead.

## Suprasegmentals

### Stress

| Feature | Symbol | Name             |
|---------|--------|------------------|
| `st1`   | ˈ◌     | primary stress   |
| `st2`   | ˌ◌     | secondary stress |
| `st3`   | ˈˈ◌    | extra stress     |

### Length

| Feature | Symbol | Name            |
|---------|--------|-----------------|
| `est`   | ◌̆      | extra short     |
| `hlg`   | ◌ˑ     | half-long       |
| `lng`   | ◌ː     | long            |

### Rhythm

| Feature | Symbol | Name              |
|---------|--------|-------------------|
| `sbr`   | ◌.◌    | syllable break    |
| `lnk`   | ◌‿◌    | linked (no break) |

### Intonation

| Feature | Symbol | Name                     |
|---------|--------|--------------------------|
| `fbr`   | &#124; | minor (foot) break       |
| `ibr`   | ‖      | major (intonation) break |
| `glr`   | ↗      | global rise              |
| `glf`   | ↘      | global fall              |

### Tone Stepping

| Feature | Symbol | Name        |
|---------|--------|-------------|
| `ust`   | ꜛ◌     | upstep      |
| `dst`   | ꜜ◌     | downstep    |

### Tones

Tones are defined using the following 3 properties:

	tone_start  <value>
	tone_middle <value>
	tone_end    <value>

The `<value>` field for these properties is a number with one of the following
values:

| Tone               | Symbol | `<value>` |
|--------------------|--------|-----------|
| extra high (top)   | ◌˥     | `5`       |
| high               | ◌˦     | `4`       |
| mid                | ◌˧     | `3`       |
| low                | ◌˨     | `2`       |
| extra low (bottom) | ◌˩     | `1`       |

A *level* tone can be specified by just using the `tone_start` value. A *raising*
or *falling* tone can be specified using the `tone_start` and `tone_end` values.
A *raising-falling* (*peaking*) or *falling-raising* (*dipping*) tone can be
specified using all three values.

## References

1. <a name="ref1"></a> Kirshenbaum, Evan,
   [Representing IPA phonetics in ASCII](http://www.kirshenbaum.net/IPA/faq.html) (HTML). 1993.

2. <a name="ref2"></a> Kirshenbaum, Evan,
   [Representing IPA phonetics in ASCII](http://www.kirshenbaum.net/IPA/ascii-ipa.pdf) (PDF). 2001.

3. <a name="ref3"></a> International Phonetic Association,
   [The International Phonetic Alphabet and the IPA Chart](https://www.internationalphoneticassociation.org/content/ipa-chart). 2015.
   Creative Commons Attribution-Sharealike 3.0 Unported License (CC-BY-SA).

4. <a name="ref4"></a> Wikipedia.
   [International Phonetic Alphabet](https://en.wikipedia.org/wiki/International_Phonetic_Alphabet). 2017.
   Creative Commons Attribution-Sharealike 3.0 Unported License (CC-BY-SA).

5. <a name="ref5"></a> Dunn, R. H.,
   [Cainteoir Text-to-Speech Phoneme Features](https://raw.githubusercontent.com/rhdunn/cainteoir-engine/master/src/libcainteoir/phoneme/phoneme.cpp). 2013-2015.

6. <a name="ref6"></a> Wikipedia.
   [Voiced glottal fricative](https://en.wikipedia.org/wiki/Voiced_glottal_fricative). 2017,
   Creative Commons Attribution-Sharealike 3.0 Unported License (CC-BY-SA).

7. <a name="ref7"></a> Wikipedia.
   [Extensions to the International Phonetic Alphabet](https://en.wikipedia.org/wiki/Extensions_to_the_International_Phonetic_Alphabet). 2017,
   Creative Commons Attribution-Sharealike 3.0 Unported License (CC-BY-SA).

8. <a name="ref8"></a> Wikipedia.
   [Fortis and lenis](https://en.wikipedia.org/wiki/Fortis_and_lenis). 2017,
   Creative Commons Attribution-Sharealike 3.0 Unported License (CC-BY-SA).

9. <a name="ref9"></a> Wikipedia.
   [Place of articulation](https://en.wikipedia.org/wiki/Place_of_articulation). 2017,
   Creative Commons Attribution-Sharealike 3.0 Unported License (CC-BY-SA).
