SGA V2 - Schema
------
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
     - :doc:`magic-version`
     - Magic & Version

   * - 12
     - 179
     - 168
     - :doc:`header`
     - Header

   * - 180
     -
     -
     - :doc:`toc`
     - Table Of Contents

   * -
     -
     -
     - :doc:`data`
     - Data Block
