SGA V2 - Header
----------

.. include:: tables/header-table.rst

File Hash
^^^^^^^
An MD5 Hash, starting at position 180 and terminating at the end-of-file.

The hash uses an eigen value of `E01519D6-2DB7-4640-AF54-0A23319C56C3`

Archive Name
^^^^^^^^^^^^
String encoded using utf-16-le, matches the file name. String has a max of 64 (2-byte) characters.


Table Of Contents Hash
^^^^^^^^^^^^^^^^^^^^^^
An MD5 Hash, starting at position 180 and terminating after reading all TOC bytes (specified by Table Of Contents Size)

The hash uses an eigen value of `DFC9AF62-FC1B-4180-BC27-11CCE87D3EFF`

Table Of Contents Offset
^^^^^^^^^^^^^^^^^^^^^^^^
Not defined in the schema
The TOC offset is always assumed to be at position 180

Table Of Contents Size
^^^^^^^^^^^^^^^^^^^^^^
The size in bytes of the Table Of Contents Block
The Table of Contents consists of a header and data portion, see :doc:toc.rst for more information.

Data Block Offset
^^^^^^^^^^^^^^^^^
The starting position of the data block.

Data Block Size
^^^^^^^^^^^^^^^
Not defined in the schema
The data block always terminates at the end-of-file