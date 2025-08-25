SGA V2 - Table Of Contents Block
-----------------------

Table Of Contents Header
************************
.. toctree::
   :maxdepth: 2

   file-definition/index


.. include:: tables/toc-header-table.rst

Folder/File/Name Offset
^^^^^^^
Offsets are relative to the TOC start; at position 180


Folder/File/Name Count
^^^^^^
Counts are the number of entries in the block


Root Folder Definition
**********************
.. include:: tables/toc-root-folder-table.rst

Path
^^^^

Alias
^^^^^


First Folder/File
^^^^^^^^^^^^^^^^^
Inclusive index into the Table Of Content's folder/file array

Last Folder/File
^^^^^^^^^^^^^^^^
Exclusive index into the Table Of Content's folder/file array

Root Folder
^^^^^^^^^^^
Index into the Table Of Content's folder array which servers as the root folder



*****************
Folder Definition
*****************
.. include:: tables/toc-folder-table.rst

Name Offset
^^^^^^^^^^^^^^^^^^^^

First Child Folder
^^^^^^^^^^^^^^^^^^

Last Child Folder
^^^^^^^^^^^^^^^^^


First File
^^^^^^^^^^

Last File
^^^^^^^^^


File Definition
***************
Dawn Of War and Impossible Creatures use two slightly different schemas for files

Dawn Of War
###########

.. include:: tables/dow-file-table.rst

Impossible Creatures
###########

.. include:: tables/ic-file-table.rst

Name Offset
^^^^^^^^^^^

Storage Flag
^^^^^^^^^^^
The only difference between the two schemas is the size of the storage flag; Dawn Of War uses 4 bytes, where as Impossible Creatures uses only 1 byte.

.. include:: tables/toc-file-storageflag.rst


Data Offset
^^^^^^^^^^^
Offset to the file data relative to the data offset defined in the SGA header.
See :doc:data.rst for more information

Compressed Size
^^^^^^^^^^^^^^^
Size of the packed file in the archive

This is the size used to read data from the archive.

Decompressed Size
^^^^^^^^^^^^^^^
Size of the unpacked file on disk

This size is used to verify the file was not corrupted after unpacking.