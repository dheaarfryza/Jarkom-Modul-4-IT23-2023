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

Setelah menentukan subnetting pada topologi nya, selanjutnya melakukan pembagian IP dengan menggunakan tree (pohon) :

![Salinan modul4 drawio](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/89828723/065d4272-a5b2-4c3a-841e-1ff7f7e37b9c)

### Pembagian IP

![pembagian ip](https://github.com/dheaarfryza/Jarkom-Modul-4-IT23-2023/assets/89828723/b3c9bf31-cb15-4fdf-9fce-a8fda56fd883)

Melakukan routing pada GNS3, dengan perintah:
``` route add -net <NID subnet> netmask <netmask> gw <IP gateway> ```

Berikut static routing di GNS3 untuk menghubungkan semua subnet:
### Aura

### Denken

### Eisen

