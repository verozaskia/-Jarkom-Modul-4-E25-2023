# Jarkom-Modul-4-E25-2023
Berikut adalah laporan resmi untuk pengerjaan Praktikum Modul 4 Subnetting dan Routing
## Anggota Kelompok E25
| Nama | NRP |
| --- | --- |
| Zakia Kolbi | 5025211049 |
| Ketut Arda Putra Mahotama Sadha | 5025211235 |

# Daftar Isi
- [Topologi](#topologi)
- [VLSM](#Dokumentasi-Pengerjaan-VLSM-di-CPT)
- [CIDR](#Dokumentasi-Pengerjaan-CIDR-di-GNS3)

## Topologi

![Screenshot 2023-11-28 235649](https://github.com/verozaskia/-Jarkom-Modul-4-E25-2023/assets/108173647/006c5720-ec90-430e-8f5e-d9225b862bf0)

## Dokumentasi Pengerjaan VLSM di CPT

### Subnetting VLSM
Menentukan rute dan jumlah subnet pada topologi.

![CIDR-Page-2 drawio](https://github.com/verozaskia/-Jarkom-Modul-4-E25-2023/assets/108173647/1bd27f18-2003-48da-890e-69c87558d3f0)

Menentukan jumlah alamat IP yang dibutuhkan oleh tiap subnet.

| Subnet | Jumlah IP | Netmask |
| --- | --- | --- |
| A1 | 1023 | /21 |
| A2 | 2 | /30 |
| A3 | 25 | /27 |
| A4 | 1001 | /22 |
| A5 | 2 | /30 |
| A6 | 2 | /30 |
| A7 | 2 | /30 |
| A8 | 127 | /24 |
| A9 | 6 | /29 |
| A10 | 3 | /29 |
| A11 | 2 | /30 |
| A12 | 2 | /30 |
| A13 | 2 | /30 |
| A14 | 1001 | /22 |
| A15 | 2 | /30 |
| A16 | 32 | /26 |
| A17 | 2 | /30 |
| A18 | 512 | /22 |
| A19 | 255 | /23 |
| A20 | 2 | /30 |
| A21 | 250 | /24 |
| Total | 4255 | /19 |

### Tree VLSM

Setelah itu, lakukan pembagian IP untuk VLSM dengan melakukan pembuatan tree

Dari Tree di atas akan mendapat pembagian IP sebagai berikut

![a3](https://github.com/verozaskia/-Jarkom-Modul-4-E25-2023/assets/108173647/043a587e-4ab3-435e-99e0-a5d36a71b659)


## Configuration VLSM

## Dokumentasi Pengerjaan CIDR di GNS3

### Subnetting CIDR
Menentukan rute dan jumlah subnet pada topologi.

![CIDR-Page-2 drawio](https://github.com/verozaskia/-Jarkom-Modul-4-E25-2023/assets/108173647/1bd27f18-2003-48da-890e-69c87558d3f0)

Setelah menentukan rute dan jumlah subnet, lakukan Penggabungan rute hingga menjadi satu kesatuan agar dapat dibuat pembagian IP CIDR

![Gabung1](https://github.com/verozaskia/-Jarkom-Modul-4-E25-2023/assets/108173647/9312d4d4-5690-4af8-b0a7-d3653142ab3b)

![gabung2](https://github.com/verozaskia/-Jarkom-Modul-4-E25-2023/assets/108173647/7588c61a-8c3f-483c-9f72-a685fb809170)

![gabung3](https://github.com/verozaskia/-Jarkom-Modul-4-E25-2023/assets/108173647/dfd23ad2-60d2-4113-b691-73ab50f23adb)

#### Hasil Penggabungan

![CIDR drawio](https://github.com/verozaskia/-Jarkom-Modul-4-E25-2023/assets/108173647/823a1954-7bff-4185-9e49-8cb9b7eb20b3)

Menentukan jumlah alamat IP yang dibutuhkan oleh tiap subnet.

| Subnet | Jumlah IP | Netmask |
| --- | --- | --- |
| A1 | 1023 | /21 |
| A2 | 2 | /30 |
| A3 | 25 | /27 |
| A4 | 1001 | /22 |
| A5 | 2 | /30 |
| A6 | 2 | /30 |
| A7 | 2 | /30 |
| A8 | 127 | /24 |
| A9 | 6 | /29 |
| A10 | 3 | /29 |
| A11 | 2 | /30 |
| A12 | 2 | /30 |
| A13 | 2 | /30 |
| A14 | 1001 | /22 |
| A15 | 2 | /30 |
| A16 | 32 | /26 |
| A17 | 2 | /30 |
| A18 | 512 | /22 |
| A19 | 255 | /23 |
| A20 | 2 | /30 |
| A21 | 250 | /24 |
| Total | 4255 | /19 |

### Tree CIDR

Setelah mendapatkan penggabungan CIDR lakukan pembagian IP untuk CIDR dengan melakukan pembuatan tree untuk pembagian CIDR.

Dari Tree di atas akan mendapat pembagian IP sebagai berikut

![a1](https://github.com/verozaskia/-Jarkom-Modul-4-E25-2023/assets/108173647/aae2e2e0-b5a5-4dc3-9fbe-24fcdb79d2d5)
![a2](https://github.com/verozaskia/-Jarkom-Modul-4-E25-2023/assets/108173647/dd1dce1d-188c-4a70-a5ed-f7085cd2194d)

## Configuration CIDR

### Router
- Aura

```
auto eth0
iface eth0 inet dhcp

#A11 Aura-Eisen
auto eth1
iface eth1 inet static
	address 10.49.73.49
	netmask 255.255.255.252

#A7 Aura-Denken
auto eth2
iface eth2 inet static
	address 10.49.73.53
	netmask 255.255.255.252

#A6 Aura-Frieren
auto eth3
iface eth3 inet static
	address 10.49.73.45
	netmask 255.255.255.252
```

- Frieren

```
#A6 Aura-Frieren
auto eth0
iface eth0 inet static
	address 10.49.73.46
	netmask 255.255.255.252
	gateway 10.49.73.45

#A3 Frieren-PC Lake Korridor
auto eth1
iface eth1 inet static
	address 10.49.73.1
	netmask 255.255.255.252

#A5 Frieren-Flamme
auto eth2
iface eth2 inet static
	address 10.49.20.33
	netmask 255.255.255.224
```

- Flamme

```
#A5 Frieren-Flamme
auto eth0
iface eth0 inet static
	address 10.49.20.34
	netmask 255.255.255.252
	gateway 10.49.20.33

#A2 Flamme-Fern
auto eth1
iface eth1 inet static
	address 10.49.8.1
	netmask 255.255.255.252

#A4 Flamme-PC Rohr Road
auto eth2
iface eth2 inet static
	address 10.49.16.1
	netmask 255.255.252.0

#A20 Flamme-Himmel
auto eth3
iface eth3 inet static
	address 10.49.20.17
	netmask 255.255.255.252
```

- Fern

```
#A2 Flamme-Fern
auto eth0
iface eth0 inet static
	address 10.49.8.2
	netmask 255.255.255.252
	gateway 10.49.8.1

#A1 Fern-PC Laub Hills, PC Appetit Region
auto eth1
iface eth1 inet static
	address 10.49.0.1
	netmask 255.255.248.0
```

- Himmel

```
#A20 Flamme-Himmel
auto eth0
iface eth0 inet static
	address 10.49.20.18
	netmask 255.255.255.252
	gateway 10.49.20.17

#A9 Himmel-PC Schwer Mountains
auto eth1
iface eth1 inet static
	address 10.49.20.1
	netmask 255.255.255.248
```

- Denken

```
#A7 Aura-Denken
auto eth0
iface eth0 inet static
	address 10.49.73.54
	netmask 255.255.255.252
	gateway 10.49.73.53

#A8 Denken-PC Royal Capital, PC Wille Region
auto eth1
iface eth1 inet static
	address 10.49.72.1
	netmask 255.255.255.0
```

- Eisen

```
#A11 Aura-Eisen
auto eth0
iface eth0 inet static
	address 10.49.73.50
	netmask 255.255.255.252
	gateway 10.49.73.49

#A12 Eisen-Stark
auto eth1
iface eth1 inet static
	address 10.49.73.41
	netmask 255.255.255.248

#A10 Eisen-Server Ritcher, Server Revolte
auto eth2
iface eth2 inet static
	address 10.49.73.33
	netmask 255.255.255.248

#A15 Eisen-Linie
auto eth3
iface eth3 inet static
	address 10.49.50.1
	netmask 255.255.255.252

#A13 Eisen-Lugner
auto eth4
iface eth4 inet static
	address 10.49.69.1
	netmask 255.255.255.252
```

- Lugner

```
#A13 Eisen-Lugner
auto eth0
iface eth0 inet static
	address 10.49.69.2
	netmask 255.255.255.252
	gateway 10.49.69.1

#A21 Lugner-PC Grobe Forest
auto eth1
iface eth1 inet static
	address 10.49.68.1
	netmask 255.255.252.0

#A14 Lugner-PC Turk Region
auto eth2
iface eth2 inet static
	address 10.49.64.1
	netmask 255.255.255.0
```

- Linie

```
#A15 Eisen-Linie
auto eth0
iface eth0 inet static
	address 10.49.50.2
	netmask 255.255.255.252
	gateway 10.49.50.1

#A17 Linie-Lawine
auto eth1
iface eth1 inet static
	address 10.49.40.1
	netmask 255.255.255.252

#A19 Linie-PC Granz Channel
auto eth2
iface eth2 inet static
	address 10.49.48.1
	netmask 255.255.254.0
```

- Lawine

```
#A17 Linie-Lawine
auto eth0
iface eth0 inet static
	address 10.49.40.2
	netmask 255.255.255.252
	gateway 10.49.40.1

#A16 Lawine-PC Breadt Region, Router Heiter
auto eth1
iface eth1 inet static
	address 10.49.36.1
	netmask 255.255.255.192
```

- Heiter

```
#A16 Lawine-Heiter
auto eth0
iface eth0 inet static
	address 10.49.36.3
	netmask 255.255.255.192
	gateway 10.49.36.1

#A18 Heiter-Server Sein, PC Riegel Canyon
auto eth1
iface eth1 inet static
	address 10.49.32.1
	netmask 255.255.252.0
```

### Client
- PC LakeKorridor(24 Host)

```
#A3 Frieren-PC Lake Korridor
auto eth0
iface eth0 inet static
	address 10.49.73.2
	netmask 255.255.255.224
	gateway 10.49.73.1
```

- PC LaubHills(397 Host)

```
#A1 Fern-PC Laub Hills
auto eth0
iface eth0 inet static
	address 10.49.0.2
	netmask 255.255.248.0
	gateway 10.49.0.1
```

- PC Appetit Ragion(625 Host)

```
#A1 Fern-PC Appetit Region
auto eth0
iface eth0 inet static
	address 10.49.0.3
	netmask 255.255.248.0
	gateway 10.49.0.1
```

- PC RohrRoad (1000 Host)

```
#A4 Flamme-PC Rohr Road
auto eth0
iface eth0 inet static
	address 10.49.16.2
	netmask 255.255.252.0
	gateway 10.49.16.1
```

- PC SchwerMountains(5 Host)

```
#A9 PC Schwer Mountains
auto eth0
iface eth0 inet static
	address 10.49.20.2
	netmask 255.255.255.248
	gateway 10.49.20.1
```

- PC RoyalCapital(63 Host)

```
#A8 Denken-PC Royal Capital
auto eth0
iface eth0 inet static
	address 10.49.72.2
	netmask 255.255.255.0
	gateway 10.49.72.1
```

- PC WilleRegion(63 Host)

```
#A8 Denken-PC Wille region
auto eth0
iface eth0 inet static
	address 10.49.72.3
	netmask 255.255.255.0
	gateway 10.49.72.1
```

- PC GrobeForest(250 Host)

```
#A21 Lugner-PC Grobe Forest
auto eth0
iface eth0 inet static
	address 10.49.68.2
	netmask 255.255.255.0
	gateway 10.49.68.1
```

- PC TurkRegion(1000 Host)

```
#A14 Lugner-PC Turki Region
auto eth0
iface eth0 inet static
	address 10.49.64.2
	netmask 255.255.252.0
	gateway 10.49.64.1
```

- PC GranzChannel(254 Host)

```
#A19 Linie-PC Granz Channel
auto eth0
iface eth0 inet static
	address 10.49.48.2
	netmask 255.255.254.0
	gateway 10.49.48.1
```

- PC BredtRegion(29 Host)

```
#A16 Lawine-PC Breadt Region
auto eth0
iface eth0 inet static
	address 10.49.36.2
	netmask 255.255.255.192
	gateway 10.49.36.1
```

- PC RiegelCanyon(510 Host)

```
#A18 Heiter-PC Riegel Canyon
auto eth0
iface eth0 inet static
	address 10.49.32.2
	netmask 255.255.252.0
	gateway 10.49.32.1
```

### Server
- Server-Ritcher

```
#A10 Eisen-Server Ritcher
auto eth0
iface eth0 inet static
	address 10.49.73.34
	netmask 255.255.255.248
	gateway 10.49.73.33
```

- Server-Revolte

```
#A10 Eisen-Server Revolte
auto eth0
iface eth0 inet static
	address 10.49.73.35
	netmask 255.255.255.248
	gateway 10.49.73.33
```

- Server-Stark

```
#A12 Eisen-Stark
auto eth0
iface eth0 inet static
	address 10.49.73.42
	netmask 255.255.255.252
	gateway 10.49.73.41
```

- Server-Sein

```
#A18 Heiter-Server Sein
auto eth0
iface eth0 inet static
	address 10.49.32.3
	netmask 255.255.252.0
	gateway 10.49.32.1
```

### Route Configuration

Berikut adalah konfigurasi routing.

- Fern

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.49.8.1	#default A1,A2
```

- Himmel

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.49.20.17	#default A9,A20
```

- Flamme

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.49.20.33	#default A2,A13,A14,A15
route add -net 10.49.0.0 netmask 255.255.248.0 gw 10.49.8.2		#A1
route add -net 10.49.20.0 netmask 255.255.255.248 gw 10.49.20.18	#A9
```

- Frieren

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.49.73.45	#default A3,A5,A6
route add -net 10.49.0.0 netmask 255.255.248.0 gw 10.49.20.34		#A1
route add -net 10.49.8.0 netmask 255.255.255.252 gw 10.49.20.34		#A2
route add -net 10.49.16.0 netmask 255.255.252.0 gw 10.49.20.34		#A4
route add -net 10.49.20.0 netmask 255.255.255.248 gw 10.49.20.34	#A9
route add -net 10.49.20.16 netmask 255.255.255.252 gw 10.49.20.34	#A20
```

- Denken

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.49.73.53	#default A8,A7
```

- Heiter

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.49.36.1	#default A18,A16
```

- Lawine

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.49.40.1	#default A17,A16
route add -net 10.49.32.0 netmask 255.255.252.0 gw 10.49.36.3	#A18
```

- Linie

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.49.50.1	#default A15,A19,A17
route add -net 10.49.36.0 netmask 255.255.255.192 gw 10.49.40.2	#A16
route add -net 10.49.32.0 netmask 255.255.252.0 gw 10.49.40.2	#A18
```

- Lugner

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.49.69.1	#default A14,A21,A13
```

- Eisen

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.49.73.49	#default A11,A10,A12,A13,A15
route add -net 10.49.36.0 netmask 255.255.255.192 gw 10.49.50.2	#A16
route add -net 10.49.32.0 netmask 255.255.252.0 gw 10.49.50.2	#A18
route add -net 10.49.40.0 netmask 255.255.255.252 gw 10.49.50.2	#A17
route add -net 10.49.48.0 netmask 255.255.254.0 gw 10.49.50.2	#A19
route add -net 10.49.64.0 netmask 255.255.252.0 gw 10.49.69.2	#A14
route add -net 10.49.68.0 netmask 255.255.255.0 gw 10.49.69.2	#A21
```

- Aura

```
#eth1
route add -net 10.49.0.0 netmask 255.255.248.0 gw 10.49.73.46		#A1
route add -net 10.49.8.0 netmask 255.255.255.252 gw 10.49.73.46		#A2
route add -net 10.49.16.0 netmask 255.255.252.0 gw 10.49.73.46		#A4
route add -net 10.49.20.0 netmask 255.255.255.248 gw 10.49.73.46	#A9
route add -net 10.49.20.16 netmask 255.255.255.252 gw 10.49.73.46	#A20
route add -net 10.49.20.32 netmask 255.255.255.252 gw 10.49.73.46	#A5
route add -net 10.49.73.0 netmask 255.255.255.224 gw 10.49.73.46	#A3

#eth2
route add -net 10.49.72.0 netmask 255.255.255.0 gw 10.49.73.54	#A8

#eth3
route add -net 10.49.73.32 netmask 255.255.255.248 gw 10.49.73.50	#A10
route add -net 10.49.73.40 netmask 255.255.255.252 gw 10.49.73.50	#A12
route add -net 10.49.69.0 netmask 255.255.255.252 gw 10.49.73.50	#A13
route add -net 10.49.64.0 netmask 255.255.252.0 gw 10.49.73.50		#A14
route add -net 10.49.68.0 netmask 255.255.255.0 gw 10.49.73.50		#A21
route add -net 10.49.50.0 netmask 255.255.255.252 gw 10.49.73.50	#A15
route add -net 10.49.48.0 netmask 255.255.254.0 gw 10.49.73.50		#A19
route add -net 10.49.40.0 netmask 255.255.255.252 gw 10.49.73.50	#A17
route add -net 10.49.36.0 netmask 255.255.255.192 gw 10.49.73.50	#A16
route add -net 10.49.32.0 netmask 255.255.252.0 gw 10.49.73.50		#A18
```
