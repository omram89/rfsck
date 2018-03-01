This is repository for "rfsck-lib", a generic logging library.

The repository contains two folders:

  1. "src" contains the source files for rfsck-lib. 
      There is a README available in this folder with steps to
      show how to integerate the tool with your program
      
  2.  "redo_e2fsprogs" is an example of how to integrate rfsck-
      lib with existing checkers. The source files of the log 
      file are copied into the folder redo_e2fsprogs/e2fsprogs/
      lib/ext2fs/. Then redo.h is imported into various header 
      files. 
      
      A grep on the function names would show you how we have
      integrated rfsck-lib with e2fsck.
      
  3.  "redo_xfsprogs" -> Coming soon
  4.  "e2fsck-patch"  -> Coming soon
