#_Домашнее задание занятию "Домашнее задание к занятию "3.8. Компьютерные сети, лекция 3"_ #
##Выполнил  - Каплин Владимир ##



1. Подключитесь к публичному маршрутизатору в интернет. Найдите маршрут к вашему публичному IP
```
telnet route-views.routeviews.org
Username: rviews
show ip route x.x.x.x/32
show bgp x.x.x.x/32
```

Решение:
Определим свой внешний IP  c помощью https://whoer.net/ru. Мой IP: 95.140.26.133 

Подключимся к маршрутизщатору и выполним команды

```
route-views>show ip route 95.140.26.133
Routing entry for 95.140.24.0/21
  Known via "bgp 6447", distance 20, metric 0
  Tag 6939, type external
  Last update from 64.71.137.241 7w0d ago
  Routing Descriptor Blocks:
  * 64.71.137.241, from 64.71.137.241, 7w0d ago
      Route metric is 0, traffic share count is 1
      AS Hops 2
      Route tag 6939
      MPLS label: none
```

```
route-views>show bgp 95.140.26.133
BGP routing table entry for 95.140.24.0/21, version 293138
Paths: (23 available, best #22, table default)
  Not advertised to any peer
  Refresh Epoch 1
  8283 31133 48739
    94.142.247.3 from 94.142.247.3 (94.142.247.3)
      Origin IGP, metric 0, localpref 100, valid, external
      Community: 8283:1 8283:101
      unknown transitive attribute: flag 0xE0 type 0x20 length 0x18
        value 0000 205B 0000 0000 0000 0001 0000 205B
              0000 0005 0000 0001
      path 7FE0B9092EC8 RPKI State not found
      rx pathid: 0, tx pathid: 0
  Refresh Epoch 1
  4901 6079 31133 48739
    162.250.137.254 from 162.250.137.254 (162.250.137.254)
      Origin IGP, localpref 100, valid, external
      Community: 65000:10100 65000:10300 65000:10400
      path 7FE0D4F224D0 RPKI State not found
      rx pathid: 0, tx pathid: 0
  Refresh Epoch 1
  3333 31133 48739
    193.0.0.56 from 193.0.0.56 (193.0.0.56)
      Origin IGP, localpref 100, valid, external
      path 7FE156348FC8 RPKI State not found
      rx pathid: 0, tx pathid: 0
  Refresh Epoch 1
  101 3491 20485 20485 48739
    209.124.176.223 from 209.124.176.223 (209.124.176.223)
      Origin IGP, localpref 100, valid, external
      Community: 101:20300 101:22100 3491:300 3491:311 3491:9001 3491:9080 3491:9081 3491:9087 3491:62210 3491:62220 20485:10099
      path 7FE03C8DB660 RPKI State not found
      rx pathid: 0, tx pathid: 0
  Refresh Epoch 1
  57866 9002 9049 48739 48739 48739
    37.139.139.17 from 37.139.139.17 (37.139.139.17)
      Origin IGP, metric 0, localpref 100, valid, external
      Community: 9002:0 9002:64667
      path 7FE0FE56FD68 RPKI State not found
      rx pathid: 0, tx pathid: 0
  Refresh Epoch 1
  852 31133 48739
    154.11.12.212 from 154.11.12.212 (96.1.209.43)
      Origin IGP, metric 0, localpref 100, valid, external
      path 7FE122CCE5F0 RPKI State not found
      rx pathid: 0, tx pathid: 0
  Refresh Epoch 1
  20130 6939 48739
    140.192.8.16 from 140.192.8.16 (140.192.8.16)
      Origin IGP, localpref 100, valid, external
      path 7FE0A768BB20 RPKI State not found
      rx pathid: 0, tx pathid: 0
  Refresh Epoch 1
  1351 20764 20764 20764 20764 20764 20764 20764 20764 20764 48739 48739 48739
    132.198.255.253 from 132.198.255.253 (132.198.255.253)
      Origin IGP, localpref 100, valid, external
      path 7FE04CFBEF08 RPKI State not found
      rx pathid: 0, tx pathid: 0
  Refresh Epoch 1
  701 5511 12389 12389 12389 25478 48739 48739 48739
    137.39.3.55 from 137.39.3.55 (137.39.3.55)
      Origin IGP, localpref 100, valid, external
      path 7FDFFC8137E8 RPKI State not found
      rx pathid: 0, tx pathid: 0
  Refresh Epoch 1
  3549 3356 20485 48739
    208.51.134.254 from 208.51.134.254 (67.16.168.191)
      Origin IGP, metric 0, localpref 100, valid, external
      Community: 3356:2 3356:22 3356:100 3356:123 3356:501 3356:903 3356:2065 3549:2581 3549:30840 20485:10099
      path 7FE0DD9DDEA8 RPKI State not found
      rx pathid: 0, tx pathid: 0
  Refresh Epoch 1
  53767 174 31133 48739
    162.251.163.2 from 162.251.163.2 (162.251.162.3)
      Origin IGP, localpref 100, valid, external
      Community: 174:21101 174:22028 53767:5000
      path 7FE0C9D0FC30 RPKI State not found
      rx pathid: 0, tx pathid: 0
  Refresh Epoch 1
  3356 20485 48739
    4.68.4.46 from 4.68.4.46 (4.69.184.201)
      Origin IGP, metric 0, localpref 100, valid, external
      Community: 3356:2 3356:22 3356:100 3356:123 3356:501 3356:903 3356:2065 20485:10099
      path 7FE15DEE9310 RPKI State not found
      rx pathid: 0, tx pathid: 0
  Refresh Epoch 1
  20912 3257 174 31133 48739
    212.66.96.126 from 212.66.96.126 (212.66.96.126)
      Origin IGP, localpref 100, valid, external
      Community: 3257:8070 3257:30155 3257:50001 3257:53900 3257:53902 20912:65004
      path 7FE0C34231D8 RPKI State not found
      rx pathid: 0, tx pathid: 0
  Refresh Epoch 1
  3303 20485 48739
    217.192.89.50 from 217.192.89.50 (138.187.128.158)
      Origin IGP, localpref 100, valid, external
      Community: 3303:1004 3303:1006 3303:1030 3303:3056 20485:10099
      path 7FE1506116B0 RPKI State not found
      rx pathid: 0, tx pathid: 0
  Refresh Epoch 1
  7018 3356 20485 48739
    12.0.1.63 from 12.0.1.63 (12.0.1.63)
      Origin IGP, localpref 100, valid, external
      Community: 7018:5000 7018:37232
      path 7FE0C815E130 RPKI State not found
      rx pathid: 0, tx pathid: 0
  Refresh Epoch 1
  3561 3910 3356 20485 48739
    206.24.210.80 from 206.24.210.80 (206.24.210.80)
      Origin IGP, localpref 100, valid, external
      path 7FE0E3C705B0 RPKI State not found
      rx pathid: 0, tx pathid: 0
  Refresh Epoch 1
  7660 2516 6762 20485 48739
    203.181.248.168 from 203.181.248.168 (203.181.248.168)
      Origin IGP, localpref 100, valid, external
      Community: 2516:1030 7660:9003
      path 7FE18BC1DE68 RPKI State not found
      rx pathid: 0, tx pathid: 0
  Refresh Epoch 2
  2497 20485 48739
    202.232.0.2 from 202.232.0.2 (58.138.96.254)
      Origin IGP, localpref 100, valid, external
      path 7FE0DD21DD28 RPKI State not found
      rx pathid: 0, tx pathid: 0
  Refresh Epoch 1
  49788 12552 31133 48739
    91.218.184.60 from 91.218.184.60 (91.218.184.60)
      Origin IGP, localpref 100, valid, external
      Community: 12552:12000 12552:12100 12552:12101 12552:22000
      Extended Community: 0x43:100:1
      path 7FE1180A68C8 RPKI State not found
      rx pathid: 0, tx pathid: 0
  Refresh Epoch 1
  1221 4637 31133 48739
    203.62.252.83 from 203.62.252.83 (203.62.252.83)
      Origin IGP, localpref 100, valid, external
      path 7FE0D9902868 RPKI State not found
      rx pathid: 0, tx pathid: 0
  Refresh Epoch 1
  3257 1299 31133 48739
    89.149.178.10 from 89.149.178.10 (213.200.83.26)
      Origin IGP, metric 10, localpref 100, valid, external
      Community: 3257:8794 3257:30052 3257:50001 3257:54900 3257:54901
      path 7FE098F63D68 RPKI State not found
      rx pathid: 0, tx pathid: 0
  Refresh Epoch 1
  6939 48739
    64.71.137.241 from 64.71.137.241 (216.218.252.164)
      Origin IGP, localpref 100, valid, external, best
      unknown transitive attribute: flag 0xE0 type 0x20 length 0xC
        value 0000 21B7 0000 0777 0000 21B7
      path 7FE0173B0A98 RPKI State not found
      rx pathid: 0, tx pathid: 0x0
  Refresh Epoch 1
  19214 174 31133 48739
    208.74.64.40 from 208.74.64.40 (208.74.64.40)
      Origin IGP, localpref 100, valid, external
      Community: 174:21101 174:22028
      path 7FE0DDD80E88 RPKI State not found
      rx pathid: 0, tx pathid: 0
```

2. Создайте dummy0 интерфейс в Ubuntu. Добавьте несколько статических маршрутов. Проверьте таблицу маршрутизации.

- создадим интерфейсы и инициализируем их
```
vagrant@vagrant:~$ sudo ip link add dummy0 type dummy
vagrant@vagrant:~$ sudo ip link add dummy1 type dummy
vagrant@vagrant:~$ sudo ip link set dummy0 up
vagrant@vagrant:~$ sudo ip link set dummy1 up
```
- пропишем IP адреса
```
vagrant@vagrant:~$ sudo ip addr add 192.168.1.150/24 dev dummy0
vagrant@vagrant:~$ sudo ip addr add 192.168.2.150/24 dev dummy1
```
- проверим
```
vagrant@vagrant:~$ ifconfig
dummy0: flags=195<UP,BROADCAST,RUNNING,NOARP>  mtu 1500
        inet 192.168.1.150  netmask 255.255.255.0  broadcast 0.0.0.0
        inet6 fe80::bc3a:53ff:fee1:e195  prefixlen 64  scopeid 0x20<link>
        ether be:3a:53:e1:e1:95  txqueuelen 1000  (Ethernet)
        RX packets 0  bytes 0 (0.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 6  bytes 714 (714.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

dummy1: flags=195<UP,BROADCAST,RUNNING,NOARP>  mtu 1500
        inet 192.168.2.150  netmask 255.255.255.0  broadcast 0.0.0.0
        inet6 fe80::5ca8:96ff:fea8:4967  prefixlen 64  scopeid 0x20<link>
        ether 5e:a8:96:a8:49:67  txqueuelen 1000  (Ethernet)
        RX packets 0  bytes 0 (0.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 6  bytes 714 (714.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 10.0.2.15  netmask 255.255.255.0  broadcast 10.0.2.255
        inet6 fe80::a00:27ff:feb1:285d  prefixlen 64  scopeid 0x20<link>
        ether 08:00:27:b1:28:5d  txqueuelen 1000  (Ethernet)
        RX packets 1008  bytes 111398 (111.3 KB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 772  bytes 108082 (108.0 KB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 793  bytes 213754 (213.7 KB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 793  bytes 213754 (213.7 KB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
```

- добавим статические маршруты и проверим таблицу маршрутизации.
```
vagrant@vagrant:~$ sudo route add -net 192.168.2.0 netmask 255.255.255.0 gw 192.168.2.150
vagrant@vagrant:~$ sudo route add -net 192.168.1.0 netmask 255.255.255.0 gw 192.168.1.150

vagrant@vagrant:~$ route -n
Kernel IP routing table
Destination     Gateway         Genmask         Flags Metric Ref    Use Iface
0.0.0.0         10.0.2.2        0.0.0.0         UG    100    0        0 eth0
10.0.2.0        0.0.0.0         255.255.255.0   U     0      0        0 eth0
10.0.2.2        0.0.0.0         255.255.255.255 UH    100    0        0 eth0
192.168.1.0     192.168.1.150   255.255.255.0   UG    0      0        0 dummy0
192.168.1.0     0.0.0.0         255.255.255.0   U     0      0        0 dummy0
192.168.2.0     192.168.2.150   255.255.255.0   UG    0      0        0 dummy1
192.168.2.0     0.0.0.0         255.255.255.0   U     0      0        0 dummy1
```

3. Проверьте открытые TCP порты в Ubuntu, какие протоколы и приложения используют эти порты? Приведите несколько примеров.

Решение:

Используем команду SS, запущенную с полномочиями root

Порты в состоянии LISTEN
```
vagrant@vagrant:~$ sudo ss -tpln
State               Recv-Q              Send-Q                            Local Address:Port                              Peer Address:Port              Process
LISTEN              0                   4096                              127.0.0.53%lo:53                                     0.0.0.0:*                  users:(("systemd-resolve",pid=638,fd=13))
LISTEN              0                   128                                     0.0.0.0:22                                     0.0.0.0:*                  users:(("sshd",pid=735,fd=3))
LISTEN              0                   4096                                  127.0.0.1:8125                                   0.0.0.0:*                  users:(("netdata",pid=683,fd=45))
LISTEN              0                   4096                                    0.0.0.0:19999                                  0.0.0.0:*                  users:(("netdata",pid=683,fd=4))
LISTEN              0                   70                                    127.0.0.1:33060                                  0.0.0.0:*                  users:(("mysqld",pid=877,fd=32))
LISTEN              0                   151                                   127.0.0.1:3306                                   0.0.0.0:*                  users:(("mysqld",pid=877,fd=34))
LISTEN              0                   128                                        [::]:22                                        [::]:*                  users:(("sshd",pid=735,fd=4))
LISTEN              0                   511                                           *:80                                           *:*                  users:(("apache2",pid=6729,fd=4),("apache2",pid=6728,fd=4),("apache2",pid=6727,fd=4),("apache2",pid=6725,fd=4),("apache2",pid=2324,fd=4),("apache2",pid=2303,fd=4),("apache2",pid=2302,fd=4),("apache2",pid=2301,fd=4),("apache2",pid=2300,fd=4),("apache2",pid=2299,fd=4),("apache2",pid=689,fd=4))
```

Порты с состоянием ESTEBLISH
```
vagrant@vagrant:~$ sudo ss -tpn
State           Recv-Q           Send-Q                            Local Address:Port                              Peer Address:Port            Process
ESTAB           0                0                                     10.0.2.15:22                                    10.0.2.2:61961            users:(("sshd",pid=1770,fd=4),("sshd",pid=1730,fd=4))
ESTAB           0                0                                     10.0.2.15:22                                    10.0.2.2:59115            users:(("sshd",pid=6797,fd=4),("sshd",pid=6756,fd=4))
ESTAB           0                0                                     127.0.0.1:54874                                127.0.0.1:80               users:(("python.d.plugin",pid=953,fd=3))
ESTAB           0                0                            [::ffff:127.0.0.1]:80                          [::ffff:127.0.0.1]:54874            users:(("apache2",pid=2324,fd=10))
```

Приложения, использующие открытые сокеты - apache, ssh, python и т.д.

4. Проверьте используемые UDP сокеты в Ubuntu, какие протоколы и приложения используют эти порты?

Решение - применим команду ss с ключом -U
```
vagrant@vagrant:~$ sudo ss -uap
State               Recv-Q              Send-Q                            Local Address:Port                              Peer Address:Port              Process
UNCONN              0                   0                                     127.0.0.1:8125                                   0.0.0.0:*                  users:(("netdata",pid=683,fd=41))
UNCONN              0                   0                                 127.0.0.53%lo:domain                                 0.0.0.0:*                  users:(("systemd-resolve",pid=638,fd=12))
UNCONN              0                   0                                10.0.2.15%eth0:bootpc                                 0.0.0.0:*                  users:(("systemd-network",pid=636,fd=19))
```

Все порты закрыты, приложения, которые используют эти порты - netdata, systemd-resolve.

5. Используя diagrams.net, создайте L3 диаграмму вашей домашней сети или любой другой сети, с которой вы работали.
