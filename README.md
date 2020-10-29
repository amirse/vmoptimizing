# Stuff to do on servers

1. Disable ksm (Kernel Samepage merging)
  * ```systemctl disable ksmd```
  * ```systemctl disable ksmtuned```
2. Disable transparent hugepages
  * add ```transparent_hugepage=never``` to grub cmd line and remake grub.cfg
3. Enable 1G hugepages
  * add ```default_hugepagesz=1G hugepagesz=1G hugepages=X``` to grub.cfg. X = total_ram_in_gb-32
4. Configure KVM machines to use hugepages
  * add ```<memoryBacking> <hugepages/> </memoryBacking>``` to vm's XML
  

