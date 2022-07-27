
## debian
```
sudo virt-install --name debian \
--ram 8192 \
--disk path=images/debian.img,size=250 \
--vcpus 4 \
--os-variant debian10 \
--network bridge=br0 \
--graphics none \
--console pty,target_type=serial \
--location iso/debian-11.3.0-amd64-DVD-1.iso \
--extra-args 'console=ttyS0,115200n8 serial'
```

## ubuntu

```
virt-install --name ubuntu \
--ram 8192 \
--disk path=images/ubuntu2004.img,size=250 \
--vcpus 4 \
--os-variant ubuntu20.04 \
--network bridge=br0 \
--graphics none \
--console pty,target_type=serial \
--location /home/microfixer/iso/ubuntu-20.04.4-live-server-amd64.iso,kernel=casp                                                                                                                                                             er/vmlinuz,initrd=casper/initrd \
--extra-args 'console=ttyS0,115200n8 serial'
```
