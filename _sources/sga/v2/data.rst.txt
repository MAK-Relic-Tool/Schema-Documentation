SGA V2 - Data Block
-------------------
The data block is stream of file metadata and data pairs.

.. include:: tables/data-block-pair.rst

File Metadata
*************
File metadata begins 264 bytes *BEFORE* the data offset specified by the file definition.

Metadata does not seem to be required by the engine, and other modding tools may not include metadata, as there are no *explicit* pointers to it.

.. include:: tables/file-metadata-table.rst

File Name
^^^^^^^^^

Last Modified
^^^^^^^^^^^^^
Unix Timestamp, truncated to the last second

File Data Hash
^^^^^^^^^^^^^^
CRC32 hash; calculated from the raw/compressed file data in the archive

File Data
*********
Depending on the File's Storage Flag, this is either raw binary data, or ZLib compressed binary data

