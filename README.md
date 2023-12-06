# Jarkom-Modul-4-IT23-2023
**Praktikum Jaringan Komputer Modul 4**

## Author
| Nama | NRP |
|---------------------------|------------|
|Rendy Anfi Yudha| 5027211006 |
|Dhea Arfryza Ananda P. | 5027211013 |

# Laporan Resmi
## Daftar Isi
[Rute](#rute)

[A. VLSM](#VLSM)
- [Topologi VLSM](#topologivlsm)
- [Pembagian IP - VLSM](#pembagianipvlsm)
- [Tree VLSM](#tree-vlsm)
- [Konfigurasi Router](#konfigurasi-router)
- [Konfigurasi Client PC](#konfigurasi-client-pc)
- [Routing](#routing)
- [Ping VLSM](#ping-vlsm)


[B. CIDR](#CIDR)
- [Topologi CIDR](#topologicidr)
- [Penggabungan - CIDR](#penggabungancidr)
- [Pembagian IP](#pembagianip)

### Rute
| Nama Subnet | Rute | Jumlah IP | Netmask |
|---------|---------------------------|---------|---------|
| A1 | Fern-Switch4-LaubHills-AppetitRegion	| 1023 |	/21 |
| A2 |	Fern-Flamme |	2 |	/30 |
| A3	| Flamme-Switch5-RohrRoad |	1001|	/22 |
| A4 |	Flamme-Himmel	| 2	| /30 |
| A5 |	Himmel-Switch6-SchwerMountains | 6 |	/29 |
| A6	| Flamme-Frieren |	2	| /30 |
| A7 |	Frieren-Switch3-LakeKorridor |	25 |	/27 |
| A8 |	Frieren-Aura |	2 |	/30 |
| A9 |	Aura-Denken |	2 |	/30 |
| A10 |	Denken-Switch2-RoyalCapital-WilleRegion |	127 |	/24 |
| A11 |	Aura-Eisen | 2 |	/30 |
| A12 |	Eisen-Switch0-Stark |	2 |	/30 |
| A13	| Eisen-Switch1-Richter-Revolte |	3 |	/29 |
| A14	| Eisen-Lugner |	2 |	/30 |
| A15 |	Lugner-Switch10-TurkRegion |	1001 |	/22 |
| A16	| Lugner-Switch9-GrobeForest	| 251 |	/24 |
| A17	| Eisen-Linie |	2 |	/30 |
| A18	| Linie-Switch11-GranzChannel |	255 |	/23 |
| A19 |	Linie-Lawine	| 2	| /30 |
| A20	| Lawine-Switch7-BredtRegion-Heiter |	31 |	/26 |
| A21	| Heiter-Switch8-RiegelCanyon-Sein |	512	| /22 |
| Total | | 4255 | |

### Topologi VLSM

![topo vlsm](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/94961661/b49f1cbf-2a93-45df-90ab-03282ff9b50a)

### Pembagian IP - VLSM

| Subnet | Network ID    | Subnet Mask         | Broadcast        | Netmask | Jumlah IP |
|--------|---------------|---------------------|------------------|---------|-----------|
| A1     | 10.75.0.0     | 255.255.248.0       | 10.75.7.255      | /21     | 1023      |
| A2     | 10.75.144.0   | 255.255.255.252     | 10.75.144.3      | /30     | 2         |
| A3     | 10.75.8.0     | 255.255.252.0       | 10.75.11.255     | /22     | 1001      |
| A4     | 10.75.148.0   | 255.255.255.252     | 10.75.148.3      | /30     | 2         |
| A5     | 10.75.128.0   | 255.255.255.248     | 10.75.128.7      | /29     | 6         |
| A6     | 10.75.152.0   | 255.255.255.252     | 10.75.152.3      | /30     | 2         |
| A7     | 10.75.192.0   | 255.255.255.224     | 10.75.192.31     | /27     | 25        |
| A8     | 10.75.156.0   | 255.255.255.252     | 10.75.156.3      | /30     | 2         |
| A9     | 10.75.160.0   | 255.255.255.252     | 10.75.160.3      | /30     | 2         |
| A10    | 10.75.24.0    | 255.255.255.0       | 10.75.24.255     | /24     | 127       |
| A11    | 10.75.164.0   | 255.255.255.252     | 10.75.164.3      | /30     | 2         |
| A12    | 10.75.168.0   | 255.255.255.252     | 10.75.168.30     | /30     | 2         |
| A13    | 10.75.136.0   | 255.255.255.248     | 10.75.136.7      | /29     | 3         |
| A14    | 10.75.172.0   | 255.255.255.252     | 10.75.172.3      | /30     | 2         |
| A15    | 10.75.12.0    | 255.255.252.0       | 10.75.15.255     | /22     | 1001      |
| A16    | 10.75.25.0    | 255.255.255.0       | 10.75.25.255     | /24     | 251       |
| A17    | 10.75.176.0   | 255.255.255.252     | 10.75.176.3      | /30     | 2         |
| A18    | 10.75.20.0    | 255.255.254.0       | 10.75.21.255     | /23     | 255       |
| A19    | 10.75.180.0   | 255.255.255.252     | 10.75.180.3      | /30     | 2         |
| A20    | 10.75.64.0    | 255.255.255.192     | 10.75.64.63      | /26     | 31        |
| A21    | 10.75.216.0   | 255.255.252.0       | 10.75.219.255    | /22     | 512       |

### Tree-VLSM   
![Vlsm-tree](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/94961661/17eabe36-25d1-468f-9938-b6fef7134d07)

### Konfigurasi Router
Setelah dilakukan pembagian IP lakukan set up pada setiap router sesuai dengan netmask dan subnet yang tertera pada tabel di atas.

Misalnya pada router Aura di subnet A9, maka sebagai berikut:
![config-ip](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/94961661/4dcbcc92-0811-442b-a5f3-fd505cf4f03b)

Lakukan hal yang sama pada router lainnya, sesuai dengan subnet dan netmask yang telah ditentukan.

### Konfigurasi Client PC
Seperti halnya router untuk client(PC) di setiap subnet juga harus diatur IP nya sesuai dengan subnet yang telah ditentukan.

Misalnya pada client PC(RoyalCapital) di subnet A10, maka sebagai berikut:
![config-pc](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/94961661/8a9584ef-5180-4b0a-981a-5fcf33430f61)
masukkan IP yang tersedia di subnet A10 dan netmask yang telah ditentukan. jangan lupa untuk memasukkan gateway yang mengarah ke ip pertama di subnet A10. lakukan hal yang sama pada client PC lainnya sesuai dengan subnet yang telah ditentukan.

### Routing
Untuk melakukan routing, pada setiap router masukkan network id setiap subnet ke router yang akan dihubungkan dan dilakukan secara bolak balik, contoh routing untuk aura adalah sebagai berikut:
![routing](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/94961661/0c59defa-32c9-41bc-a699-ea16057fba06)

Namun terkadang kita perlu menambahkan routing wildcard dari semua ip yang keluar dari salah satu router untuk agar bisa kembali ke router utama, seperti contoh berikut:
![wildcardroute](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/94961661/e314c242-4438-43bf-9f3d-9d260fc3ff52)

### Ping VLSM
Berikut adalah hasil uji coba ping untuk testcase yang telah diberikan.
![testcase1](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/94961661/8fe4ad8a-1893-4d3e-a500-35f8b8534c97)

![testcase2](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/94961661/46c97cbd-2b6b-4f06-8983-d33173a20c6d)


### Topologi CIDR

![topo gns3](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/89828723/e51f7853-b945-46f8-9ae7-79a7899d7471)

### Penggabungan - CIDR

#### Subnetting A

![A](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/89828723/243fb82d-ce3e-4095-8741-3c63df7275d9)

#### Subnetting B

![B](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/89828723/873d96e3-970a-4540-8432-a0a42587c2f8)

#### Subnetting C

![C](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/89828723/9180807c-fb28-4848-83dd-818e22cd1533)

#### Subnetting D

![D](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/89828723/10430547-76f9-4711-9a42-260f78f0bc30)

#### Subnetting E

![E](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/89828723/0128a025-40c9-472f-be52-2c041d937ac5)

#### Subnetting F

![F](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/89828723/44859b51-f4d7-4836-ac88-141f0a05f952)

#### Subnetting G

![G](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/89828723/7e475cae-cbf0-4e02-93d9-1c11a4f641fc)

#### Subnetting H

![H](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/89828723/719f89ad-694f-4cc6-8446-bd6a31bb2ed0)

#### Subnetting I

![I](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/89828723/36d8ec38-a74d-4e92-896c-e5ac94dc1aea)

Setelah menentukan subnetting pada topologi nya, dilakukan penggabungan berdasarkan subnetting diatas

![1](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/89828723/93317af9-4106-41c6-bd9f-1e1bfa452ae4)

![2](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/89828723/bee3abc4-5042-4e1f-880f-b1206d074a73)

![3](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/89828723/331758f5-db77-4b23-805d-c488c6d4df99)

![4](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/89828723/ab303055-89db-4a04-a34f-ff58181ffb61)

![5](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/89828723/e73d6531-0d46-4b33-a8e5-9f8a72b9a25f)

![6](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/89828723/01c5d028-a336-4da2-9d0c-a4d138a11833)

![7](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/89828723/713b67cc-5de8-48d2-833c-6a23bb22e30a)

![8](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/89828723/764d878b-9d63-400b-806f-8c414b84e312)

### Tree
Selanjutnya melakukan pembagian IP dengan menggunakan tree (pohon) :

![Salinan modul4 drawio](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/89828723/065d4272-a5b2-4c3a-841e-1ff7f7e37b9c)

### Pembagian IP

![pembagian ip](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/89828723/b3c9bf31-cb15-4fdf-9fce-a8fda56fd883)

Melakukan routing pada GNS3, dengan perintah:
``` route add -net <NID subnet> netmask <netmask> gw <IP gateway> ```

Berikut konfigurasi network
#### Aura
```
auto eth0
iface eth0 inet dhcp

#A11 Aura-Eisen
auto eth1
iface eth1 inet static
	address 10.75.16.1
	netmask 255.255.255.252

#A9 Aura-Denken
auto eth2
iface eth2 inet static
	address 10.75.128.1
	netmask 255.255.255.0

#A8 Aura-Frieren
auto eth3
iface eth3 inet static
	address 10.78.0.1
	netmask 255.255.255.252
```

#### Denken
```
#A9 Denken-Aura
auto eth0
iface eth0 inet static
	address 10.75.128.2
	netmask 255.255.255.0

#A10 Denken-Switch-RoyalCapital-Switch-WileRegion
auto eth1
iface eth1 inet static
	address 10.75.32.1
	netmask 255.255.255.0
```

#### Eisen
```
#A11 Eisen-Aura
auto eth0
iface eth0 inet static
	address 10.75.16.2
	netmask 255.255.255.252

#A12 Eisen-Switch-Stark
auto eth1
iface eth1 inet static
	address 10.75.8.1
	netmask 255.255.255.252

#A13 Eisen-Switch1-Richter-Revolte
auto eth2
iface eth1 inet static
	address 10.75.8.2
	netmask 255.255.255.248

#A14 Eisen-Lugner
auto eth3
iface eth3 inet static
	address 10.75.0.2
	netmask 255.255.255.252
 ```

Berikut static routing di GNS3 untuk menghubungkan semua subnet:
- Aura
```
Ke Denken
route add -net 10.75.32.0 netmask 255.255.255.0 gw 10.75.128.2

Ke Eisen
route add -net 10.75.16.0 netmask 255.255.255.252 gw 10.75.16.2

Ke TurkRegion
route add -net 10.75.0.4 netmask 255.255.255.0 gw 10.75.16.2

Ke GrobeForest
route add -net 10.75.64.0 netmask 255.255.255.0 gw 10.75.16.2

Ke GranzChannel
route add -net 10.75.66.0 netmask 255.255.254.0 gw 10.75.16.2
```

- Denken
```
Ke Aura
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.75.128.2
```

- Eisen
```
Ke Aura
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.75.128.2

Ke TurkRegion
route add -net 10.75.0.4 netmask 255.255.255.0 gw 10.75.0.2

Ke GrobeForest
route add -net 10.75.64.0 netmask 255.255.255.0 gw 10.75.0.2

Ke GranzChannel
route add -net 10.75.66.0 netmask 255.255.254.0 gw 10.75.65.2
```

- Lugner
```
Ke Eisen
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.75.0.1

Ke GrobeForest
route add -net 10.75.64.0 netmask 255.255.255.0 gw 10.75.64.2

Ke TurkRegion
route add -net 10.75.0.4 netmask 255.255.255.0 gw 10.75.0.5
```

- Linie
```
Ke Eisen
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.75.65.1
```


### Testing PING

#### Aura - Eisen

![aura-eisen](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/89828723/39a98c5e-2120-4304-b261-85fc6cddbdd7)

#### GrobeForest - GranzChannel

![grob-granz](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/89828723/8144ca73-9163-40b3-a83a-bed1755d6cc6)


