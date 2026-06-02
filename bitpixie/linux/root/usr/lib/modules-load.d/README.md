# modules-load.d

The service `modules` with path `/etc/init.d/modules` loads all kernel
modules (at boot time) defined in `.conf` files which are defined in the
directories `/lib/modules-load.d/*.conf` and `/usr/lib/modules-load.d/*.conf`.

The file `virtio.conf` is shown as an example for a virtual passthrough
network. This could also be done manually in a bootstrapped initramfs as
follows:

```
$ modprobe virtio-pci virtio_net
$ ip a
$ ifup eth0
```
