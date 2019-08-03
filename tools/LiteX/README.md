It is recommended for all FPGA host boards with CRUVI slots to provide LiteX platform support files.

WiP list of platforms provided at https://github.com/micro-FPGA/litex-boards

|Board|FPGA|Status|FPGA build|Test|SDRAM|
|-----|----|--|--|--|--|
|TE0890 S7-mini|Spartan-7|beta|OK|OK|-|
|TE0714|Artix-7|wip | | |n/a|
|TE0725|Artix-7|wip | | |-|
|TE0741|Kintex-7|wip |pass||n/a|
|MAX1000|MAX-10|wip|pass|OK|OK|
|AnalogMAX|MAX-10|||||
|AnalogMAX DAQ1|MAX-10|||||
|AnalogMAX DAQ2|MAX-10|||||
|CYC1000|Cyclone 10LP|||||
|C10LPRefKit|Cyclone 10LP|||||

Boards with HyperRAM are not currently supporting external RAM with LiteX

Note: building for MAX10 10M08 requires manual post-patching of top.v due to bug in LiteX

https://github.com/enjoy-digital/litex/issues/228

