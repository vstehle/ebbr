List of potential deprecations
==============================

.. list-table:: Items we warned in a note that a future version of EBBR will disallow
   :widths: 50 50
   :header-rows: 1
   :class: longtable

   * - Item
     - Comments
   * - MBR partitioning for shared storage.
     - Could we require GPT partitioning?
       Some SoCs need an MBR to find their firmware; would the GPT MBR work in
       that case? This allows to describe 4 partitions.
   * - SoCs loading firmware from a fixed offset into the storage media.
     - Does not sound reallistic; RK3xxx SoCs are using this. i.MX8M does this,
       too, but eMMC boot partitions mitigate.

.. list-table:: Other items
   :widths: 50 50
   :header-rows: 1
   :class: longtable

   * - Item
     - Comments
   * - Firmware support of MBR partitioning on block devices (and GPT and El
       Torito)
     - Do not deprecate; continue to require.
   * - PSCI pre-v1.0
     - We recommend >= 1.0; require?
   * - SMCCC pre-v1.1
     - We recommend >= 1.1; require?
