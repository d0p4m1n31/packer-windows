# Build a virtual machine 

1: Clone the repository to have all the scripts and files available to use

2: Make sure you have the needed local ISO files available. In this example they are in the /ISO/  folder.

3: Get the sha256 checksum of the ISO for verification, for example with Powershell: Get-FileHash <isofile> 

4: run: packer build --only=vmware-iso --var vhv_enable=true --var iso_url=/iso/en-us_windows_server_2022_updated_aug_2023_x64_dvd_78639bda.iso --var iso_checksum=sha256:E58B82C03759ECABF1875C03C7DA4D3AD51028612D6B8997BF5B2DA97BA74900 .\windows_2022.json
