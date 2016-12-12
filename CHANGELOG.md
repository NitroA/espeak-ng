# Change Log

## 1.49.1 - (In Development)

*  Vim syntax support for rule files.
*  Replace `ieee80.c` with the implementation at
   http://www.realitypixels.com/turk/opensource/ToFromIEEE.c.txt for Debian
   open source license compliance.
*  Documentation updates.
*  Emscripten support.

bug fixes:

*  Fix `.Lnn` rule groups to allow groups above 62.
*  Fix reporting the eSpeak NG version in the `--version` string and Windows
   installer.
*  Fix a crash when calling `LoadDictionary` when using clang.
*  Threading fixes and Mac OSX portability for the fifo and event code.
*  Fixes for running thre spect code on big-endian architectures.

updated languages:

*  en (English) -- Valdis Vitolins
*  it (Italian) -- chrislm
*  ky (Krygyz) -- JRMeyer
*  lv (Latvian) -- Valdis Vitolins
*  tr (Turkish) -- Valdis Vitolins

## 1.49.0 - 2016-09-10

*  Support the `--compile-mbrola` command-line option.
*  Support the `--compile-phonemes` command-line option.
*  Support the `--compile-intonations` command-line option.
*  Support SSML &lt;phoneme alphabet="espeak" ph="..."&gt; tags.
*  Added man files for the `speak-ng` and `espeak-ng` command-line programs.
*  Created a companion espeak-ng API to provide more detailed error codes and
   provide access to the new espeak-ng functionality.
*  Fixed many logic and security issues reported by clang scan-build, Coverity
   and msvc /analyze.
*  Group languages by their language family and use BCP47 compliant names.
*  Support for Windows and BSD platforms.
*  Removed support for WinCE, MS-DOS and RiscOS.
*  Add support for `maintainer` and `status` field in voice files for tracking
   voice maintenance.
*  Vim syntax highlighting for espeak dictionary (list and rules) files.
*  Support reading input from named pipes.
*  Fix wav file truncation when reading multiline text from stdin or a named pipe.

build:

*  Build the code with a C99 compiler, instead of a C++ compiler.
*  Provide a pkg-config file (patch by Luke Yelavich).
*  Use -fPIC to support sparc/sparc64 architectures.
*  Removed the local portaudio header files.
*  Use the system's sonic library and header files.
*  Output phoneme compilation errors to stderr.
*  Generate build failures if building phoneme, intonation or dictionary files
   contain errors.
*  Provide modern Visual Studio project files to build eSpeak NG on Windows,
   with a WiX-based project to create an MSI installer.
*  Use the NetBSD `getopt_long` implementation on Windows.

restructuring:

*  Moved the library code to `src/libespeak-ng`.
*  Renamed `espeak` to `espeak-ng`.
*  Renamed `speak` to `speak-ng`.
*  Use the `libespeak-ng` API in `speak-ng` using a shared implementation with
   `espeak-ng`.
*  Moved the code to build the mbrola voice data, phoneme tables and intonation
   data to libespeak-ng.
*  Removed the `espeakedit` program and the associated wxWidgets dependency.
*  Removed the platforms directory and approaching portability in a similar way
   to how libressl handles portability.
*  Converted the documentation to markdown.
*  Group the Windows and POSIX mbrowrap code to provide the `mbrowrap.h`
   implementation in a single place.
*  Replaced the audio APIs with PCAudioLib to improve portability of the audio
   and to share that across different projects.
*  Reworked the synchronous audio to share the code paths with asynchronous
   audio.

cleanup:

*  Removed unused/empty internal header files.
*  Removed unused and commented out code.
*  Reformatted the code to use a consistent style and indentation.
*  Fixed many GCC and clang warnings.
*  Improved the error handling within the codebase to report the underlying
   error where possible.
*  Inlined several wrapper methods that were adding little/no value.

updated languages:

*  en (English) -- Thanks to Kendell Clark for identifying mispronunciations.
*  el (Greek) : improved polytonic Greek support
*  es (Spanish) : ChrisLeo (improved intonations)
*  fa (Persian) -- Shadyar Khodayari
*  fr (French) -- Thomas Guillory
*  ga (Irish Gaelic) -- Jim Regan
*  it (Italian) -- ChrisLeo
*  lv (Latvian) -- Valdis Vitolins

new languages:

*  gn (Guarani) -- ChrisLeo
*  ky (Kyrgyz) -- JRMeyer
*  mb-br2 (Brazillian Portuguese)
*  mb-de\* (German) : extend support coverage of the German MBROLA voices
*  mb-lt1 (Lithuanian) -- embar
*  mb-lt2 (Lithuanian) -- embar
*  mt (Maltese)
*  my (Myanmar/Burmese) -- Min Maung, Lwin Moe
*  tn (Setswana)
*  tt (Tatar)

## Historic

These are a condensed set of releases that were maintained in step with the
upstream eSpeak releases. The releases containing minor build fixes, or only
incorporating upstream changes have been omitted.

### 1.48.11 - 2014-08-31

*  Support building the MBROLA voice files.
*  mbrola/de6 support for syllabic m and syllabic n.

### 1.47.14 - 2013-12-03

*  Support building with the extended Chinese and Russian dictionary data.

### 1.47.13 - 2013-10-22

updated languages:

*  om (Oromo)

### 1.47.12 - 2013-10-12

*  Added the NVDA voice variants.
*  Do not crash if `espeak_SetPunctuationList` is called with a NULL
   punctuation list.
*  Fix a segfault in `GetTranslatedPhonemeString`.

new languages:

*  om (Oromo)

build:

*  Support the `--with-async` configure option.
*  Support the `--with-sonic` configure option.
*  Support the `--with-mbrola` configure option.
*  Support the `--with-klatt` configure option.
*  Support the `--with-sada` configure option.
*  More build improvements.

### 1.46.23 - 2012-09-11

*  Converted the build to use autotools.

### 1.46.11 - 2011-12-31

*  Support building all the voice dictionaries.
*  More build improvements.

### 1.43.46 - 2010-06-28

*  Initial build changes to make it easier to build espeak on POSIX systems.
