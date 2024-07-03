## K3Raid


> Install Steps

1. Git clone this repo to your unraid's `/boot/k3raid`

2. Download k3s binary to `/boot/k3raid/k3s`

3. Edit `/boot/k3raid/kof` which contains your k3s startup commands

4. Last step, edit your `/boot/config/go` file, add a line of code: `bash /boot/k3raid/k3raid init`


> Usage Notice

1. Ensure docker engine enabled, cause we reuse unraid's docker lifetime event in this version

2. After start, you can find k3s in `/home/k3s`, *DO NOT REMOVE THESE FILES !!!*

3. All data are located in `/mnt/disk1/system/k3s`, you can change it by edit `k3raid` file
