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

    ![3](https://user-images.githubusercontent.com/115912116/210395598-fe7df17d-c901-4bb5-b1c5-5a58adf053d6.PNG)

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

    ![5](https://user-images.githubusercontent.com/115912116/210395709-47af7057-ee4a-4cb9-9f4f-c28e4a88b56a.PNG)

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
- Output Ubah Data

    ![7](https://user-images.githubusercontent.com/115912116/210395793-9128fb03-1d4a-4a48-b7b9-41f7c6c7eb1f.PNG)

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

    ![8](https://user-images.githubusercontent.com/115912116/210395839-9e787011-89bc-4722-9e3d-e6f605fa775c.PNG)

- Output Keluar

    ![9](https://user-images.githubusercontent.com/115912116/210395878-c5adab2f-cf35-4eeb-91d8-d91aa9409fde.PNG)




    ========   SELESAI TRIMKASIH ==========
