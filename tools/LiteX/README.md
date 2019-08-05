It is recommended for all FPGA host boards with CRUVI slots provide LiteX platform support files.

WiP list of platforms provided at https://github.com/micro-FPGA/litex-boards

| Board         | FPGA       |Stat|variant|FPGA build|Test|SDRAM|
|---------------|------------|----|-----|-|-|--|
|TE0890 S7-mini |Spartan-7   |beta|min  |OK|OK|-hyper|
|MEGA65         |Artix-7     |    |     | | | |
|TE0710         |Artix-7     |wip |full |pass| | |
|TE0711         |Artix-7     |wip |full |OK|OK|n/a|
|TE0712         |Artix-7     |wip |     | | | |
|TE0713         |Artix-7     |wip |     | | | |
|TE0714         |Artix-7     |wip |     | | |n/a|
|TE0725         |Artix-7     |wip |     | | |-hyper|
|TE0741         |Kintex-7    |wip |?    |pass||n/a|
|MAX1000        |MAX-10      |wip |min  |OK|OK|OK|
|AnalogMAX      |MAX-10      |    |min  ||||
|AnalogMAX DAQ1 |MAX-10      |    |min  ||||
|AnalogMAX DAQ2 |MAX-10      |    |min  ||||
|CYC1000        |Cyclone 10LP|    |?    ||||
|C10LPRefKit    |Cyclone 10LP|wip |full |OK|OK|OK|
|TEI0006        |Cyclone 10GX|    |     ||||

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
        
* make sure the riscv toolchanin is also on the path
* build your LiteX SoC as usual

