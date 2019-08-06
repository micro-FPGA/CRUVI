It is recommended for all FPGA host boards with CRUVI slots provide LiteX platform support files.

WiP list of platforms provided at https://github.com/micro-FPGA/litex-boards

| Board         | FPGA       |Stat|variant|FPGA build|Test|SDRAM|Linux|
|---------------|------------|----|-----|-|-|--|--|
|TE0890 S7-mini |Spartan-7   |beta|min  |OK|OK|-hyper|n/a|
|MEGA65         |Artix-7     |    |     | | | |n/a|
|TE0710         |Artix-7     |wip |full |pass| | |-|
|TE0711         |Artix-7     |wip |full |OK|OK|n/a|n/a|
|TE0712         |Artix-7     |wip |     | | | |-|
|TE0713         |Artix-7     |wip |     | | | |-|
|TE0714         |Artix-7     |wip |     | | |n/a|n/a|
|TE0725         |Artix-7     |wip |     | | |-hyper|n/a|
|TE0741         |Kintex-7    |wip |?    |pass||n/a|n/a|
|MAX1000        |MAX-10      |wip |min  |OK|OK|OK|?|
|AnalogMAX      |MAX-10      |    |min  ||||n/a|
|AnalogMAX DAQ1 |MAX-10      |    |min  ||||n/a|
|AnalogMAX DAQ2 |MAX-10      |    |min  ||||n/a|
|CYC1000        |Cyclone 10LP|    |?    ||||-|
|C10LPRefKit    |Cyclone 10LP|wip |full* |OK|OK|OK|OK|
|TEI0006        |Cyclone 10GX|    |     ||||?|

Boards with HyperRAM are not currently supporting external RAM with LiteX

Note: do not select "linux" variant when build the bitstreams, different memory map makes the design not bootable

LiteX on Windows (no WSL) quick howto:
* Make sure Python 3.7 is installed (maybe need copy python.exe to python3.exe)
* Make sure you have gnu make, and Quartus, Vivado on the path
* clone and install LiteX and this repo
* get and install https://gnu-mcu-eclipse.github.io/toolchain/riscv/install/
* in file C:\Python37\Lib\site-packages\litex-0.2.dev0-py3.7.egg\litex\soc\cores\cpu\vexriscv\core.py change

        return ("riscv64-unknown-elf", "riscv32-unknown-elf")
to >>>       

        return ("riscv-none-embed", "riscv-none-embed")
        
* make sure the riscv toolchain riscv-none-embed is also on the path
* build your LiteX SoC as usual

for Linux use make.py from

https://github.com/micro-FPGA/linux-on-litex-vexriscv

and prebuilt linux images from

https://github.com/litex-hub/linux-on-litex-vexriscv-prebuilt






