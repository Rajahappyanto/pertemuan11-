# pertemuan11

```s
Nama   : Raja Happyanto
Nim    : 312210235
Ruangan : TI.22.A2
BAHASA PEMOGRAMAN
```

# Practice 1
## Mengubah code lambda

code:

```s
import math
def a(x):
  return x**2
a = lambda x : x**2
print(a(8))
def b(x, y):
  return math.sqrt(x*2 + y*2)
b = lambda x, y : x * 2 + y * 2
print(b(2, 7))
def c(*args):
  return sum(args)/len(args)
c = lambda *args : sum(args)/len(args)
print(c(8,9,10,11,12))
def d(s):
  return "".join(set(s))
d = lambda s: "".join(set(s))
print(d("Rajaa"))
```

#### Output

![ss2]foto/ss2.png


### TUGAS PRAKTIKUM
Buat program sederhana dengan menggunakan fungsi yang akan menampilkan daftar nilai mahasiswa, Dengan ketentuan:

Fungsi - Tambah() untuk menambah data

Fungsi - Tampilkan() untuk menampilkn data

Fungsi - Hapus(nama) untuk menghapus data berdasarkan nama

Fungsi - Ubah(nama) untuk mengubah data berdasarkan nama

code di bawah menerapkan fungsi tambah tampilkan hapus ubah 

## Code Source
```s
x = mahasiswa = {}

def tambah():
    print("Tambah Data")
    nama = input("Nama  : ")
    nim = input("NIM    : ")
    tugas = int(input("Nilai Tugas      : "))
    uts = int(input("Nilai UTS        : "))
    uas = int(input("Nilai UAS        : "))
    akhir = tugas * 30/100 + uts * 35/100 + uas * 35/100
    mahasiswa[nama] = nim , tugas, uts , uas , akhir
def tampilkan():
    if mahasiswa.items():
        print("=================================================================================")
        print("\n                               DAFTAR NILAI MAHASISWA                    ")
        print("=================================================================================")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("=================================================================================")
        i = 0
        for b in mahasiswa.items():
             i += 1
             print("| {no:2d} | {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} | {5:7f}   |"
                . format ( b [ 0 ][: 14 ], b [ 1 ][ 0 ], b [ 1 ][ 1 ], b [ 1 ][ 2 ], b [ 1 ][ 3 ], b [ 1 ][ 4 ] , no = i ))
        print("---------------------------------------------------------------------------------")
    else :
        print("---------------------------------------------------------------------------------")
        print("\n                               DAFTAR NILAI MAHASISWA                    ")
        print("---------------------------------------------------------------------------------")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("---------------------------------------------------------------------------------")
        print("|                                TIDAK ADA DATA                                 |")
        print("---------------------------------------------------------------------------------")
def hapus():
    print ( "Hapus Data" )
    nama = input("Nama   : ")
    if  nama in  mahasiswa . keys ():
        del  mahasiswa [ nama ]
    else :
        print ( "Nama {0} Tidak Ditemukan" . format ( nama ))
def ubah():
    print ( "Ubah Data" )
    nama = input("Nama  : ")
    if nama in  mahasiswa . keys ():
        nim = input("NIM              : ")
        tugas = int(input("Nilai Tugas      : "))
        uts = int(input("Nilai UTS        : "))
        uas = int(input("Nilai UAS        : "))
        akhir = tugas * 30/100 + uts * 35/100 + uas * 35/100
        mahasiswa[nama] = nim , tugas, uts , uas , akhir
    else :
        print ( "Nama{0} Tidak Ditemukan" . format(nama ))

while True:
    print("")
    print("===========================")
    print("|   Program Input Nilai   |")
    print("===========================")
    c = input("L)ihat, T)ambah, U)bah, H)apus, K)eluar: ")
    if c.lower() == "l":
        tampilkan()
    elif c.lower() == "t":
        tambah()
    elif c.lower() == "u":
        ubah()
    elif c.lower() == "h":
        hapus()
    elif c.lower() == "k":
        print()
        print("---------------------------------------------------------------------------------")
        print("                                 PROGRAM TELAH SELESAI                    ")
        print("---------------------------------------------------------------------------------")
        print(35*'=')
        print("Nama\t: Rini Ariza\nKelas\t: TI.22.A3\nNIM\t\t: 312210337")
        print(35*'=')
        break

    else:
        print()
        print("Kode yang anda masukkan tidak benar!")
```

## Output

![ss1]foto/ss1.png
## Flowchart



