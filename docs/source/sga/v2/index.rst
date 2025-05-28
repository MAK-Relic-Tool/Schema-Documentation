SGA V2
======
.. toctree::

   table-of-contents/index

SGA V2 Schema
=============

.. list-table:: File Layout
   :header-rows: 1

   * - Start
     - Stop
     - Size
     - Type
     - Name

   * - 0
     - 11
     - 12
     - [link-to-table]
     - Magic & Version

   * - 12
     - 179
     - 168
     - [link-to-table]
     - Header

   * - 180
     -
     -
     - [link-to-table]
     - Table Of Contents

   * -
     -
     - EOF - 180
     - [link-to-table]
     - Data Block

Magic & Version
---------------
.. list-table:: Magic & Version
   :header-rows: 1

   * - Start
     - Stop
     - Size
     - Type
     - Name

   * - 0
     - 7
     - 8
     - Bytes
     - Magic Word

   * - 8
     - 9
     - 2
     - UInt-16
     - Version Major

   * - 10
     - 11
     - 2
     - UInt-16
     - Version Minor

Magic Word
^^^^^^^^^^
An 8 byte ascii string, which is always 'ARCHIVE_'


Version
^^^^^^^
The Version Major and Minor determine the schema of the SGA file
Major is always 2 for the original Dawn of War series and Impossible Creatures


SGA Header
----------
.. list-table:: Header
   :header-rows: 1

   * - Start
     - Stop
     - Size
     - Type
     - Name

   * - 0
     - 15
     - 16
     - MD5 Hash
     - File Hash

   * - 16
     - 143
     - 128
     - String [1]_
     - Archive Name

   * - 144
     - 159
     - 16
     - MD5 Hash
     - Table of Contents Hash

   * - 160
     - 163
     - 4
     - UInt-32
     - Table Of Contents Size

   * - 164
     - 167
     - 4
     - UInt-32
     - Data Block Offset

File Hash
^^^^^^^
An MD5 Hash, starting at position 180 and terminating at the end-of-file.

The hash uses an eigen value of `E01519D6-2DB7-4640-AF54-0A23319C56C3`

Archive Name
^^^^^^^^^^^^

Table Of Contents Hash
^^^^^^^^^^^^^^^^^^^^^^
An MD5 Hash, starting at position 180 and terminating after reading all TOC bytes (specified by Table Of Contents Size)

The hash uses an eigen value of `DFC9AF62-FC1B-4180-BC27-11CCE87D3EFF`

Table Of Contents Offset
^^^^^^^^^^^^^^^^^^^^^^^^
While not defined in the schema, the TOC offset is always assumed to be at position 180

Table Of Contents Size
^^^^^^^^^^^^^^^^^^^^^^

Data Block Offset
^^^^^^^^^^^^^^^^^





.. [1] String is encoded using `utf-16-le`, and padded with the null character `\0`

.. [2] String is encoded using `ascii`, and padded with the null character `\0`



