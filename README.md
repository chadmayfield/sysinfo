# sysinfo

Quickly gather system information and print it in an easy to consume format


## Description

Show system information for various OSes, including load, uptime, cpu information, docker version and running containers, and network information. When used with the `--connections` option it will show all established connections with hostname if possible.

(Works with: macOS, RHEL, CentOS, Ubuntu, Debian)

Apple macOS Sierra
```
macbookpro:~ $ ./sysinfo.sh --connections 
------------------------------------------------------------------------
Current Date:        Fri Apr  7 18:59:43 MDT 2017
Hostname:            macbookpro.local
OS:                  Mac OS X 10.12.4 (16E195)
Kernel:              Darwin 16.5.0
HW Version:          MacBook Pro (13-inch, 2016, Two Thunderbolt 3 ports)
HW Serial:           8SF79S7DA9SF
HW UUID:             6EB1244E-BC1F-323A-9724-5AB7B382D921
Uptime:              21:01 hours
Load Average:        1.34 1.37 1.28
Processor:           Intel(R) Core(TM) i5-6360U CPU @ 2.00GHz
Core Count:          2
Virtual Cores:       4
Total Memory:        8.00 gigabytes
Memory Used:         7956M used (1864M wired), 234M unused.
Internal IP:         192.168.110.213 (Tx/Rx: 94544383 bytes)
External IP:         166.72.33.98 (166-72-33-98.xmission.com)
Docker Version:      17.03.1-ce
Containers:          CONTAINER ID       NAME 
                     b22c0ef58f62	confident_bose
                     50b7deb5898f	loving_torvalds
Current Connections: 192.168.110.213
                     173.194.196.109 (ix-in-f109.1e100.net.)
                     34.192.55.128 (ec2-34-192-55-128.compute-1.amazonaws.com.)
                     40.97.150.242
                     52.2.45.245 (ec2-52-2-45-245.compute-1.amazonaws.com.)
                     54.84.82.15 (ec2-54-84-82-15.compute-1.amazonaws.com.)
                     65.52.108.204 (msnbot-65-52-108-204.search.msn.com.)
                     74.125.202.108 (io-in-f108.1e100.net.)
------------------------------------------------------------------------
``` 

Red Hat Enterprise Linux 7.3
```
[chad@fileserver ~]$ ./sysinfo.sh --connections 
------------------------------------------------------------------------
Current Date:        Fri Apr  7 18:57:35 MDT 2017
Hostname:            fileserver.local
OS:                  Red Hat Enterprise Linux Server release 7.3 (Maipo)
Kernel:              Linux 3.10.0-514.10.2.el7.x86_64
HW Version:          Dell Inc. PowerEdge T20
HW Serial:           None
HW UUID:             4C4C6544-0082-3610-8056-B4C04FY05A21
Uptime:              29 days hours
Load Average:        0.00, 0.02, 0.05
Processor:           Intel(R) Xeon(R) CPU E3-1245 v3 @ 3.40GHz
Core Count:          4
Virtual Cores:       8
Total Memory:        23.30 gigabytes
Memory Used:         1.2G used (of 23G), 6.5G unused. 
Internal IP:         192.168.110.30 (Tx/Rx: 121.3 GiB)
External IP:         166.72.33.98 (166-72-33-98.xmission.com)
Docker Version:      1.12.6
Containers:          CONTAINER ID       NAME 
                     d4199824e0a5	plex
                     1b92338bbb80	unifi
Current Connections: 192.168.110.3
                     52.41.5.6 (ec2-52-41-5-6.us-west-2.compute.amazonaws.com.)
                     52.41.5.6 (ec2-52-41-5-6.us-west-2.compute.amazonaws.com.)
                     52.41.5.6 (ec2-52-41-5-6.us-west-2.compute.amazonaws.com.)
                     192.168.110.213
------------------------------------------------------------------------
```
