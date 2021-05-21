It is recommended for all FPGA host boards with CRUVI slots provide LiteX platform support files.

WiP list of platforms provided at https://github.com/micro-FPGA/litex-boards

| Board         | FPGA       |Stat|variant|FPGA build|Test|SDRAM|Linux|ETH|
|---------------|------------|----|-----|-|-|--|--|--|
|CR00010        |MAX-10      |wip |min  |||OK|opt*|n/a|
|CR00070        |PolarFire   | |  ||||+||
|CR00071        |PolarFireSoC|20Q2|  ||||+||
|TE0890 S7-mini |Spartan-7   |beta|min  |OK|OK|Hyper|n/a|n/a|
|[MEGA65](http://mega65.org/) |Artix-7     ||full|OK|OK|Hyper|n/a|OK|
|TE0710         |Artix-7     |wip |full |pass| | |||
|TE0711         |Artix-7     |wip |full |OK|OK|n/a|n/a|n/a|
|TE0712         |Artix-7     |wip |     | | | |||
|TE0713         |Artix-7     |wip |     | | | ||n/a|
|TE0714         |Artix-7     |wip |     | | |n/a|n/a|n/a|
|TE0725         |Artix-7     |wip |full |OK|OK|Hyper|n/a|n/a|
|TE0741         |Kintex-7    |wip |?    |pass||n/a|n/a|n/a|
|TE0841         |Kintex-U    | |?    |||n/a|n/a|n/a|
|TEC0089        |Kintex-7    |wip |    |||n/a|n/a|n/a|
|MAX1000        |MAX-10      |wip |min  |OK|OK|OK|opt*|n/a|
|AnalogMAX      |MAX-10      |    |min  ||||n/a|n/a|
|AnalogMAX DAQ1 |MAX-10      |    |min  ||||n/a|n/a|
|AnalogMAX DAQ2 |MAX-10      |    |min  ||||n/a|n/a|
|CYC1000        |Cyclone 10LP|wip |full |OK|OK|OK|opt*|n/a|
|C10LPRefKit    |Cyclone 10LP|wip |full* |OK|OK|SDR+Hyp|OK|OK|
|C10LP EvalKit  |Cyclone 10LP|wip |lite|OK|OK|Hyper|n/a||
|[SoCkit](https://www.arrow.com/en/products/sockit/arrow-development-tools) |CycloneV SoC|wip |lite|OK|blink||||
|TEI0006        |Cyclone 10GX|    |     ||||?||
|SMF2000        |SmartFusion2|    |lite|OK|OK|OK|n/a|n/a|
|SmartBerry     |SmartFusion2|    |     ||||||
|TEM0006        |PolarFire|    |     ||||||
|TEM0007        |PolarFireSoC|20Q1|     ||||||


Note: do not select "linux" variant when building bitstreams, different memory map makes the design not bootable

LiteX on Windows (no WSL) quick howto:
* Make sure Python 3.7 is installed (maybe need copy python.exe to python3.exe)
* Make sure you have gnu make, and Quartus, Vivado on the path
* clone and install LiteX and this repo
* get and install https://gnu-mcu-eclipse.github.io/toolchain/riscv/install/
* make sure the riscv toolchain riscv-none-embed is also on the path
* build your LiteX SoC as usual

for Linux use make.py from

https://github.com/micro-FPGA/linux-on-litex-vexriscv

and prebuilt linux images from

https://github.com/litex-hub/linux-on-litex-vexriscv-prebuilt






