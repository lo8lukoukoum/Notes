![image](https://user-images.githubusercontent.com/42563981/175800808-bbae7bc6-401d-4543-90e9-5184fd4df129.png)

sudo apt install linux-headers-5.18.0-kali2-amd64

wget https://github.com/mkubecek/vmware-host-modules/archive/workstation-16.2.3.tar.gz

tar -xzf workstation-16.2.3.tar.gz

cd vmware-host-modules-workstation-16.2.3

tar -cf vmmon.tar vmmon-only

tar -cf vmnet.tar vmnet-only

sudo cp -v vmmon.tar vmnet.tar /usr/lib/vmware/modules/source/

sudo vmware-modconfig --console --install-all



The command comes from:
https://communities.vmware.com/t5/VMware-Workstation-Pro/VM-Workstation-16-1-gt-16-2-1-on-Ubuntu-21-10-broke-everything/m-p/2913449/highlight/false#M176158


Ignore this if that work:
sudo apt install gcc build-essential linux-headers-generic linux-headers-$(uname -r)
