---
tags:
  - Fleeting
  - "#Business"
status: inbox
created: 2026-09-04
---
Setuju—kebutuhanmu bukan ERP besar. Yang cocok adalah **“ERP ringan untuk kontrol order, purchasing, dan uang”**. Jangan dulu masuk jurnal debit/kredit, inventory kompleks, atau approval bertingkat.

Dari sistem yang sekarang, alur SO → Surat Jalan → Invoice sudah cukup bagus. Kita tinggal memperkuat beberapa titik penting.

## 1. Tracking SO dan revisinya

Dashboard SO sebaiknya menjadi pusat aktivitas admin. Setiap SO memperlihatkan:

- Belum dikirim
- Terkirim sebagian
- Terkirim penuh
- Belum ditagih
- Ditagih sebagian
- Ditagih penuh
- Belum dibayar
- Lunas

Detail per barang:

|Barang|Qty SO|Sudah dikirim|Sisa kirim|Sudah ditagih|
|---|---|---|---|---|
|Barang A|100|60|40|60|
*ini sudah ok tapi ada errornya soalnya nominal SO dihitung include ppn dan nominal invoice dihitungnya belum ppn jadi mismatch dan masuk ke partly billed. diperbaiki aja semua SO dan invoice dihitung total nominal dari semua barang itu sebelum ppn*
Sistem yang sekarang sebenarnya sudah menghitung banyak bagian ini. Yang perlu ditambahkan adalah **revisi SO**. 

### Cara menangani revisi SO

Jangan otomatis mengubah Surat Jalan dan Invoice yang sudah terbit karena dokumen tersebut mungkin sudah dikirim ke customer.

Lebih aman:

1. Admin membuka SO dan memilih **“Buat Revisi”**.
2. Sistem menyimpan versi lama, misalnya SO-001 Rev.0.
3. Admin mengubahnya menjadi Rev.1.
4. Sistem membandingkan perubahan:
    - Barang bertambah/dihapus
    - Harga berubah
    - Kuantitas berubah
    - Data customer berubah
5. Sistem menampilkan dokumen terdampak:
    - SJ-001 perlu diperiksa
    - Invoice-001 perlu diperiksa
6. Admin memilih tindakan:
    - Tidak perlu revisi
    - Buat revisi Surat Jalan
    - Buat revisi Invoice
    - Batalkan dan terbitkan dokumen pengganti

Tambahkan label sederhana seperti **“Ada revisi belum diselesaikan”** pada dashboard. Ini sudah cukup tanpa workflow approval yang kompleks. *Ini sudah oke, nanti coba bikin workflow dan UXnya yang bagus ya*

## 2. Supplier dan dokumen supplier *ini boleh dibuat modulnya dulu dan formulirnya generate, kalau mereka belum isi berarti diremind lagi otomatis atau dikasih filter status*

Modul supplier sekarang terlalu sederhana. Supplier sebaiknya mempunyai profil:

- Nama perusahaan
- Alamat
- NPWP
- PIC
- Nomor WhatsApp/telepon
- Email
- Termin pembayaran
- Kategori barang yang dijual *ini diusahakan diisi banyak informasi, jadi lebih ke keyword barang apa yang mereka jual dan brand apa dalam satu kategori aja. kalau dalam formulir berarti mereka kasih satu input box dan bisa dipisahkan dengan tab dan dianjurkan buat menulis keyword banyak sesuai dengan yang mereka jual  supaya kita juga bisa tentuin mereka tuh jual apa, terkadang kita eh gatau juga mereka jualan ada barang ini kaya rukun aja baru tau ada merk vertex* 
- Catatan kualitas atau pengalaman *ini self isi sendiri, sisanya boleh dibuatin formulir*
- Status aktif/tidak aktif

Dokumen yang dapat dilampirkan:

- Kartu nama
- Brosur
- Katalog
- Price list
- NPWP
- Informasi rekening
- Dokumen lainnya

### Form untuk supplier

Bisa dibuat **link formulir supplier** yang dikirim melalui WhatsApp. Supplier dapat mengisi sendiri tanpa login. Link menggunakan token unik dan memiliki masa berlaku.

Namun data jangan langsung dianggap resmi. Alurnya:

`Supplier mengisi → status Menunggu Review → admin periksa → Simpan sebagai Supplier`

Price list dari supplier sebaiknya disimpan dengan:

- Tanggal berlaku
- File asli
- Barang/kategori 
- Harga jika ingin dimasukkan secara terstruktur
- Catatan
- Riwayat versi

Untuk tahap awal, cukup simpan katalog dan price list sebagai file. Belum perlu langsung membuat sistem perbandingan harga supplier yang rumit.

## 3. Cash flow yang simpel *kayanya ini hold dulu deh jangan ada perubahan*

Menurut saya jangan langsung membuat sistem akuntansi lengkap. Buat satu modul bernama **Kas & Bank** yang mencatat uang masuk dan keluar secara nyata.

Setiap transaksi berisi:

- Tanggal
- Kas atau rekening bank
- Uang masuk/keluar
- Kategori
- Nominal
- Metode: cash/transfer
- Customer atau supplier
- Terkait SO customer
- Nomor nota
- PPN/non-PPN
- Foto atau scan nota
- Keterangan
- Pembuat transaksi

### SOP uang kas Rp7 juta

Kas Rp7 juta sebaiknya diperlakukan sebagai **Kas Kecil/Petty Cash**:

1. Dicatat saldo awal atau pengisian kas: Rp7 juta.
    
2. Setiap nota cash dimasukkan sebagai pengeluaran kas.
    
3. Sistem otomatis menghitung:
    
    - Saldo awal
    - Total nota
    - Sisa uang fisik
4. Ketika diserahkan kepada manager, admin membuat **Batch Pertanggungjawaban Kas**.
    
5. Sistem menghasilkan daftar seluruh nota dalam batch tersebut.
    
6. Manager cukup memeriksa:
    
    `Saldo sistem = uang fisik tersisa`
    

Contoh:

| Keterangan         | Nilai       |     |
| ------------------ | ----------- | --- |
| Kas diberikan      | Rp7.000.000 |     |
| Total nota         | Rp4.350.000 |     |
| Seharusnya tersisa | Rp2.650.000 |     |
| Uang fisik         | Rp2.650.000 |     |
| Selisih            | Rp0         |     |
|                    |             |     |

Nota tidak perlu direkap ulang manual. Tinggal upload foto, masukkan nominal, dan pilih kategorinya.  *kayaknya proses kalau foto notanya ribet dan lama gak sih jatohnya? gua mikirnya ya notanya ditulis angka kode gitu keyID trus kalau mau cari ya cari fisiknya tapi ribet juga kayanya. enaknya gimana ya?*

### Pembelian transfer

Untuk nota yang langsung ditransfer:

- Buat transaksi pembelian
- Pilih rekening bank
- Masukkan tanggal transfer
- Upload bukti transfer dan nota
- Status otomatis `Sudah Dibayar`
- Sistem membuat kas keluar dari rekening tersebut

### Pembelian tempo/tagihan

Untuk nota yang belum dibayar:

- Status `Belum Dibayar`
- Isi tanggal jatuh tempo
- Nota disimpan/upload
- Muncul pada daftar tagihan supplier
- Ketika dibayar, pilih rekening dan tanggal pembayaran
- Sistem membuat kas keluar

Jadi tiga kondisi itu tidak perlu menjadi tiga modul:

- Cash → mengurangi Kas Kecil
- Transfer → mengurangi Bank
- Tempo → masuk Tagihan Supplier, lalu mengurangi Kas/Bank saat dibayar

## 4. Menghubungkan biaya pembelian ke SO

Ini bagian paling penting untuk mengetahui untung-rugi tiap order.

Setiap nota pembelian dapat dialokasikan ke:

- Satu SO
- Beberapa SO
- Biaya operasional umum

Contohnya nota supplier Rp10 juta:

|Alokasi|Nilai|
|---|---|
|SO-001|Rp6.000.000|
|SO-002|Rp3.000.000|
|Operasional|Rp1.000.000|

Karena satu nota bisa berisi barang untuk beberapa SO, relasinya jangan hanya satu `idInvoice` atau satu SO. Gunakan daftar **alokasi biaya**.

Untuk pembelian langsung berdasarkan order, admin cukup memilih SO customer ketika memasukkan nota. Kalau pembeliannya untuk stok atau operasional, pilih “Tidak terkait SO”.

### Laporan profit per SO

Sistem kemudian dapat menampilkan:

- Nilai penjualan sebelum PPN
- Total biaya barang
- Biaya tambahan langsung
- Laba kotor
- Margin
- Pembelian yang belum punya nota
- Nota yang belum dialokasikan

Contoh:

|Komponen SO-001|Nilai|
|---|---|
|Penjualan sebelum PPN|Rp15.000.000|
|Pembelian barang|Rp11.000.000|
|Ongkir|Rp500.000|
|Laba kotor|Rp3.500.000|
|Margin|23,3%|

Penting: perbandingan profit harus menggunakan nilai **sebelum PPN**, karena PPN bukan pendapatan atau biaya perusahaan.

Sistem juga dapat memberi peringatan:

- Harga beli item melebihi harga jual
- Total cost SO melebihi nilai penjualan
- Nota belum dialokasikan
- SO selesai tetapi dokumen pembelian belum lengkap

Saya menyarankan dua jenis margin:

- **Estimasi margin:** dari harga/modal saat SO dibuat.
- **Margin aktual:** dari nota supplier yang benar-benar masuk.


## 5. Otomatisasi laporan

Dengan struktur di atas, laporan berikut bisa otomatis:

### Operasional

- SO belum dikirim
- SO terkirim sebagian
- Sisa barang yang harus dikirim
- SO/SJ/invoice terdampak revisi
- SO belum ditagih

### Piutang customer

- Belum dibayar, dikelompokkan per customer
- Dikelompokkan per bulan invoice
- Sudah jatuh tempo
- Akan jatuh tempo
- Total pembayaran masuk

### Purchasing

- Tagihan supplier belum dibayar
- Jatuh tempo supplier
- Pembelian per supplier
- Pembelian per SO
- Nota belum di-upload
- Nota belum dialokasikan
- Rekap PPN dan non-PPN

### Keuangan

- Cash flow harian/bulanan
- Saldo setiap kas dan bank
- Rekap kas kecil
- Biaya operasional per kategori
- Omzet
- Profit per SO
- Margin per customer

Untuk omzet, tampilkan dua angka agar tidak membingungkan:

- **Omzet invoice:** invoice yang diterbitkan pada periode itu.
- **Uang masuk:** pembayaran yang benar-benar diterima pada periode itu.

## Prioritas implementasi yang paling masuk akal

### Tahap 1 — Kontrol order

- Revisi/versioning SO
- Indikator dokumen terdampak
- Penyempurnaan dashboard pengiriman parsial
- Peringatan kelebihan pengiriman/penagihan

### Tahap 2 — Purchasing dan dokumen

- Profil supplier lebih lengkap
- Upload kartu nama, katalog, price list, nota, dan bukti transfer
- Kategori barang supplier
- Form supplier melalui link
- Alokasi nota ke satu atau beberapa SO

### Tahap 3 — Keuangan ringan

- Master Kas & Rekening Bank
- Transaksi uang masuk/keluar
- Kas kecil Rp7 juta dan batch pertanggungjawaban
- Pembayaran cash, transfer, dan tempo
- Cash flow otomatis
- Profit aktual per SO

### Tahap 4 — Laporan otomatis

- Piutang per customer dan bulan
- Tagihan supplier
- Omzet versus uang masuk
- Biaya operasional
- Rekap PPN
- Margin per SO

Untuk jumlah penggunamu, saya juga tidak akan membuat permission kompleks. Cukup tiga akses:

- **Admin:** SO, SJ, invoice, supplier, dan pembelian.
- **Finance:** pembayaran, kas/bank, dan laporan.
- **Owner:** melihat semuanya dan koreksi tertentu.

UI untuk finance sebaiknya sangat sederhana: halaman awal berisi tombol besar **Uang Masuk**, **Uang Keluar**, **Bayar Tagihan**, **Kas Kecil**, dan **Laporan**.

Asumsi desain saya: mayoritas pembelian dilakukan untuk memenuhi SO tertentu, bukan untuk menyimpan stok besar. Kalau asumsi ini benar, kita belum perlu modul inventory/gudang—cukup kaitkan nota dan biaya langsung ke SO.

## Next
