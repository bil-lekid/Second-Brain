---
tags:
  - SOP
  - Tax
  - Coretax
---

# Coretax – Pajak Keluaran (Impor XML)

Referensi DJP (template + converter): https://www.pajak.go.id/id/reformdjp/coretax/template-xml-dan-converter-excel-ke-xml

## Intinya
Isi Excel → convert jadi XML → import ke Coretax → cek draft → kirim & tanda tangan elektronik.

## Rules paling penting (template v1.6)
- `Jenis Faktur`: **selalu `Normal`**.
- `Baris`: urut mulai **1** (satu faktur = satu baris di sheet `Faktur`).
- Kalau `Kode Transaksi` = **`07` atau `08`**:
  - `Keterangan Tambahan` **wajib**
  - `Cap Fasilitas` **wajib**
- `Referensi`: pakai **nomor invoice internal** (rule internal).
- `ID TKU Penjual`: **wajib 22 digit (NITKU)** NPWP + 000000.
- Pembeli `TIN`:
  - `NPWP/NIK Pembeli`: di sample terisi **16 digit**
  - `ID TKU Pembeli` = **`NPWP/NIK Pembeli` + `000000`** (jadi 22 digit)
  - `Nomor Dokumen Pembeli`: isi `-`
- Kalau `Jenis ID Pembeli` **bukan** `TIN`:
  - `NPWP/NIK Pembeli` = `0000000000000000`
  - `ID TKU Pembeli` = `000000`
- Sheet `DetailFaktur`:
  - `Baris` harus match `Faktur.Baris`
  - Angka (harga/qty/dpp/dll) max **2 desimal**
  - `Total Diskon`: kalau tidak ada isi `0`
  - `Tarif PPnBM` & `PPnBM`: kalau tidak ada isi `0`

## Cara isi (ceklist singkat)
### 1) Sheet `Faktur` (header)
Isi minimal: `Baris`, `Tanggal Faktur`, `Jenis Faktur`, `Kode Transaksi`, `Referensi`, `ID TKU Penjual`, data pembeli (`NPWP/NIK`, `Jenis ID`, `Negara`, `Nama`, `Alamat`, `ID TKU Pembeli`).

### 2) Sheet `DetailFaktur` (item)
Untuk tiap item, isi: `Baris`, `Barang/Jasa` (A=Barang, B=Jasa), `Nama Barang/Jasa`, `Nama Satuan Ukur`, `Harga Satuan`, `Jumlah`, `Diskon`.
Biarkan formula hitung `DPP/PPN` jalan (jangan copas sebagai value kalau bisa).

### 3) Convert & Import
1. Jalankan converter DJP → pilih jenis XML: **Faktur Pajak Keluaran** → simpan XML.
2. Coretax: `e-Faktur` → `Pajak Keluaran` → `Impor Data` → pilih XML.
3. Cek draft → **Kirim** → tanda tangan elektronik.

