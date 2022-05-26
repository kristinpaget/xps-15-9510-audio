# Linux kernel patch for XPS 15 9510 audio
The 2021-model XPS 15 appears to use the same 4-speakers-on-ALC289 audio setup as the Precision models, so the woofers do not work by default.  This patch enables the same driver quirk to allow for much better audio quality and greater volume output.\
\
Available as a .patch file (if you want to compile your own kernel) and a .deb package built from the 5.13.9 kernel using the supplied Ubuntu configuration (minus signatures, obviously). It's included in the mainline kernel as of 5.14-rc7.\
\
For folks looking to patch their own machines in similar ways, the ID numbers in the patch are the PCI SubVendor and SubDevice. Run \
`lspci -vmnn` \
and look for your audio controller, it's likely to be at address 00:1f.3.  You want SVendor (likely 0x1028 for Dell machines) and SDevice; modify sound/pci/hda/patch_realtek.c accordingly.
