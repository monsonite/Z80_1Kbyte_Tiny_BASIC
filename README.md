# Z80_1Kbyte_Tiny_BASIC
A Z80 Tiny BASIC in under 1 Kbytes - inspired by Paul Scott Robson's 8008 Version

Converted from 8008 mnemonics to Z80.

These mnemonics are not yet optimised to use the Z80 relative jumps or the 16-bit math instructions.

There are some really sneaky code routines for performing 16-bit add, sub, and, or, xor, using minimum code.

Rather than having inline code to handle the low byte and then the high byte, it has a routine that handles just 1-byte, which it presents with the low byte first, then call it again presenting it the high byte.

This saves about 20 bytes (3% of total).

Equally, his multiply and divide routines are very concise.

The other elegant routine is the test for  =, <.  or >, which he squeezes all 3 comparisons into just 21 bytes.  

Paul's site is here: where he has written emulators (in C)  for both the 8008 and the RCA 1802, and ported TinyBASIC to them.

https://github.com/paulscottrobson/1k-coding-challenge/tree/master

Also see his 2017 Hackaday 1K Coding Challenge entry:

https://hackaday.io/project/18851-8008-1k-tiny-basic
