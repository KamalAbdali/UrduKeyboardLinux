URDU QWERTY KEYBOARD LAYOUT FOR LINUX

This keyboard layout enables one to enter and edit Urdu documents. 
It also includes support for Persian, Punjabi (Shahmukhi or 
Pakistani style), Arabic, and Ottoman Turkish. With this layout, 
you can type all the Arabic script characters that these languages 
use. In addition, it also has keys for several mathematical and 
technical symbols.

The file "UrduQWERTYkeyboardWinLnx.pdf" is a printable one-page
keyboard map for reference.


*** DIRECTORIES ***

1. src

- Linux keyboard layout source file 'pk' 
(in the subdirectory 'symbols').
This file contains several layout variants for Urdu. 
The present one, Urdu QWERTY, is labeled "urd-qwerty".

- The files base.lst, evdev.xml, and xorg.lst (all in the
subdirectory 'rules') needed to add the new layout to 
the xkb datbase.

- TeX source file UrduQWERTYkeyboardWinLnx.tex. It should 
be processed by the XeLaTeX engine to produce the keymap picture 
UrduQWERTYkeyboardWinLnx.pdf.


2. distrib
This directory contains the files needed for installing the Urdu 
QWERTY keyboard layout on a Linux computer. It also includes 
some files providing installation instructions and a keyboard map. 
A zip of the files in this directory is a convenient way to 
distribute the layout. Such a zip file is downloadable from 
http://geomete.com/ftp/UrduQWERTY-v6linux.zip


*** CAUTION ***

As the keyboard map UrduQWERTYkeyboardWinLnx.pdf shows, pressing
the key '=' is intended to generate the Urdu symbol 
"letter alif superimposed with the diacritcal mark 'do zabar'" 
(in Unicode parlance, "ARABIC ALEF LETTER WITH FATHATAN ABOVE").
This requires making the key '=' generate the Unicode string 
'U0627 + U04B'. I haven't found a way to do this in Linux/xkb. 
If anyone knows how to do this, I'll appreciate their advice.
Note that this task is accomplished perfectly in Windows and MacOS,
by the keyboard layout compilers Microsoft's "Keyboard Layout 
Creator" and John Brownie's "Ukelele", respectively. Until the 
problem is solved in Linux/xkb, the user can generate that symbol 
by pressing the key 'a' followed by the key '~'.



