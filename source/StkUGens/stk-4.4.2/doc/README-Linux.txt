The Synthesis ToolKit in C++ (STK)

By Perry R. Cook and Gary P. Scavone, 1995-2010.

Please read the file README and INSTALL for more general STK information.

Realtime audio support for Linux currently includes the Advanced Linux Sound Architecture (ALSA), the JACK low-latency audio server, and/or Open Sound System (OSS version 4.0 and higher only) APIs.  One or more APIs are selected during compilation using the __LINUX_ALSA__, __UNIX_JACK__, and/or __LINUX_OSS__ definitions.  Because the ALSA library is now integrated into the standard Linux kernel, it is the default audio/MIDI API with STK versions 4.2 and higher.  The __LINUX_ALSASEQ__ definition is required to compile RtMidi with ALSA sequencer support.  Native OSS MIDI support no longer exists in RtMidi.  If the __LINUX_OSS__ preprocessor definition is specified, only OSS audio support will be compiled and RtMidi will still be compiled using the ALSA API.  For this reason, STK now requires the asound library for realtime support.  Realtime programs must also link with the pthread library.  The OSS audio API can be selected by passing the "--with-oss" option to configure.

STK should compile without much trouble under Linux.  Since all Linux distributions typically include the GNU makefile utilities, you should be able to use the default Makefile.  Typing "make" will initiate the compilation process.

MIDIATOR SERIAL PORT MIDI SUPPORT:

MIDIator support has been removed from RtMidi with STK versions 4.2 and higher.  If you really need it, you can contact us to get an old distribution.

NOTE REGARDING PTHREADS:

There haven't been any problems with threads since the old days of RedHat Linux 5.0.  STK uses the MIT pthreads API.


