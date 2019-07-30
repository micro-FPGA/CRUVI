CRUVI adpaters for ADI SDP interface

Both to-from adapters would be smart translating ones, most likely using Intel MAX10 as the prtocol conversion and pin function multiplexer.

Note: for SDP-to-CRUVI SDP pins that connec to FTDI channel A on SDP-S should be connected to MAX10 hardware JTAG (with JTAG muxing controlled by dip switch). This would allow access to the MAX10 JTAG using SDP-S (may have to replace the drivers).
