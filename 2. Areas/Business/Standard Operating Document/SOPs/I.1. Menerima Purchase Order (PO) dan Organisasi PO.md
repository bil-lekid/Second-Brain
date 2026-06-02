---
tags:
  - Business
  - StandardOperatingDocument
  - SOP
  - Purchasing
---

# I.1. Menerima Purchase Order (PO) dan Organisasi PO

## Alur Normal: PO Customer Sudah Ada

1. PO customer dikirim oleh sales/customer melalui email atau WA.
2. Admin save file PO customer ke folder customer di OneDrive.
3. Admin print PO customer.
4. Admin buat Sales Order (SO) Draft di ERPNext.
5. Admin tulis nomor SO di PO customer fisik.
6. Admin input item, quantity, harga, tax, dan payment terms di SO Draft.
7. Manager/owner cek SO Draft.
8. Kalau SO belum OK, admin revisi SO Draft.
9. Kalau SO sudah OK:
	1. Admin print SO.
	2. Manager/owner simpan SO fisik sebagai arsip.
	3. PO customer fisik diberikan ke purchasing sebagai pegangan pembelian dan cari harga.
10. Purchasing menggunakan PO customer fisik untuk pembelian, dan menggunakan nomor SO untuk pencatatan DO/nota/bukti pembelian.
11. Untuk masing-masing barang pada PO customer, purchasing mengikuti [[I.2. Delivery Order (DO) - Pesan Barang]].
12. Kalau barang untuk satu PO customer sudah lengkap, purchasing kasih PO customer ke admin/manager.
13. Owner menentukan jadwal pengiriman.
14. Setelah jadwal pengiriman ditentukan, admin membuat surat jalan dan invoice.

## Alur Khusus: Customer Minta Kirim Dulu, PO Menyusul

1. Admin buat SO Draft di ERPNext.
2. Di nomor PO customer, isi sementara "PO menyusul".
3. SO Draft dicetak dan diberikan ke Manager/owner.
4. Manager/owner wajib approve sebelum barang dibeli atau dikirim.
5. Setelah approved, purchasing menerima SO print untuk pembelian.
6. Saat PO customer resmi datang, admin update nomor PO customer di ERPNext dan arsip.

Note:
1. Jangan kirim barang tanpa PO customer kecuali sudah approved oleh manager/owner.
