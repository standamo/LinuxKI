## Directly install from git repo

To create repo directly installable from github:

````
# cd rpms
# createrepo -u https://github.com/HewlettPackard/LinuxKI/releases/download/v5.5-1/ .
# cd ..
# git add rpms/repodata
````

The corresponding repo file:

````
# cat /etc/yum.repos.d/linuxki.repo
[linuxKI]
metadata_expire = 86400
baseurl = https://raw.githubusercontent.com/standamo/LinuxKI/master/rpms
sslverify = 0
name = LinuxKI repository
enabled = 1
gpgcheck = 0
````


