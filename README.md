TAMUDrivers
===========

Drivers for optical gigabit network cards used for electronics development in TAMU CMS group

So far, network cards of two types were used:
- D-Link DGE-550SX - Revision 0c
   - based on DL2000 chip, PCI Vendor ID 0x1186, Device ID 0x4000 (use lspci -nn)
   - older card, originally used for VME control for CSC detectors
   - almost impossible to find for sale
   - runs with dl2k linux driver
- D-Link DGE-550SX - Revision b1
   - Based on Marvel 88E8022 chip? Vendor ID 0x1186, Device ID 0x4001
   - a newer revision, but now is also hard to find
   - runs with sk98lin (in older kernels) or sky2 (newer kernels) linux drivers

From the [manual](http://www.dlink.com/uk/en/support/product/dge-550sx-pci-bus-fiber-sc-connector-gigabit-ethernet-adapter):
they could be installed into a 32 or 64 bit PCI/PCI-X slot with various supported frequences, with the best performance with a 64-bit/133 MHz bus.
