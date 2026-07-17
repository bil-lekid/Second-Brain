---
tags:
  - Business
  - StandardOperatingDocument
  - SOP
  - Admin
Divisi: III. Admin
---

# III. 9 Membuat Sales Order ERPNEXT

## Prinsip

- Sales Order (SO) dibuat secepat mungkin supaya semua pembelian punya nomor tracking.
- PO customer disimpan admin di folder customer OneDrive sebelum dicetak.
- PO customer fisik diberikan ke purchasing sebagai pegangan pembelian.
- Nomor SO ditulis di PO customer fisik untuk pencatatan DO/nota/bukti pembelian.

## Alur Membuat Sales Order

1. Buka erp.primaputraperkasa.com.
2. Login.
3. Buka Purchase Order customer pada tab windows berbeda, safe juga pdf purchase order pada folder onedrive\purchase order.
4. Tekan `ctrl+g` dan cari `Sales Order List`.
5. Tekan tambah Sales Order.
6. Isi customer.
7. Isi customer purchase order:
	1. Jika PO customer sudah ada, isi nomor PO customer.
	2. Jika PO customer belum ada, isi "PO menyusul".
8. Isi tanggal PO customer:
	1. Jika PO customer sudah ada, isi tanggal sesuai dokumen PO.
	2. Jika PO customer belum ada, isi tanggal request customer.
9. Isi bagian barang sesuai PO customer atau request customer:
	1. Item code: isi `Trading Barang Mekanikal` jika belum ada item code khusus.
	2. Item name: isi nama barang.
	3. Description: isi detail barang jika perlu.
	4. Quantity: isi jumlah barang.
	5. UOM: isi satuan barang, misalnya pcs, pak, klg, dll.
10. Isi sales and tax category. Gunakan Indonesian tax untuk PPN Indonesia.
11. Pastikan address contact, billing address, dan contact person terisi sesuai.
12. Isi payment terms sesuai customer, misalnya Net 30 atau Net 60.
13. Save sebagai Draft.
14. Nomor Sales Order berupa SAL-ORD-YYYY-XXXXX muncul, rename file pdf tambahkan nomor sales order di depan nama file (nama file - nomor sales order.pdf).
15. Admin Print SO Draft, berikan ke manager.
16. Manager/owner cek SO Draft.
17. Kalau SO belum OK, admin revisi.

## Jika PO Customer Belum Ada

1. Admin save bukti request customer ke folder customer OneDrive.
2. Isi customer purchase order dengan "PO menyusul".
3. Manager/owner wajib approve sebelum barang dibeli atau dikirim.
4. Saat PO customer resmi datang, admin update nomor PO customer di ERPNext dan arsip.


