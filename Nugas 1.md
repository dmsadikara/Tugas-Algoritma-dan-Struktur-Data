# BAGIAN A: RANCANGAN ALGORITMA DENGAN KARAKTERISTIK LENGKAP
## Studi Kasus: Algoritma Pemesanan Makanan Secara Online via Aplikasi.
### Langkah-langkah Pemesanan Makananan Secara Online via Aplikasi apapun:
1. Pengguna memilih satu restoran berdasarkan lokasi rumah dan rating restoran tersebut.
2. Pengguna memilih satu atau beberapa item menu beserta jumlahnya (qty) di satu restoran yang telah dipilih.
3. Setelah memilih banyak nya item yang dipilih, sistem akan mengalikan harga setiap item, lalu menjumlahkan seluruh item untuk medapatkan subtotal harga keseluruhan menu yang dipilih.
4. Sistem menghitung ongkir berdasarkan jarak antara restoran dengan lokasi pengguna (misalnya tarif per km).
5. Setelah subtotal menu dan ongkos kirim sudah diketahui, sistem akan menjumlahkan subtotal menu dengan ongkos kirim untuk mendapatkan total pembayaran yang harus di bayar pengguna.
6. Sistem akan menampilkan metode pembayaran apa yang ingin digunakan oleh pengguna, misalnya tunai (COD) dan nontunai. Bila pengguna ingin menggunakan metode pembayaran nontunai sistem akan memvalidasi ketersediaan atau kecukupan saldo pengguna. 
7. Sistem memproses pembayaran sesuai dengan metode yang dipilih. Jika berhasil, status pesanan diubah menjadi terkonfirmasi dan jika gagal, proses dihentikan dan pengguna diminta untuk mengulang pembayaran.
8. Setelah seluruh pembayaran sudah terkonfirmasi, sistem akan mengirim rincian pesanan pengguna ke dapur restoran yang telah dipilih sebelumnya untuk diproses.

### Pemenuhan 5 Karakteristik Utama Tugas:
- Input: Pilihan restoran yang dipiih, pilihan menu beserta jumlahnya, lokasi pengiriman, dan pilihan metode pembayaran.
- Output: Pesanan yang terkonfirmasi dan terkirim ke dapur restoran, rincian subtotal menu dan ongkos kirim, dan status pembayaran.
- Definiteness: Rumus perhitungan subtotal (harga x qty) dan total bayar (subtotal menu + ongkir) sudah pasti nilainya begitu input diketahui.
- Finiteness: Proses berakhir begitu pesanan berhasil dikirim ke dapur resto (atau berhenti lebih awal jika pembayaran gagal dan pengguna tidak mengulang), bukan berputar terus-menerus.
- Effectiveness: Setiap langkah dapat benar-benar dikerjakan/dihitung secara nyata dengan sumber daya yang ada (harga menu diketahui, jarak dapat dihitung, sistem pembayaran dapat memverifikasi saldo), sehingga algoritma memang dapat dijalankan sampai selesai dan menghasilkan output yang benar, bukan sekadar konsep abstrak.

 
# BAGIAN B: ANALISIS PEMILIHAN STRUKTUR DATA
## Studi Kasus: Pilihlah struktur data yang paling tepat (Array, Linked List, Stack, Queue, Binary Search Tree, Hash Table, atau Graph) untuk menyelesaikan 3 skenario di bawah ini. Berikan alasan logis mengapa struktur data tersebut dipilih!

# BAGIAN C: EKSPLORASI ANALOGI MANDIRI
