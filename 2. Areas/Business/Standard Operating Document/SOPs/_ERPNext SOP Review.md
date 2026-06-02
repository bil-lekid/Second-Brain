---
tags:
  - Business
  - StandardOperatingDocument
  - SOP
  - ERPNext
  - Review
---

# ERPNext SOP Review

Tanggal kumpul: 2026-05-06

Note ini mengumpulkan SOP yang sekarang berhubungan dengan ERPNext, baik yang sudah eksplisit menyebut ERPNext maupun yang prosesnya kemungkinan masuk ke modul ERPNext.

## Prioritas Review

### P0 - Sudah langsung pakai/menyebut ERPNext
- [[III.9 Membuat Sales Order ERPNEXT]] - Sales Order di ERPNext dari PO customer.
- [[II.3. Cold Call-outreach, Telepon calon pelanggan baru.]] - Lead, CRM activity, follow-up, dan opportunity di ERPNext.

### P1 - Alur utama yang perlu nyambung ke ERPNext
- [[I.1. Menerima Purchase Order (PO) dan Organisasi PO]] - input awal dari customer PO menuju Sales Order.
- [[II.1. Meminta Penawaran Harga (PH)]] - request quotation dari customer sebelum transaksi.
- [[II.2. Mencari Harga Repeat (Harga yang sudah pernah dibeli).]] - referensi harga/customer/item history.
- [[III.1. Membuat Penawaran Harga (PH).]] - quotation admin; kemungkinan perlu dipindah dari Excel ke ERPNext.
- [[III.3. Membuat Surat Jalan.]] - Delivery Note/surat jalan dari Sales Order.
- [[III.4. Membuat Invoice.]] - Sales Invoice dari Delivery Note/Sales Order.
- [[VI.1. Coretax Pajak Keluaran (Impor XML)]] - pajak keluaran dari invoice.

### P2 - Purchasing, supplier, stock, dan fulfillment
- [[I.2. Delivery Order (DO) - Pesan Barang]] - pembelian barang ke supplier untuk memenuhi PO customer.
- [[I.3. Menerima nota, tagihan, dan Surat Jalan.]] - arsip nota/tagihan, pembelian, dan faktur pajak supplier.
- [[III.2. Prosedur Arsip Nota dan DO Pembelian.]] - Purchase Invoice Draft, klop nota supplier, dan arsip fisik per SO di manager/owner.
- [[I.5. Menanyakan Harga ke Supplier baru-lama]] - supplier quotation / price discovery.
- [[IV.2. Pengambilan dan Penerimaan Barang supplier.]] - penerimaan barang fisik dari supplier, tanpa wajib Purchase Receipt untuk workflow simpel ini.
- [[IV.3. Menanyakan-mencari harga ke supplier baru.]] - supplier discovery dan price capture.

### P3 - Terkait operasional/admin, tapi masih blank atau belum jelas
- [[II.4. Customer Relation Manager (CRM)]] - slot CRM, masih kosong.
- [[II.5. Penjualan pada toko]] - sales counter/toko.
- [[III.5. Membuat Tanda Terima]] - slot tanda terima, masih kosong.
- [[III.6. Pencatatan Penjualan.]] - slot pencatatan penjualan, masih kosong.
- [[III.7. Pencatatan Tagihan.]] - slot pencatatan tagihan, masih kosong.
- [[III.8. Pencatatan Penjualan.]] - duplikat slot pencatatan penjualan, masih kosong.
- [[IV.1. Pengantaran Barang ke pelanggan.]] - slot delivery/fulfillment, masih kosong.

## Yang Tidak Dimasukkan

- [[I.4. Laporan Uang Kas]] - bisa masuk Accounting ERPNext, tapi saat ini blank dan belum ada konteks ERPNext.
- [[I.6. Log in ke akun gmail purchasing]] - pendukung purchasing, bukan proses ERPNext langsung.
- [[V.1. Pembelian Barang Kantor]] - office purchase, bukan alur transaksi utama customer/supplier.
- [[V.2. Proses Rekrutmen]] - HR.
- [[V.3. Sistem masukan-opini (feedback)]] - feedback internal.

## Checklist Review ERPNext

- [ ] Tentukan dokumen ERPNext untuk tiap SOP: Lead, Opportunity, Quotation, Sales Order, Delivery Note, Sales Invoice, Purchase Invoice Draft, Purchase Invoice, Payment Entry.
- [ ] Tandai bagian yang masih pakai Excel/buku/manual dan putuskan apakah tetap manual atau pindah ke ERPNext.
- [ ] Cek field wajib: customer, supplier, item, UOM, quantity, rate, tax category, payment terms, address, contact, nomor PO customer, nomor SO reference.
- [ ] Cek approval point: siapa input, siapa cek, siapa submit.
- [ ] Cek case "PO menyusul": bukti request customer tersimpan dan manager/owner approve sebelum beli/kirim.
- [ ] Cek dokumen cetak: format Sales Order, Surat Jalan, Invoice, Tanda Terima.
- [ ] Cek naming/numbering: nomor PO customer, nomor surat jalan, nomor invoice, dan nomor dokumen ERPNext.
- [ ] Cek pajak: PPN 11%, tax category, Coretax/XML, faktur pajak.
- [ ] Cek stock flow: barang dari supplier, barang stock lama, barang untuk customer/PO tertentu.
- [ ] Cek arsip bukti fisik/digital: PO, DO, nota, surat jalan, invoice, faktur pajak, tanda terima.

## Embed SOP Untuk Review

### P0 - Langsung ERPNext

![[III.9 Membuat Sales Order ERPNEXT]]

![[II.3. Cold Call-outreach, Telepon calon pelanggan baru.]]

### P1 - Sales, Delivery, Invoice, Tax

![[I.1. Menerima Purchase Order (PO) dan Organisasi PO]]

![[II.1. Meminta Penawaran Harga (PH)]]

![[II.2. Mencari Harga Repeat (Harga yang sudah pernah dibeli).]]

![[III.1. Membuat Penawaran Harga (PH).]]

![[III.3. Membuat Surat Jalan.]]

![[III.4. Membuat Invoice.]]

![[VI.1. Coretax Pajak Keluaran (Impor XML)]]

### P2 - Purchasing, Supplier, Stock

![[I.2. Delivery Order (DO) - Pesan Barang]]

![[I.3. Menerima nota, tagihan, dan Surat Jalan.]]

![[III.2. Prosedur Arsip Nota dan DO Pembelian.]]

![[I.5. Menanyakan Harga ke Supplier baru-lama]]

![[IV.2. Pengambilan dan Penerimaan Barang supplier.]]

![[IV.3. Menanyakan-mencari harga ke supplier baru.]]

### P3 - Slot Yang Perlu Dicek

![[II.4. Customer Relation Manager (CRM)]]

![[II.5. Penjualan pada toko]]

![[III.5. Membuat Tanda Terima]]

![[III.6. Pencatatan Penjualan.]]

![[III.7. Pencatatan Tagihan.]]

![[III.8. Pencatatan Penjualan.]]

![[IV.1. Pengantaran Barang ke pelanggan.]]
