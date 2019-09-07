# sysinfo

Quickly gather system information and print it in an easy to consume format


## Description

Show system information for various OSes, including load, uptime, cpu information, docker version and running containers, and network information. When used with the `--connections` option it will show all established connections with hostname if possible.

(Works with: macOS, RHEL, CentOS, Ubuntu, Debian)


## Sample Output

### Linux

##### Linux Mint (as an unprivileged user, then as root)
```
chad@dev-vm:~$ sudo sysinfo.sh
------------------------------------------------------------------------
Current Date:        Tue Jul 30 22:00:54 MDT 2019
Hostname:            dev-vm
OS:                  Linux Mint 19.1 Tessa
Kernel:              Linux 4.15.0-55-generic
HW Version:          >>>FOR THIS STAT, RUN AS ROOT<<<
HW Serial:           >>>FOR THIS STAT, RUN AS ROOT<<<
HW UUID:             >>>FOR THIS STAT, RUN AS ROOT<<<
Uptime:              44 minutes
Load Average:        0.22, 0.35, 0.51
Processor:           Intel(R) Core(TM) i5-6360U CPU @ 2.00GHz
Core Count:          2
Virtual Cores:       2
Total Memory:        1.95 gigabytes
Memory Used:         494M used (of 1.9G), 1.1G unused.
Internal IP:         192.168.7.240 (Tx/Rx: 1.2 MB/25.4 MB)
External IP:         170.xx.x.xxx (170-xx-x-xxx.ut.internethost.net)
Docker Version:      >>>FOR THIS STAT, RUN AS ROOT<<<
------------------------------------------------------------------------

chad@dev-vm:~$ sudo sysinfo.sh
------------------------------------------------------------------------
Current Date:        Tue Jul 30 21:43:14 MDT 2019
Hostname:            dev-vm
OS:                  Linux Mint 19.1 Tessa
Kernel:              Linux 4.15.0-55-generic
HW Version:          innotek GmbH VirtualBox
HW Serial:           0
HW UUID:             C9061541-26F1-4D70-839E-76726F0B6CC6
Uptime:              26 minutes
Load Average:        0.14, 0.39, 0.54
Processor:           Intel(R) Core(TM) i5-6360U CPU @ 2.00GHz
Core Count:          2
Virtual Cores:       2
Total Memory:        1.95 gigabytes
Memory Used:         1.4G used (of 1.9G), 111M unused.
Internal IP:         192.168.7.240 (Tx/Rx: 411.3 KB/10.5 MB)
External IP:         170.xx.xx.xx (170-xx-xx-xx.ut.internethost.net)
Docker Version:      18.09.7
------------------------------------------------------------------------
```
##### CentOS 7

```
[chad@nuc1 ~]$ sudo ./sysinfo.sh
------------------------------------------------------------------------
Current Date:        Wed Feb 13 20:04:12 MST 2019
Hostname:            nuc1.hostname.com
OS:                  CentOS Linux release 7.6.1810 (Core)
Kernel:              Linux 3.10.0-957.1.3.el7.x86_64
HW Version:          NUC7PJYH
HW Serial:           F6BJY813003BT
HW UUID:             9fa57af8-919b-7abc-595f-44c6911d33ad
Uptime:              7 weeks, 7 hours, 50 minutes
Load Average:        0.05, 0.04, 0.05
Processor:           Intel(R) Pentium(R) Silver J5005 CPU @ 1.50GHz
Core Count:          4
Virtual Cores:       4
Total Memory:        7.23 gigabytes
Memory Used:         427M used (of 7.2G), 597M unused.
Internal IP:         192.168.7.3 (Tx/Rx: 1.6 GB/1.9 GB)
External IP:         170.xx.x.xxx (170-xx-x-xxx.ut.internethost.net)
Docker Version:      18.09.0
------------------------------------------------------------------------
```

##### CentOS 7.6
```
[chad@file ~]$ sudo ./sysinfo.sh
------------------------------------------------------------------------
Current Date:        Mon Jul 29 22:22:22 MDT 2019
Hostname:            file.hostname.com
OS:                  CentOS Linux release 7.6.1810 (Core)
Kernel:              Linux 3.10.0-957.1.3.el7.x86_64
HW Version:          Dell Inc. PowerEdge T20
HW Serial:           XXXXXXX
HW UUID:             4c4c4555-014c-3810-8908-b5a04f35b931
Uptime:              25 weeks, 4 days, 1 hour, 49 minutes
Load Average:        1.19, 1.64, 1.64
Processor:           Intel(R) Xeon(R) CPU E3-1245 v3 @ 3.40GHz
Core Count:          4
Virtual Cores:       8
Total Memory:        23.30 gigabytes
Memory Used:         5.2G used (of 23G), 532M unused.
Internal IP:         192.168.6.140 (Tx/Rx: 1.0 TiB/2.0 TiB)
External IP:         170.xx.x.xxx (170-xx-x-xxx.ut.internethost.net)
Docker Version:      18.09.1
------------------------------------------------------------------------
```

##### Ubuntu 18.04
```
chad@hostname:~$ sudo sysinfo.sh
------------------------------------------------------------------------
Current Date:        Thu Feb 14 10:18:41 MST 2019
Hostname:            hostname
OS:                  Ubuntu 18.04.2 LTS
Kernel:              Linux 4.15.0-45-generic
HW Version:          HP EliteDesk 800 G1 SFF
HW Serial:           2UA50608BT
HW UUID:             509C1380-A315-22E4-A607-645106565972
Uptime:              3 days, 10 minutes
Load Average:        0.54, 0.50, 0.49
Processor:           Intel(R) Core(TM) i5-4590 CPU @ 3.30GHz
Core Count:          4
Virtual Cores:       4
Total Memory:        15.57 gigabytes
Memory Used:         3.1G used (of 15G), 8.1G unused.
Internal IP:         172.24.76.133 (Tx/Rx: 19.6 GB/1.6 GB)
External IP:         166.xx.xxx.xx (166-xx-xxx-xx.internethost.com)
Docker Version:      18.09.0
------------------------------------------------------------------------
```

##### RHEL 7.5 (running Kubernetes)
```
[root@hostname ~]# ./sysinfo.sh
------------------------------------------------------------------------
Current Date:        Thu Feb 14 15:57:16 MST 2019
Hostname:            hostname.local
OS:                  Red Hat Enterprise Linux Server release 7.5 (Maipo)
Kernel:              Linux 3.10.0-862.el7.x86_64
HW Version:          VMware Virtual Platform
HW Serial:           VMware-42 29 a2 7e 1e 14 55 93-b5 b7 5a 73 e1 91 31 8c
HW UUID:             4229A27E-1E14-5593-B5B7-5A73E191318C
Uptime:              1 hour, 34 minutes
Load Average:        1.30, 0.71, 0.66
Processor:           Intel(R) Xeon(R) CPU E5-2690 v2 @ 3.00GHz
Core Count:          1
Virtual Cores:       2
Total Memory:        3.70 gigabytes
Memory Used:         1.4G used (of 3.7G), 110M unused.
Internal IP:         172.24.81.159 (Tx/Rx: 55.1 MiB/278.8 MiB)
External IP:         166.xx.xxx.xx (166-xx-xxx-xx.internethost.com)
Docker Version:      1.13.1
Containers:          CONTAINER ID       NAME
                     4ddcdcb1901d       k8s_nginx-ingress-ingress-controller_main-nginx-ingress-ingress-controller-6dddb4d4d7-wmjfr_ingress-nginx_3dcb6196-309f-11e9-b964-005056a91740_0
                     000f43b13d9a       k8s_nginx-ingress-default-backend_main-nginx-ingress-default-backend-764f465755-5vgdh_ingress-nginx_3dcc80a0-309f-11e9-b964-005056a91740_0
                     7eaa3e77b4ec       k8s_POD_main-nginx-ingress-ingress-controller-6dddb4d4d7-wmjfr_ingress-nginx_3dcb6196-309f-11e9-b964-005056a91740_0
                     c1a8f72b8d41       k8s_POD_main-nginx-ingress-default-backend-764f465755-5vgdh_ingress-nginx_3dcc80a0-309f-11e9-b964-005056a91740_0
                     d3969eddabf5       k8s_grafana_grafana-7f69f4ffd-97kq6_grafana_28fb9880-309f-11e9-b964-005056a91740_0
                     4145a5a5ba1f       k8s_POD_grafana-7f69f4ffd-97kq6_grafana_28fb9880-309f-11e9-b964-005056a91740_0
                     8a76098d74fa       k8s_prometheus-server_prometheus-server-77dd5bf6bb-7brn8_prometheus_105a1ed9-309f-11e9-b964-005056a91740_0
                     b332bf7a2b0f       k8s_prometheus-server-configmap-reload_prometheus-server-77dd5bf6bb-7brn8_prometheus_105a1ed9-309f-11e9-b964-005056a91740_0
                     32bc48b1c730       k8s_prometheus-alertmanager-configmap-reload_prometheus-alertmanager-7995bc8577-5vxcv_prometheus_104d8b29-309f-11e9-b964-005056a91740_0
                     2c82f5ae0708       k8s_prometheus-pushgateway_prometheus-pushgateway-648d6c8b-w7mbl_prometheus_1054d94f-309f-11e9-b964-005056a91740_0
                     9ed8a61d330d       k8s_prometheus-node-exporter_prometheus-node-exporter-8rl7s_prometheus_103d8b91-309f-11e9-b964-005056a91740_0
                     cfbd8df0bd2d       k8s_prometheus-alertmanager_prometheus-alertmanager-7995bc8577-5vxcv_prometheus_104d8b29-309f-11e9-b964-005056a91740_0
                     20be7f92f01e       k8s_prometheus-kube-state-metrics_prometheus-kube-state-metrics-64fd5b47fd-gczgx_prometheus_10580140-309f-11e9-b964-005056a91740_0
                     83af71057fd5       k8s_POD_prometheus-alertmanager-7995bc8577-5vxcv_prometheus_104d8b29-309f-11e9-b964-005056a91740_0
                     ee20fe12793e       k8s_POD_prometheus-server-77dd5bf6bb-7brn8_prometheus_105a1ed9-309f-11e9-b964-005056a91740_0
                     c9da218603ea       k8s_POD_prometheus-kube-state-metrics-64fd5b47fd-gczgx_prometheus_10580140-309f-11e9-b964-005056a91740_0
                     17e2e9c9d333       k8s_POD_prometheus-pushgateway-648d6c8b-w7mbl_prometheus_1054d94f-309f-11e9-b964-005056a91740_0
                     8aa82d6755fa       k8s_POD_prometheus-node-exporter-8rl7s_prometheus_103d8b91-309f-11e9-b964-005056a91740_0
                     ca77355305bd       k8s_coredns_coredns-86c58d9df4-bpkvp_kube-system_f6c29ae7-309e-11e9-b964-005056a91740_0
                     ec215d05c52c       k8s_tiller_tiller-deploy-dbb85cb99-zzkn7_kube-system_fe3733e8-309e-11e9-b964-005056a91740_0
                     e5506cee828b       k8s_coredns_coredns-86c58d9df4-477vf_kube-system_f6b8fc46-309e-11e9-b964-005056a91740_0
                     bb670f0e2725       k8s_POD_tiller-deploy-dbb85cb99-zzkn7_kube-system_fe3733e8-309e-11e9-b964-005056a91740_0
                     55777e8c46e4       k8s_POD_coredns-86c58d9df4-bpkvp_kube-system_f6c29ae7-309e-11e9-b964-005056a91740_0
                     edd8aa848602       k8s_POD_coredns-86c58d9df4-477vf_kube-system_f6b8fc46-309e-11e9-b964-005056a91740_0
                     b3e55601811b       k8s_weave-npc_weave-net-sk8w6_kube-system_f6b1d46d-309e-11e9-b964-005056a91740_0
                     b9123cd86e56       k8s_weave_weave-net-sk8w6_kube-system_f6b1d46d-309e-11e9-b964-005056a91740_0
                     3b47612a4ddf       k8s_kube-proxy_kube-proxy-r5v5c_kube-system_f6b250d2-309e-11e9-b964-005056a91740_0
                     58a3105eb78f       k8s_POD_weave-net-sk8w6_kube-system_f6b1d46d-309e-11e9-b964-005056a91740_0
                     bde13e5fd278       k8s_POD_kube-proxy-r5v5c_kube-system_f6b250d2-309e-11e9-b964-005056a91740_0
                     bf1e33a600dd       k8s_etcd_etcd-hostname.local_kube-system_aaf41a2de5f6054f98e8846e116191eb_0
                     f9363fcc323e       k8s_kube-scheduler_kube-scheduler-hostname.local_kube-system_b734fcc86501dde5579ce80285c0bf0c_0
                     2ba66f42e449       k8s_kube-apiserver_kube-apiserver-hostname.local_kube-system_31305a146d9b4c5aab0182840128a57d_0
                     5fa996ec393a       k8s_kube-controller-manager_kube-controller-manager-hostname.local_kube-system_43bf25263b7036f8626365f45552fdba_0
                     bffa547d97cc       k8s_POD_etcd-hostname.local_kube-system_aaf41a2de5f6054f98e8846e116191eb_0
                     120d238c154c       k8s_POD_kube-scheduler-hostname.local_kube-system_b734fcc86501dde5579ce80285c0bf0c_0
                     ebf48857e4d1       k8s_POD_kube-apiserver-hostname.local_kube-system_31305a146d9b4c5aab0182840128a57d_0
                     0f1360227707       k8s_POD_kube-controller-manager-hostname.local_kube-system_43bf25263b7036f8626365f45552fdba_0
------------------------------------------------------------------------
```

### macOS

##### Macbook Pro
```
(0) [chad@mbp:~] $ bash sysinfo.sh
------------------------------------------------------------------------
Current Date:        Wed Feb 13 20:24:18 MST 2019
Hostname:            mbp.wifi.hostname.com
OS:                  Mac OS X 10.14.2 (18C54)
Kernel:              Darwin 18.2.0
HW Version:          MacBook Pro (13-inch, 2016, Two Thunderbolt 3 ports)
HW Serial:           XXXXXXXXXXXX
HW UUID:             ABFA244E-13EF-113E-9710-5187A382D92A
Uptime:              2 days hours
Load Average:        1.89 1.93 1.82
Processor:           Intel(R) Core(TM) i5-6360U CPU @ 2.00GHz
Core Count:          2
Virtual Cores:       4
Total Memory:        8.00 gigabytes
Memory Used:         8153M used (1892M wired), 38M unused.
Internal IP:         192.168.7.10 (Tx/Rx: 179 MB/2705 MB)
Docker Version:      18.09.1
------------------------------------------------------------------------
```
##### Macbook Air Retina
```
CM-Macbook-Air:~ $ ./sysinfo.sh
------------------------------------------------------------------------
Current Date:        Sun Aug 18 15:14:47 MDT 2019
Hostname:            CM-Macbook-Air.wifi.hostname.com
OS:                  Mac OS X 10.14.6 (18G87)
Kernel:              Darwin 18.7.0
HW Version:          MacBook Air (Retina, 13-inch, 2019)
HW Serial:           XXXXXXXXXXXX
HW UUID:             44BA58F7-F498-874A-8EFB-CE2D79885C10
Uptime:              1 day hours
Load Average:        2.12 2.04 1.91
Processor:           Intel(R) Core(TM) i5-8210Y CPU @ 1.60GHz
Core Count:          2
Virtual Cores:       4
Total Memory:        8.00 gigabytes
Memory Used:         8141M used (1739M wired), 50M unused.
Internal IP:         192.168.7.11 (Tx/Rx: 354 MB/2717 MB)
------------------------------------------------------------------------
```