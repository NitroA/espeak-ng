# Table of contents

  * [Phonemes](#phonemes)
    * [English Consonants](#english-consonants)
    * [Some Additional Consonants](#some-additional-consonants)
    * [English Vowels](#english-vowels)
    * [Some Additional Vowels](#some-additional-vowels)

# Phonemes

In general a different set of phonemes can be defined for each language.

In most cases different languages inherit the same basic set of
consonants. They can add to these or modify them as needed.

The phoneme mnemonics are based on the scheme by Kirshenbaum which
represents International Phonetic Alphabet symbols using ascii
characters. See:
[www.kirshenbaum.net/IPA/ascii-ipa.pdf](http://www.kirshenbaum.net/IPA/ascii-ipa.pdf).

Phoneme mnemonics can be used directly in the text input to
**espeak-ng**. They are enclosed within double square brackets. Spaces
are used to separate words, and all stressed syllables must be marked
explicitly. eg:  
\[[D,Is Iz sVm f@n'EtIk t'Ekst 'InpUt]\]

## English Consonants

Phoneme|Phoneme
----------------|-----------
\[p\]           | \[b\]
\[t\]           | \[d\]
\[tS\] **ch**urch | \[dZ\] **j**udge
\[k\]           | \[g\]
\[f\]           | \[v\]
\[T\] **th**in  | \[D\] **th**is
\[s\]           | \[z\]
\[S\] **sh**op  | \[Z\] plea**s**ure
\[h\]           |
\[m\]           | \[n\]
\[N\] si**ng**  |
\[l\]           | \[r\] **r**ed (Omitted if not immediately followed by a vowel). |
\[j\] **y**es   | \[w\]

## Some Additional Consonants

Phoneme|Phoneme
------------------------|-----------
\[C]\ German i**ch**    | \[x\] German bu**ch**
\[l^\] Italian **g**li  | \[n^\] Spanish **ñ**

## English Vowels

These are the phonemes which are used by the English spelling-to-phoneme
translations (en\_rules and en\_list). In some varieties of English
different phonemes may have the same sound, but they are kept separate
because they may differ in another variety.

In rhotic accents, such as General American, the phonemes
`[3:], [A@], [e@], [i@], [O@], [U@]` include the "r" sound.

Phoneme|Pronunciation|Description
----------|-------------------------|--------------------------------------------
\[@\]    | alph**a**                | schwa
\[3\]    | bett**er**               | rhotic schwa. In British English this is the same as \[@\], but it includes 'r' colouring in American and other rhotic accents. In these cases a separate \[r\] should not be included unless it is followed immediately by another vowel.
\[3:\]   | n**ur**se                |
\[@L\]   | simp**le**               |
\[@2\]   | the Used only for "the". |
\[@5\]   | to  Used only for "to".  | 
\[a\]    | tr**a**p                 |
\[aa\]   | b**a**th                 | This is \[a\] in some accents, \[A:\] in others.
\[a#\]   | **a**bout                | This may be \[@\] or may be a more open schwa.
\[A:\]   | p**al**m                 | 
\[A@\]   | st**ar**t                |
\[E\]    | dr**e**ss                | 
\[e@\]   | squ**are**               | 
\[I\]    | k**i**t                  |
\[I2\]   | **i**ntend               | As \[I\], but also indicates an unstressed syllable.
\[i\]    | happ**y**                | An unstressed "i" sound at the end of a word.
\[i:\]   | fl**ee**ce               | 
\[i@\]   | n**ear**                 | 
\[0\]    | l**o**t                  | 
\[V\]    | str**u**t                |
\[u:\]   | g**oo**se                |
\[U\]    | f**oo**t                 |
\[U@\]   | c**ure**                 |
\[O:\]   | th**ou**ght              |
\[O@\]   | n**or**th                |
\[o@\]   | f**or**ce                |
\[aI\]   | pr**i**ce                |
\[eI\]   | f**a**ce                 |
\[OI\]   | ch**oi**ce               |
\[aU\]   | m**ou**th                |
\[oU\]   | g**oa**t                 |
\[aI@\]  | sc**ie**nce              |
\[aU@\]  | h**our**                 |

## Some Additional Vowels

Other languages will have their own vowel definitions, eg:

Phoneme|Description
--------|------------------------
\[e\]   | German **eh**, French **é**
\[o\]   | German **oo**, French **o**
\[y\]   | German **ü**, French **u**
\[Y\]   | German **ö**, French **oe**

**\[:\]** can be used to lengthen a vowel, eg \[e:\]
