# Lab7py

Inisialisasi Kelas

python
Copy code
def __init__(self):
    self.data = []
Method __init__ merupakan konstruktor kelas yang dipanggil saat objek kelas dibuat.
self.data adalah variabel untuk menyimpan data mahasiswa dalam bentuk list.
Method tambah

python
Copy code
def tambah(self, nama, nilai):
    self.data.append({'nama': nama, 'nilai': nilai})
    print(f"Data mahasiswa {nama} dengan nilai {nilai} berhasil ditambahkan.")
Method tambah digunakan untuk menambahkan data mahasiswa baru ke dalam self.data.
Parameter nama dan nilai mewakili nama mahasiswa dan nilai yang ingin ditambahkan.
Data baru ditambahkan dalam bentuk dictionary yang berisi nama dan nilai, lalu dimasukkan ke dalam list self.data.
Pesan konfirmasi akan ditampilkan setelah data berhasil ditambahkan.
Method tampilkan

python
Copy code
def tampilkan(self):
    if not self.data:
        print("Belum ada data nilai mahasiswa.")
    else:
        print("Daftar nilai mahasiswa:")
        for idx, nilai in enumerate(self.data, start=1):
            print(f"{idx}. Nama: {nilai['nama']}, Nilai: {nilai['nilai']}")
Method tampilkan digunakan untuk menampilkan semua data mahasiswa yang tersimpan.
Jika tidak ada data (self.data kosong), akan ditampilkan pesan bahwa belum ada data yang tersimpan.
Jika ada data, maka akan ditampilkan daftar nama dan nilai setiap mahasiswa dengan bantuan enumerate untuk menampilkan nomor urut.
Method hapus

python
Copy code
def hapus(self, nama):
    data_terhapus = False
    for nilai in self.data:
        if nilai['nama'] == nama:
            self.data.remove(nilai)
            data_terhapus = True
            print(f"Data mahasiswa {nama} berhasil dihapus.")
            break
    
   if not data_terhapus:
        print(f"Tidak ada data mahasiswa dengan nama {nama}.")
Method hapus memungkinkan untuk menghapus data mahasiswa berdasarkan nama.
Mencari data yang cocok dengan nama yang diberikan.
Jika ditemukan, data mahasiswa tersebut dihapus dari self.data.
Jika tidak ditemukan, akan ditampilkan pesan bahwa tidak ada data dengan nama yang diberikan.
Method ubah

python
Copy code
def ubah(self, nama, nilai_baru):
    data_diubah = False
    for nilai in self.data:
        if nilai['nama'] == nama:
            nilai['nilai'] = nilai_baru
            data_diubah = True
            print(f"Data mahasiswa {nama} berhasil diubah menjadi nilai {nilai_baru}.")
            break
    
  if not data_diubah:
        print(f"Tidak ada data mahasiswa dengan nama {nama}.")
Method ubah memungkinkan untuk mengubah nilai mahasiswa berdasarkan nama.
Mencari data yang cocok dengan nama yang diberikan.
Jika ditemukan, nilai mahasiswa tersebut diubah menjadi nilai baru yang diberikan.
Jika tidak ditemukan, akan ditampilkan pesan bahwa tidak ada data dengan nama yang diberikan.
