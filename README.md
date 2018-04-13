# CSL
Makes C/C++ as portable as Java by linking it at target computers

----------

CSL is a technology that links your application at client side, thus making C/C++ almost as cross-platform as Java. Please note that the project is still in development: currently, the repo is empty and it's "OK": it's still in its first-lines-of-code state. This repository is empty and will stay empty until CSL is in its public beta; currently it's closed alpha.

## How it works
CSL's principle is simple: one creates an object file (does not link it). Remember that x86 assember code, for example, is compatible between operating systems, it just needs to perform different system calls and be linked with different `.lib` (`.a` on GCC) files. So, the only thing we need to do to make C/C++ very cross-platform is to link it during installation (or during launch) and provide an iterface that works the same on all platforms. C stadnard library is stadartized (C++'s STL too), so the only thing to do is to link object code with platform-specific libraries on users' machines.

### So, it's a "new cross-platform executable format"?
___Short answer___: Yes, it is. 
___Long answer___: In fact, it's __not__ a new executable format: it's an archive format which contains the application object file(s) and instructions how to use them. Executable formats remain the same: it can be ELF, or maybe PE, or _even both_! You can use an executable format and it'll be client-side-linked on all platforms which support it.

## License
The project is licensed under GNU General Public Licesnse (GNU GPL) v2.0. Our team will appreciate any help with the project!

--------
Made in Russia with love
