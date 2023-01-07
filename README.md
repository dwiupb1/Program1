Program 1

# UAS Bahasa Pemograman

Nama    : Dwi Heriyanto

Nim     : 312210541

Kelas   : TI.22.B2

# SOAL: 
* Buatlah package dan modul dengan struktur sebagai berikut

![1](https://user-images.githubusercontent.com/115912116/210259606-4230f676-a495-4861-8ebf-e2c1bf573e27.PNG)


>Penjelasan :

>daftar_nilai.py berisi modul untuk: tambah_data, ubah_data, hapus_data, dan cari_data

#    
     from view.input_nilai import *

    data = {}

    def tambah_data():
        print("====Tambah Data====")
        global data
        nama = input_nama()
        nim = input_nim()
        nilaiTugas = input_nilaiTugas()
        nilaiUts = input_nilaiUas()
        nilaiUas = input_nilaiUas()
        nilaiAkhir = (0.30 * nilaiTugas) + (0.35 * nilaiUts) + (0.35 * nilaiUas)
        data[nama] = nim, nilaiTugas, nilaiUts, nilaiUas, nilaiAkhir
        print("\nData Berhasil Ditambahkan!")
        return data

    def ubah_data():
        print("====Ubah Data====")
        nama = input("Masukkan Nama: ")
        if nama in data.keys():
            nim           = input_nim()
            nilaiTugas    = input_nilaiTugas()
            nilaiUts      = input_nilaiUts()
            nilaiUas      = input_nilaiUas()
            nilaiAkhir    = (0.30 * nilaiTugas) + (0.35 * nilaiUts) + (0.35 * nilaiUas)
            data[nama]  = nim, nilaiTugas, nilaiUts, nilaiUas, nilaiAkhir
            print("\nData Berhasil Di Update!")
        else:
            print("Data tidak ditemukan!")

    def hapus_data():
        print("====Hapus Data====")
        nama = input("Masukkan Nama:  ")
        if nama in data.keys():
            del data[nama]
            print("Data",nama,"Telah dihapus!")
        else:
            print("Data Mahasiswa Tidak Ada".format(nama))
    


* Output data

   ![daftar_nilai py](https://user-images.githubusercontent.com/115912116/210795222-944877f7-e9dd-4e01-b2f0-7f2656b7e091.PNG)

>view_nilai.py berisi modul untuk: cetak_daftar_nilai, cetak_hasil_pencarian 

#
        from model.daftar_nilai import *

    def cetak_daftar_nilai():
        print("====Lihat Data====")
        if data.items():
            print("\n Daftar Nilai Mahasiswa ")
            print("==================================================================")
            print("| No |     Nama     |    NIM    | Tugas |  UTS  |  UAS  |  Akhir |")
            print("==================================================================")
            i = 0
            for x in data.items():
                i += 1
                print("| {6:2} | {0:12s} | {1:9s} | {2:5} | {3:5} | {4:5} | {5:6} |".format(x[0], x[1][0], x[1][1], x[1][2],
                                                                                            x[1][3], x[1][4], i))
            print("==================================================================")
        else:
            print("\n Daftar Nilai Mahasiswa ")


* 0utput Data :

    ![view_nilai py](https://user-images.githubusercontent.com/115912116/210795165-cb3834b1-effc-4270-9ddc-1bbd96ae3e42.PNG)

 >input_nilai.py berisi modul untuk: input_data yang meminta pengguna memasukkan data. 

    def input_nama():
        global nama
        nama = input("Masukkan Nama anda        : ")
        return nama

    def input_nim():
        global nim
        nim = input("Masukkan NIM         : ")
        return nim

    def input_nilaiTugas():
        global nilaiTugas
        nilaiTugas = int(input("Masukkan Nilai Tugas : "))
        return nilaiTugas

    def input_nilaiUts():
        global nilaiUts
        nilaiUts = int(input("Masukkan Nilai UTS   : "))
        return nilaiUts

    def input_nilaiUas():
        global nilaiUas
        nilaiUas = int(input("Masukkan Nilai UAS   : "))
        return nilaiUas

* Output data :

   ![input_nilai py](https://user-images.githubusercontent.com/115912116/210795144-89169eff-3a8f-4b6f-a0fc-3a5b7452bbce.PNG)

 >main.py berisi program utama (menu pilihan yang memanggil semua menu yang ada)

        from view.view_nilai import *
    print("===================================================================")
    print("                         PROGRAM UAS SEMESTER 1                                 ")
    print("===================================================================")

    while True:
    c = input("\n(T)ambah, (U)bah, (H)apus, (C)ari, (L)ihat, (K)eluar: ")

    if (c.lower() == 't'):
        tambah_data()

    elif (c.lower() == 'u'):
        ubah_data()

    elif (c.lower() == 'h'):
        hapus_data()

    elif (c.lower() == 'c'):
        cetak_hasil_pencarian()

    elif (c.lower() == 'l'):
        cetak_daftar_nilai()

    elif (c.lower() == 'k'):
        break

    else:
        print("=== Pilih Sesuai Menu Yang Tersedia ===")

* Output data :

   ![main py](https://user-images.githubusercontent.com/115912116/210795160-e1ba8940-6351-4dcb-819b-9961b600357b.PNG)

# Link Youtube
 * Jangan Lupa Like & Subcribe


    ========   SELESAI TRIMKASIH ==========
