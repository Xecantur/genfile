genfile generates bare files for common programming languages to reduce typing the same
old thing thousands of times, it can also generate bare files with custom
#include/import's for C,C++ and python respectively(in the future it should handle
perl,lua,ruby, and perhaps rust, and maybe some odds and ends after a common syntax for
describing formats has been written) I do intend to add support for other common files
such as Makefiles and perhaps Licenses as well.



WARNING THIS PROGRAM/SCRIPT CAN AND WILL OVERWRITE FILES OF THE SAME NAME YOU'VE BEEN
WARNED!!!!!!!!!!(Currently this may change in the future with more wisdom)

example of the above warning(btw thats not my actual prompt I use zsh with a 2 line
prompt see my dotfiles repo):

[cexru@host dir]$ ls
somefile.py somefile.c somefile.cpp somefile.h somefile.hpp genfile
[cexru@host dir]$ cat somefile.py
#!/usr/bin/python

def main():
    print("Something");
main();
[cexru@host dir]$ ./genfile -p somefile.py
Generating bare Python Script
[cexru@host dir]$ cat somefile.py
#!/usr/bin/python/

def main():
    print("Hello World!");
main();
[cexru@host dir]$ 
