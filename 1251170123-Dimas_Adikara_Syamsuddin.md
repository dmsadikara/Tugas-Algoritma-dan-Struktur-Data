# BAGIAN A: RANCANGAN ALGORITMA DENGAN KARAKTERISTIK LENGKAP
## Studi Kasus: Algoritma Pemesanan Makanan Secara Online via Aplikasi.
### Langkah-langkah Pemesanan Makananan Secara Online via Aplikasi apapun:
- Input: Pilihan restoran yang dipiih, pilihan menu beserta jumlahnya, lokasi pengiriman, dan pilihan metode pembayaran.
- Langkah 1, Pengguna memilih satu restoran berdasarkan lokasi rumah dan rating restoran tersebut.
- Langkah 2, Pengguna memilih satu atau beberapa item menu beserta jumlahnya (qty) di satu restoran yang telah dipilih.
- Langkah 3, Setelah memilih banyak nya item yang dipilih, sistem akan mengalikan harga setiap item, lalu menjumlahkan seluruh item untuk medapatkan subtotal harga keseluruhan menu yang dipilih.
- Langkah 4, Sistem menghitung ongkir berdasarkan jarak antara restoran dengan lokasi pengguna (misalnya tarif per km).
- Langkah 5, Setelah subtotal menu dan ongkos kirim sudah diketahui, sistem akan menjumlahkan subtotal menu dengan ongkos kirim untuk mendapatkan total pembayaran yang harus di bayar pengguna.
- Langkah 6, Sistem akan menampilkan metode pembayaran apa yang ingin digunakan oleh pengguna, misalnya tunai (COD) dan nontunai. Bila pengguna ingin menggunakan metode pembayaran nontunai sistem akan memvalidasi ketersediaan atau kecukupan saldo pengguna. 
- Langkah 7, Sistem memproses pembayaran sesuai dengan metode yang dipilih. Jika berhasil, status pesanan diubah menjadi terkonfirmasi dan jika gagal, proses dihentikan dan pengguna diminta untuk mengulang pembayaran.
- Langkah 8, Setelah seluruh pembayaran sudah terkonfirmasi, sistem akan mengirim rincian pesanan pengguna ke dapur restoran yang telah dipilih sebelumnya untuk diproses.
- Output: Pesanan yang terkonfirmasi dan terkirim ke dapur restoran, rincian subtotal menu dan ongkos kirim, dan status pembayaran.
- Definiteness: Rumus perhitungan subtotal (harga x qty) dan total bayar (subtotal menu + ongkir) sudah pasti nilainya begitu input diketahui.
- Finiteness: Proses berakhir begitu pesanan berhasil dikirim ke dapur resto (atau berhenti lebih awal jika pembayaran gagal dan pengguna tidak mengulang), bukan berputar terus-menerus.
- Effectiveness: Setiap langkah dapat benar-benar dikerjakan/dihitung secara nyata dengan sumber daya yang ada (harga menu diketahui, jarak dapat dihitung, sistem pembayaran dapat memverifikasi saldo), sehingga algoritma memang dapat dijalankan sampai selesai dan menghasilkan output yang benar, bukan sekadar konsep abstrak.

 
# BAGIAN B: ANALISIS PEMILIHAN STRUKTUR DATA
## Studi Kasus: Pilihlah struktur data yang paling tepat (Array, Linked List, Stack, Queue, Binary Search Tree, Hash Table, atau Graph) untuk menyelesaikan 3 skenario di bawah ini. Berikan alasan logis mengapa struktur data tersebut dipilih!
### Skenario 1 (Fitur Fitur Undo / Redo):
Sebuah aplikasi pengolah kata (Text Editor) membutuhkan fitur untuk membatalkan ketikan terakhir pengguna (Undo) dan mengembalikannya lagi (Redo).
- Struktur Data: Stack 
- Alasan: Karena setelah saya baca di jurnal struktur data stack sendiri memiliki sifat atau prinsip LIFO yaitu Last In, First Out elemen terakhir yang dimasukkan adalah elemen pertama yang dikeluarkan. Artinya, operasi penyisipan dan penghapusan hanya terjadi di satu ujung saja dan yang pas banget buat skenario penugasan adalah struktur Stack yang pas dengan fitur undo atau redo, jadi saya tidak perlu mikir ribet soal urusan data, tinggal push aksi baru ke atas dan pop kalau mau di undo.

### Skenario 2 (Peta Navigasi Rute Perjalanan):
Sebuah aplikasi GPS membutuhkan cara untuk memodelkan lokasi-lokasi kota beserta jalan penghubungnya guna mencari rute tercepat.
- Struktur Data: Graph
- Alasan: Karena setelah saya baca di jurnal, Graph adalah struktur data non linear sendiri yang terdiri dari simpul (node) dan sisi (koneksi) yang merepresentasikan hubungan antar objek dan sruktur data Graph cocok dengan skenario penugasan ini, dengan struktur data Graph yang emang secara natural bentuknya udah kayak Graph yang dimana kota menjadi node, jalan menjadi edge yang di kasih bobot seperti jarak atau waktu tempuh, dengan struktur data Graph bisa langsung pake algoritma pencarian rute yang sudah teruji efisien.

### Skenario 3 (Sistem Login Pengguna Berbasis Username):
Sistem butuh mencari data akun dari jutaan user secara instan berdasarkan Username saat proses login.
- Struktur Data: Hast Table 
- Alasan: Karena setelah saya baca di jurnal Hash Table sendiri didefinisikan sebagai struktur data yang digunakan untuk memasukakan, mencari, dan menghapus pasangan kunci nilai dengan cepat dan makannya struktur data Hash Table ini cocok dengan skenario penugasan ini.
  
# BAGIAN C: EKSPLORASI ANALOGI MANDIRI
## Studi Kasus: Pilihlah satu struktur data di bawah ini, kemudian buatlah analogi kehidupan sehari-hari baru yang kreatif dan belum dijelaskan di dalam slide perkuliahan:
- Pilih salah satu: Array, Linked List, Stack, Queue, Tree, Graph, atau Hash Table.
- Jelaskan:
1. Nama analogi kehidupan sehari-hari yang Anda buat.
2. Bagaimana cara kerja analogi tersebut.
3. Mengapa analogi tersebut mencerminkan kelebihan atau kekurangan dari struktur data yang dipilih.

Pilihan Struktur Data saya: *Graph* 
Penjelasan:
1. Nama Analogi: Seperti peta rute angkutan umum atau kota-kota yang terhubung dengan jalan raya.
2. Cara kerja: Kota-kota bertindak sebagai titik, dan jalan raya atau rute perjalanan bertindak sebagai penghubung. Analogi ini digunakan untuk aplikasi seperti Google Maps untuk mencari rute tercepat untuk sampai di tempat.
3. Kelebihan dan kekurangan:
- Kelebihan: Dalam jaringan kota, suatu kota bisa terhubung langsung ke banyak kota lain sekaligus lewat jalur yang berbeda-beda dan rute peta jalan raya tidak hanya memberi tahu bahwa lokasi Kota A terhubung ke Kota B, tetapi juga memberi tahu jaraknya dan tingkat kemacetannya dalam sebuah warna.
- Kekurangan: Jika seseorang tersesat di kota besar dengan ribuan gang dan jalan layang, mencari jalan keluar secara manual sangat membingungkan karena pilihannya terlalu banyak dan rumit. 

# Link Jurnal yang saya baca

