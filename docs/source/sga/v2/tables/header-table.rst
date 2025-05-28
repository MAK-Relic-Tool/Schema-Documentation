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
     - String (utf-16-le)
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