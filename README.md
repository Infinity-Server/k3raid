## K3Raid


> Install Steps

1. Git clone this repo to your unraid's `/boot/k3raid`

2. Download k3s binary to `/boot/k3raid/k3s`

3. Edit `/boot/k3raid/kof` which contains your k3s startup commands like this:

```bash
#!/bin/bash
$K3S \
  server \
  --disable=traefik \
  --flannel-ipv6-masq \
  --cluster-cidr='10.42.0.0/16,fdbd:cafe:42:0::/56' \
  --service-cidr='10.43.0.0/16,fdbd:cafe:43:0::/112'
```

4. Last step, edit your `/boot/config/go` file, add a line of code: `bash /boot/k3raid/k3raid init`


> Usage Notice

1. After OS start, you can control k3raid using `/etc/rc.d/rc.k3s`

2. All data are located in `/mnt/disk1/system/k3raid` by default

3. Traefik use port `80/443` by default, which may conflict with emhttpd, use with caution
