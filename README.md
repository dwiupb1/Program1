Program 1

# UAS Bahasa Pemograman

Nama    : Dwi Heriyanto

Nim     : 312210541

Kelas   : TI.22.B2

# SOAL: 
* Buatlah package dan modul dengan struktur sebagai berikut

![1](https://user-images.githubusercontent.com/115912116/210259606-4230f676-a495-4861-8ebf-e2c1bf573e27.PNG)


* Kemudian buatlah file README.md yang berisi penjelasan dan screenshot hasil eksekusi program. Lalu upload ke repository github masing-masing.

>Penjelasan

- Tambah data
#
    if t.lower() == 't':
        print("Tambah Data")
        nama = input("Nama\t\t: ")
        nim = int(input("NIM\t\t\t: "))
        uts = int(input("Nilai UTS\t: "))
        uas = int(input("Nilai UAS\t: "))
        tugas = int(input("Nilai Tugas\t: "))
        akhir = tugas * 30/100 + uts * 35/100 + uas * 35/100
        a [nama] = nim, uts, uas, tugas, akhir

- Output Tambah data

    <img src="3.PNG">

- lihat Data
#
       elif t.lower() == 'l':
        if a.items():
            print("="*78)
            print("| Daftar Nilai Mahasiswa |")
            print("="*78)
            i = 0
            for z in a.items():
                i += 1
                print("| {no:2d} | {0:15s} | {1:15d} | {2:5d} | {3:5d} | {4:7d} | {5:7.2f} |"
                      .format(z[0][:13], z[1][0], z[1][1], z[1][2], z[1][3], z[1][4], no=i))
                print("="*78)
        else:
            print("="*78)
            print("|                        Daftar Nilai Mahasiswa                           |")
            print("="*78)
            print("|                         TIDAK ADA DATA !!!                              |")
            print("="*78)

- Output Lihat Data

    <img src="5.PNG">

- Mengubah Data 
#
    elif t.lower() == 'u':
        print("Ubah Data")
        nama = input("\tMasukkan Nama\t\t: ")
        if nama in a.keys():
            nim = int(input("\tNIM\t\t\t: "))
            uts = int(input("\tNilai UTS\t\t\t: "))
            uas = int(input("\tNilai UAS\t\t\t: "))
            tugas = int(input("\tNilai Tugas\t\t\t: "))
            akhir = tugas * 30/100 + uts * 35/100 + uas * 35/100
            a[nama] = nim, uts, uas, tugas, akhir
        else:
            print("Nama {0} tidak ditemukan".format(nama))
- Output 

    <img src="7.PNG">

-   Hapus Data

#
    elif t.lower() == 'h':
        print("Hapus Data")
        nama = input("Masukkan Nama : ")
        if nama in a.keys():
            del a[nama]
        else:
             print("Nama {0} Tidak Ditemukan".format(nama))

- 0utput Hapus Data

    <img src="8.PNG">

- Output Keluar

    <img src="9.PNG">




    ========   SELESAI TRIMKASIH ==========