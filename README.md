## Nama    :Mochamad Nabil Kurnia
## Kelas   :TI.24.A4
## NIM     : 312410307
## Matkul  : Bahasa Pemrograman


# Latihan 1

![Screenshot 2024-12-01 143954](https://github.com/user-attachments/assets/4f4ffcd7-913b-44fb-b3df-f88544a0b179)

```python
daftar_nilai_mahasiswa = {}

def tambah_data():
    print("\nTambahkan Data :")
    nama = input("Masukan Nama:")
    nim = input("Masukan NIM:")
    try:
        tugas = float(input("Nilai Tugas: "))
        uts = float(input("Nilai UTS: "))
        uas = float(input("Nilai UAS: "))
    except ValueError:
        print("Harap masukkan angka yang valid.")
        return
    daftar_nilai_mahasiswa[nama] = (nim, tugas, uts, uas)
    print(f"Data {nama} berhasil ditambahkan.")
    
def tampil_data():
    print("\nDaftar Mahasiswa:")
    if daftar_nilai_mahasiswa:
        print("Nama  |     NIM     |    Tugas   |     UTS     |      UAS     |")
        print("=" *55)
        for nama, (nim, tugas, uts, uas) in daftar_nilai_mahasiswa.items():
            print(f"{nama}    | {nim}   | {tugas}   | {uts} | {uas} ")
        print("=" *55)
    else:
        print("Tidak ada data dalam daftar.")

def hapus_data():
    nama = input("Masukan nama: ")
    if nama in daftar_nilai_mahasiswa:
        del daftar_nilai_mahasiswa[nama]
        print(f"Data {nama} telah di hapus")
    else:
        print(f"Data {nama} tidak ditemukan")

def ubah_data():
    nama = input("Masukan nama: ")
    if nama in daftar_nilai_mahasiswa:
        tugas_baru = input(f"Masukan nilai tugas baru untuk {nama}: ")
        uts_baru = input(f"Masukan nilai uts baru untuk {nama}: ")
        uas_baru = input(f"Masukan nilai uas baru untuk {nama}: ")
        
        daftar_nilai_mahasiswa[nama] = tugas_baru, uts_baru, uas_baru
        print(f"Data {nama} berhasil di ubah :) ")
    else:
        print(f"Data {nama} tidak ditemukan")
        
# menu

while True:
    print("\nMenu:")
    print("1. Tambah data")
    print("2. Tampilkan data")
    print("3. Hapus data")
    print("4. Ubah data")
    print("5. Keluar")
    
    pilihan = input("Masukkan angka (1-5):")
    
    if pilihan == "1":
        tambah_data()
    elif pilihan == "2":
        tampil_data()
    elif pilihan == "3":
        hapus_data()
    elif pilihan == "4":
        ubah_data()
    elif pilihan == "5":
        break
    else:
        print("Pilihan tidak ditemukan.")
````

Penjelasan code

---

# 1. Variabel `daftar_nilai_mahasiswa`
```python
daftar_nilai_mahasiswa = {}
```
- Fungsi: Variabel ini berupa dictionary kosong yang digunakan untuk menyimpan data mahasiswa.  
  - Key: Nama mahasiswa.  
  - Value: Tuple yang berisi NIM, nilai tugas, nilai UTS, dan nilai UAS.

---

# 2. Fungsi `tambah_data()`
```python
def tambah_data():
    ...
```
- Fungsi: Menambahkan data mahasiswa ke dalam `daftar_nilai_mahasiswa`.  
- Penjelasan langkah-langkah:
  1. Meminta input nama, NIM, nilai tugas, UTS, dan UAS dari pengguna.
  2. Memeriksa apakah nilai yang dimasukkan valid (menggunakan `try` dan `except` untuk menangani input yang bukan angka).  
  3. Menyimpan data mahasiswa dalam bentuk tuple ke dalam dictionary dengan nama sebagai key.
  4. Menampilkan pesan bahwa data berhasil ditambahkan.

---

# 3. Fungsi `tampil_data()`
```python
def tampil_data():
    ...
```
- Fungsi: Menampilkan daftar seluruh data mahasiswa yang tersimpan di `daftar_nilai_mahasiswa`.  
- Penjelasan langkah-langkah:
  1. Mengecek apakah dictionary berisi data atau kosong.
  2. Jika data ada:
     - Menampilkan header tabel.
     - Melakukan iterasi pada dictionary menggunakan `for`, dan menampilkan data dalam format tabel.
  3. Jika kosong, menampilkan pesan bahwa tidak ada data yang tersedia.

---

# 4. Fungsi `hapus_data()`
```python
def hapus_data():
    ...
```
- Fungsi: Menghapus data mahasiswa berdasarkan nama yang dimasukkan.  
- Penjelasan langkah-langkah:
  1. Meminta nama mahasiswa yang ingin dihapus.
  2. Mengecek apakah nama ada dalam dictionary:
     - Jika ada, menghapus data dengan `del`.
     - Jika tidak ada, menampilkan pesan bahwa data tidak ditemukan.

---

# 5. Fungsi `ubah_data()`
```python
def ubah_data():
    ...
```
- Fungsi: Mengubah data mahasiswa yang sudah ada.  
- Penjelasan langkah-langkah:
  1. Meminta input nama mahasiswa.
  2. Mengecek apakah nama mahasiswa ada di dictionary.
  3. Jika nama ditemukan:
     - Meminta input nilai tugas, UTS, dan UAS baru.
     - Memperbarui nilai mahasiswa di dictionary.
  4. Jika nama tidak ditemukan, menampilkan pesan bahwa data tidak ditemukan.

---

# 6. Menu Utama (`while True`)
```python
while True:
    ...
```
- Fungsi: Membuat menu interaktif untuk pengguna.  
- Penjelasan langkah-langkah:
  1. Menampilkan pilihan menu:
     - 1: Tambah data.
     - 2: Tampilkan data.
     - 3: Hapus data.
     - 4: Ubah data.
  2. Meminta input dari pengguna untuk memilih opsi menu.
  3. Berdasarkan pilihan:
     - Memanggil fungsi yang sesuai.
     - Jika pengguna memasukkan angka di luar 1-4, menampilkan pesan kesalahan.

---

![image](https://github.com/user-attachments/assets/0ab3b0b8-d293-4272-afbe-736e9ae18234)

![Screenshot 2024-12-01 150516](https://github.com/user-attachments/assets/54979da1-0d5c-4930-b86e-7bfd7a023bec)

Hasil kode program

ini adalah untuk menambahkan data

![Screenshot 2024-12-01 120126](https://github.com/user-attachments/assets/9330f178-5491-4a20-93a7-9eae7d36ea50)

Tampilkan data mahasiswa

![Screenshot 2024-12-01 120218](https://github.com/user-attachments/assets/e2f813bc-c320-4038-9ca1-4aba66d71427)

Hapus data

![Screenshot 2024-12-01 120256](https://github.com/user-attachments/assets/8af0f76b-73c6-424f-a262-f709753b8740)

Ubah data mahasiswa

![Screenshot 2024-12-01 120625](https://github.com/user-attachments/assets/f1e9fb70-581d-4adf-a500-d4fd225af6a6)

# Flowchart

![flw](https://github.com/user-attachments/assets/940540d0-6c0a-4ae3-807d-843ddd6d7806)
