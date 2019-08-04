It is recommended for all FPGA host boards with CRUVI slots provide LiteX platform support files.

WiP list of platforms provided at https://github.com/micro-FPGA/litex-boards

| Board         | FPGA       |Stat|variant|FPGA build|Test|SDRAM|
|---------------|------------|----|-----|-|-|--|
|TE0890 S7-mini |Spartan-7   |beta|min  |OK|OK|-hyper|
|TE0710         |Artix-7     |wip |     | | |n/a|
|TE0711         |Artix-7     |wip |full |OK|OK|n/a|
|TE0712         |Artix-7     |wip |     | | | |
|TE0713         |Artix-7     |wip |     | | | |
|TE0714         |Artix-7     |wip |     | | |n/a|
|TE0725         |Artix-7     |wip |     | | |-hyper|
|TE0741         |Kintex-7    |wip |?    |pass||n/a|
|MAX1000        |MAX-10      |wip |min  |pass|OK|OK|
|AnalogMAX      |MAX-10      |    |min  ||||
|AnalogMAX DAQ1 |MAX-10      |    |min  ||||
|AnalogMAX DAQ2 |MAX-10      |    |min  ||||
|CYC1000        |Cyclone 10LP|    |?    ||||
|C10LPRefKit    |Cyclone 10LP|wip |full |pass|OK|OK|
|TEI0006        |Cyclone 10GX|    |     ||||

Boards with HyperRAM are not currently supporting external RAM with LiteX

Note: building for MAX10 10M08 requires manual post-patching of top.v due to bug in LiteX

https://github.com/enjoy-digital/litex/issues/228

