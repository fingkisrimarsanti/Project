# Optimasi Penentuan Menu Diet Ketogenik Menggunakan Algoritma Greedy

## Deskripsi Proyek
Program ini bertujuan untuk membantu menentukan menu makanan bagi pelaku diet ketogenik berdasarkan kebutuhan kalori harian dan preferensi makronutrien (lemak, protein, karbohidrat). Algoritma greedy digunakan untuk memilih makanan yang memberikan memberikan nutrisi sesuai maksimum sesuai dengan aturan diet ketogenik dimana kombinasi makanan disarankan mengandung lemak tinggi, protein sedang dan karbohidrat yang rendah. Pada program ini memilih menggunakan algoritma greedy karena algoritma ini bersifat cepat dan sederhana dan cukup efektif jika digunakan untuk konteks menentuan kombinasi makanan diet yang fleksibel. 

## Fitur Utama
- Menentukan makanan dengan kandungan lemak tinggi, protein sedang, dan karbohidrat rendah.
- Mempertimbangkan harga bahan makanan dengan menntapkan anggaran.
- Penentuan menu bakanan dipilih secara greedy dari 3 objektif, yaitu raiso lemak terhadap protein dan karbohidrat, rasio lemak dan karbohidratterhadap protein, dan rasio lemak, protein dan karbohidrat berdasarkan harga.
- Menampilkan hasil berupa daftar makanan yang optimal dilengkapi informasi total kalori, lemak, protein, karbohidrat, dan harga.

## Alur Algoritma Greedy
### 1. Input Data
Menginputkan data berupa file csv dengan informasi nama makanan, kandungan nutrisi, dan harga.  
### 2. Menghapus Data Yang Tidak Diperlukan 
Data diubah dalam bentuk data frame dan memilih kolom informasi yang akan digunakan. Kolom data yangdihapus adalah kolom keterangan yang menyatakan berat setiap bahan makanan.  
### 3. Inisialisasi batas nutrisi harian
Melakukan inisialisasi batas kalori, lemak, protein, dan karbohidrat per hari yang telah ditargetkan.
### 4. Perhitungan Rasio
Perhitungan rasio setiap nutrisi untuk mengoptimalkan kandungan bahan makanan agar sesuai dengan aturan diet ketogenik.
### 5. Pengurutan (sorting)
Pengurutan data dilakukan oleh algoritma greedy berdasarkan rasio yangtelah dihitung sebelumnya. Misalnya makanan dengan kandungan lemak yang tinggi, protein sedang dan rendah karbohidrat akan diprioritaskan dengan tetap mempertimbangkan batas anggaran. 
### 6. Pemilihan Makanan
Algoritma greedy akan memilih makanan sesuai dnegan batas aturan yang telahdi tetapkan. Pengguna harus menginputkan batas anggaran untuk memilih makanan yang sesuai.
### 7. Output
Program menampilkan daftar bahan makanan yang terpilih dilengkapi dengan total kalori, lemak, protein, karbohidrat, dan harga. 

## Cara Penggunaan
### 1. Menjalankan Program
Program dapat dijalankan dengan perintah berikut:
```bash
python main.py
```
### 2. Input 
- Dataset : berupa daftar makanan dalam file CSV, setiap bahan makanan dilengkapi dengan informasi kalori, karbohidrat, protein, lemak, harga, dan keterangan.
```bash
nama_file = ("Dataset PKA.csv")
```
- Batas anggaran : pengguna menginputkan batas anggaran yangakan digunakan sebagai pertimbangan agar pemilihan mahan makanan tidak melebihi anggaran.
```bash
anggaran = input('Masukan batas harga : ')
```
Input anggaran tidak menyertakan titik dan Rp, misalnya : 100000
### 3. Output
Program akan menampilkan daftar bahan makanan terpilih dilengkapi dengan informasi total kalori, lemak, protein, karbohidrat, dan harga berdasarkan input yang telah diberikan. Berikut contoh hasil output :
```text
Masukan batas harga : 100000
Bahan Makanan : Ikan mujair, Dada ayam, Minyak kelapa, Daging sapi, Hati ayam , Ikan kembung, Pepaya, Alpukat, Lemon, Apel, Belimbing.
Total kalori : 1946
Total lemak : 163.9
Total protein : 97.9
Total karbohidrat : 49.8
Total harga : 54150
```
