# CS 525 - Advanced Database Organization

This repository contains assignments for CS512 during the term of Fall 2018

# Assignment details

Assignment 1 - Storage Manager

The goal of this assignment is to implement a simple storage manager - a module that is capable of reading blocks from a file on disk into memory and writing blocks from memory to a file on disk. The storage manager deals with pages (blocks) of fixed size (PAGE_SIZE). In addition to reading and writing pages from a file, it provides methods for creating, opening, and closing files. The storage manager maintains several types of information for an open file: The number of total pages in the file, the current page position (for reading and writing), the file name, and a POSIX file descriptor or FILE pointer.

Details regarding the implementation is available in the [assignment 1 readme](assignments/1/assign1/README.md) file.

Assignment 2 - Buffer Manager

The goal of this assignment is to implement a buffer manager. The buffer manager manages a fixed number of pages in memory that represent pages from a page file managed by the storage manager implemented in assignment 1. The memory pages managed by the buffer manager are called page frames or frames for short. We call the combination of a page file and the page frames storing pages from that file a Buffer Pool. The Buffer manager should be able to handle more than one open buffer pool at the same time. However, there can only be one buffer pool for each page file. Each buffer pool uses one page replacement strategy that is determined when the buffer pool is initialized.
Details regarding the implementation is available in the [assignment 2 readme](assignments/2/assign2/README.md) file.

Assignment 3 - Record Manager

The goal of this assignment is to create a record manager. The record manager handles tables with a fixed schema. Clients can insert records, delete records, update records, and scan through the records in a table. A scan is associated with a search condition and only returns records that match the search condition. Each table is stored in a separate page file and the record manager accesses the pages of the file through the buffer manager implemented in assignment 2.

Details regarding the implementation is available in the [assignment 3 readme](assignments/3/assign3/README.md) file.
