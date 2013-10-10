TAMUDrivers
===========

Customized drivers for optical gigabit network cards used for electronics development in TAMU CMS group

So far, three kinds of network cards were used:
- D-Link DGE-550SX - Revision 0c
   - based on DL2000 chip, PCI Vendor ID 0x1186, Device ID 0x4000 (use lspci -nn)
   - older card, originally used for VME control for CSC detectors
   - almost impossible to find for sale
   - runs with dl2k linux driver
   - in *SL4/dl2k/* and *SL5/dl2k/* directories corresponding to kernels used in Scientific Linux 4 and 5
- D-Link DGE-550SX - Revision b1
   - Based on Marvel 88E8022 chip? Vendor ID 0x1186, Device ID 0x4001
   - a newer revision, but now is also hard to find
   - runs with sk98lin (in older kernels) or sky2 (newer kernels) linux drivers
   - in *SL4/sk98lin/* and *SL5/sky2/* directories
- Intel I350-F2 (rev 01)
   - Intel ?? chip Vendor ID 0x8086, DeviceID 0x1522
   - The newest card (as of 2013) used by CSC folks
   - [Link to intel's page](http://www.intel.com/content/www/us/en/network-adapters/gigabit-network-adapters/ethernet-server-adapter-i350.html)
   - PCIE slot
   - Runs with igp driver, which was modified and renamed to igp_emu
   - in *SL5/igp* directory

From the D-Link's [manual](http://www.dlink.com/uk/en/support/product/dge-550sx-pci-bus-fiber-sc-connector-gigabit-ethernet-adapter):
they could be installed into a 32 or 64 bit PCI/PCI-X slot with various supported frequences, with the best performance with a 64-bit/133 MHz bus.
