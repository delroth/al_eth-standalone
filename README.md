al\_eth out-of-tree driver
==========================

`al_eth` is the driver for Amazon Annapurna Labs' Alpine NIC. Alpine SoCs are
used in a few consumer products, including some QNAP NAS appliances. This
driver source code was extracted from a Linux kernel source drop from QNAP.

The original source code was designed for Linux 4.2.8. The version in this
repository has only been tested with Linux 5.5.5.

TODO
----

* RX performance is a bit lackluster (~460Mbps).
* No 10Gbps support, or at least it's untested.
* Serdes driver should be split out into either an upstream-able module (in the
  Linux QNAP fork) or another out-of-tree module.
* Move some of the board specific stuff into DT (for example, clock/delay info
  currently hardcoded in a few places).
* Port the ethtool interface to more recent Linux APIs.
* Clean up coding style.
