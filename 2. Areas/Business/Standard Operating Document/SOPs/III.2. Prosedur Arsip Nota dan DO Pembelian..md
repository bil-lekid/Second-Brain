---
tags:
  - Business
  - StandardOperatingDocument
  - SOP
  - DraftSOP
  - Admin
---

# III.2. Prosedur Arsip Nota dan DO Pembelian.

Source (Notion): https://www.notion.so/29d796f898d780aeb8e3cbd06008ed88
Department: Admin  
Status: Draft  
Last Updated: 2026-05-08

## Tujuan

SOP ini mengatur pencatatan pembelian dari purchasing ke ERPNext, mulai dari bukti pembelian masuk sampai Purchase Invoice difinalisasi dan arsip fisik disimpan manager/owner.

## Prinsip

- Nomor Sales Order (SO) adalah reference utama untuk pembelian.
- Pembelian dicatat per SO/customer.
- Purchase Invoice dibuat Draft saat barang datang, walaupun nota asli supplier belum lengkap.
- Purchase Receipt tidak wajib dibuat untuk workflow ini.
- Purchase Invoice Draft tidak perlu dicetak.
- Nomor Purchase Invoice Draft ditulis di bukti pembelian fisik.
- Nota pembelian diarsip urut per SO dan disimpan manager/owner.

## Alur Admin Input Purchase Invoice Draft

1. Purchasing memberikan bukti pembelian ke admin setelah barang datang.
2. Bukti pembelian bisa berupa:
	1. PO/DO tulis tangan.
	2. Nota supplier.
	3. Struk.
	4. Screenshot WA.
	5. Catatan pembelian purchasing.
	6. Foto barang disertai info supplier dan harga.
3. Admin cek informasi minimal:
	1. Nomor SO.
	2. Nama supplier.
	3. Nama customer.
	4. Nama barang.
	5. Jumlah barang.
	6. Nominal pembelian sementara jika ada.
4. Admin buka ERPNext dan buat Purchase Invoice.
5. Purchase Invoice disimpan sebagai Draft.
6. Isi reference SO di Purchase Invoice supaya pembelian bisa ditelusuri ke customer/SO.
7. Jika ada foto PO/DO/nota/struk/screenshot, admin attach ke Purchase Invoice.
8. Admin tulis nomor Purchase Invoice Draft di bukti pembelian fisik.
9. Kalau nota asli belum ada, beri catatan "Pending Nota".

## Saat Nota Pembelian Supplier Datang

1. Admin cocokkan nota pembelian supplier dengan Purchase Invoice Draft berdasarkan nomor Purchase Invoice yang tertulis di bukti fisik.
2. Admin cek:
	1. Nama supplier.
	2. Nama barang.
	3. Jumlah barang.
	4. Harga beli.
	5. PPN/non-PPN.
	6. Total pembelian.
	7. Nomor SO/customer terkait.
3. Kalau ada selisih, admin revisi Purchase Invoice Draft atau koordinasi ke purchasing/manager.
4. Kalau sudah cocok, Purchase Invoice Draft dan nota pembelian dipakai untuk laporan uang kas.

## Laporan Uang Kas dan Refill

1. Finance/admin hitung total pembelian yang memakai uang kas.
2. Cocokkan uang kas keluar dengan nota pembelian.
3. Cocokkan pembelian dengan nomor SO/customer.
4. Ajukan refill uang kas jika perlu.
5. Manager/owner approve refill uang kas.

## Finalisasi Admin

1. Admin cari Purchase Invoice Draft di ERPNext berdasarkan nomor Purchase Invoice yang tertulis di bukti fisik.
2. Admin edit Purchase Invoice sesuai nota pembelian final.
3. Admin foto/scan nota pembelian dan attach ke Purchase Invoice.
4. Admin finalisasi Purchase Invoice setelah data sesuai.
5. Admin susun nota pembelian berdasarkan nomor SO.
6. Arsip fisik diberikan ke manager/owner untuk disimpan.

## Output Akhir

- Purchase Invoice ERPNext final dan punya attachment nota pembelian.
- Pembelian bisa dilihat per SO/customer.
- Nota fisik tersusun per SO.
- Manager/owner menyimpan arsip fisik.
- Finance bisa cek pembelian, kas, dan margin dari ERPNext serta arsip fisik saat diperlukan.


