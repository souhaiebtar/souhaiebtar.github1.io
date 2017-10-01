---
title: install parallels tools on centos 7
layout: post
---

after installing centos 7 (for testing purposes) on Parallels desktop, i run into a problem, parallels tools won't install either using gui or terminal,

at least on terminal it show missing dependency
those are 2
dkms
selinux-policy-devel

to install them

```curl -O https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm```

 yum clean metadata dbcache

 yum install epel-release-latest-7.noarch.rpm

 yum-config-manager --disable epel
 yum --enablerepo=epel install dkms

 yum install selinux-policy
 yum install selinux-policy-devel

 than navigate to the folder
 for me it was
 /run/media/root/parallels tools/

 then
 ./install
 and say yes

 it will install enjoy
