This is the repository for the "Towards Robust File System Checkers" project
published in the proceedings of the 16th USENIX Conference on File and Storage Technologies (FAST'18).

The repository contains the following:

  1. "rfsck-lib" contains the source files for rfsck-lib. 
      There is a README available in this folder with steps to
      show how to integerate the tool with your program
      
  2.  "rfsck-ext" is an example of how we integrated rfsck-lib with e2fsck. 
      The source files of the log file are copied into the folder 
      rfsck-ext/lib/ext2fs/. Then redo.h is imported into various header files. 
      
      A grep on the function names would show you how we have integrated 
      rfsck-lib with e2fsck.

      In this example we have provided safe transactions for all the updates
      in each pass.
      
  3.  "rfsck-xfs" is an example of how we integrated rfsck-lib with xfs_repair.
      Similar to rfsck-ext, we have copied the redo log files to folder 
      rfsck-ext/xfslib/, and then included redo.h into various header files.

      In this example we consider updates of the entire run of xfs_repair as
      one transaction
      
  4.  "e2fsck-patch" is a simple fix to make e2fsck robust. To achieve this,
      we synchronize the updates to the undo log.

  5.  "rfsck-test" is a  fault injection engine to analyze the fault resilience of file system checkers.


For further information about the design, please refer to our paper https://www.usenix.org/conference/fast18/presentation/gatla 


BibTex:
@inproceedings{Gatla:2018:TRF:3189759.3189770,
 author = {Gatla, Om Rameshwar and Hameed, Muhammad and Zheng, Mai and Dubeyko, Viacheslav and Manzanares, Adam and Blagojevic, Filip and Guyot, Cyril and Mateescu, Robert},
 title = {{Towards Robust File System Checkers}},
 booktitle = {{Proceedings of the 16th USENIX Conference on File and Storage Technologies}},
 series = {FAST'18},
 year = {2018},
 isbn = {978-1-931971-42-3},
 location = {Oakland, CA, USA},
 pages = {105--121},
 numpages = {17},
 url = {http://dl.acm.org/citation.cfm?id=3189759.3189770},
 acmid = {3189770},
 publisher = {USENIX Association},
 address = {Berkeley, CA, USA},
} 

Contact: Om Rameshwar Gatla, omram@nmsu.edu
