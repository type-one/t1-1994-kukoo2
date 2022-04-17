What
----

Kukoo 2 (v43) source code

BBSTro
Released January 1994
MS-Dos

https://demozoo.org/productions/142610/
https://files.scene.org/view/mirrors/hornet/code/demosrc/bbsintro/kuk2src.zip

It was an Advertising Intro for Pleasure Access BBS, a belgian BBS located in Brussels in the 90s.

It was running on 90's VGA cards like Cirrus Logic, ATI, S3, Trident 9000/8900CL.  The typical 
VGA graphic cards you had on 386/486 MS-DOS computers at that time.

The DosBox community did some workaround to have it running in the emulator when you enable VGA Compatibility.
They found a bug in the original code that was preventing it to run in the emulator and on some VGA boards.

The intro itself is a 16-bit executable using Intel 386 instructions.  

At that time I had a 486 DX 33 Mhz that I could downclock to 8 Mhz, and a friend who had a 386 DX-33 for testing, 
as well as some 386 SX-16 computers that were available at my university.

The intro was published beginning of 1994 on some Belgian BBSes and on some FTP sites that were popular in the 
early 90-ties (ftp.oulu.fi, hornet, ...).  It was mirrored later on sites like scene.org.

Most of the code was started and written during february/march 1993, during a break after the University winter exams 
when I was in 1st year of Computer Sciences.  The next months I did test and fix on several friends machines and 
VGA cards, until the published BBS and Internet release.

The released intro was compressed using PKLITE (from what I remember)
http://fileformats.archiveteam.org/wiki/PKLITE

The source is a single x86 assembly language file (.ASM) that includes some precomputed tables and some assets
converted into asm data.  A lot of comments in the code are in french, with some private jokes that only a few
friends who were studying with me will understand ;-)

Build
-----

To build the executable you will need a MASM compatible assembler with a 16 bit linker.

Use Windows and run **build.bat** in the src folder.

One possibility is to use the legacy MASM assembler that Microsoft released for free a decade ago.

Another is to use the free compatible JWasm assembler available here: 
https://www.japheth.de/JWasm.html

Instructions to use MASM 6.14 and LINKER 5.63 are available here:
https://service.scs.carleton.ca/sivarama/asm_book_web/free_MASM.html
http://www.masm32.com

Microsoft's MASM 6.14 is included in the masm32 package.

To get MASM 6.14, download masm32V8.zip from:

http://www.masm32.com/ (2.98 MB)

Unzip and run install.exe. It creates masm32 directory. 
The MASM files (ml.exe and ml.err) are in the masm32/bin directory.

Do NOT use the linker link.exe (32 bit) in the masm32/bin directory. 
Use the linker version 5.60 to generate 16-bit DOS applications. 

You can get this by googling for "Microsoft BASIC Softlib Collection"

Execute lnk563.exe to extract link.exe file.

You need these three files (ml.exe, ml.err, and link.exe) to run the assembly programs. 

You can just drop these 3 files in the src folder or copy the **jwasm.exe** executable there.


Run
---

On **DosBox** you have to use machine=vgaonly in the emulator settings

On real MS-DOS PC with MS-DOS 6.2+, an AdLib compatible card (SoundBlaster, SoundBlaster Pro, SoundBlaster 16, AWE32/64)
and an ISA/VESA VGA card or some older PCI VGA cards (like S3 Trio, S3 Virge).

I still achieve to run it on my old (preserved) 486 DX2-66/S3 (1995) and a K6-2 500/S3 Virge DX (1999), that are still working 
today in 2022.

You will maybe need a CRT to handle the expanded video mode (384x564 60 hz). Initially I defined this video mode
to cover totally the borders of the CRT screen I had at that time (an old 14' 4/3 VGA screen), inspired by the 
"overscan" tricks we were using in the Atari ST scene.

For the pre-tro joke that is in CGA and uses the PC speaker, you should have a buzzer/pc speaker to listen to the 
"belgian national anthem tone".




