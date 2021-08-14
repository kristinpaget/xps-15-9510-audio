# Linux kernel patch for XPS 15 9510 audio
The 2021-model XPS 15 appears to use the same 4-speakers-on-ALC289 audio setup as the Precision models, so the woofers do not work by default.  This patch enables the same driver quirk to allow for much better audio quality and greater volume output.\
\
Available as a .patch file (if you want to compile your own kernel) and a .deb package built from the 5.13.9 kernel using the Ubuntu configuration (minus signatures, obviously).
