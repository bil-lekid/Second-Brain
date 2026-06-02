---
tags:
  - SOP
  - PersonalKnowledgeManagement
  - Productivity
---
# SOP: Fleeting to PARA (Distill, Express, Publish)

## Prinsip
- Semua ide mentah masuk dulu ke `0. Fleeting/` (flat, Zettelkasten-style).
- Selama belum rapi/siap pakai, note harus tetap punya tag `Fleeting`.
- Saat sudah "processed" dan dipindah ke PARA, tag `Fleeting` dihapus.

## Definisi (4 tahap)
- `Capture` (tangkap): catat cepat, minim friksi.
- `Distill` (saring): bikin intinya jelas, buang noise.
- `Express` (ekspresikan): ubah jadi output yang bisa dipakai orang lain atau diri sendiri.
- `Publish` (publikasi): share ke luar (opsional).

## Aturan Tag & Status
- Tag wajib saat capture: `Fleeting`.
- Tag topik boleh ditambah kapan saja (mis. `Business`, `Relationship`, `Finance`).
- Saat sudah processed: hapus `Fleeting` dan pindahkan note ke folder PARA yang tepat.
- Opsional (biar otomatis enak): pakai frontmatter `status: inbox|distilled|expressed|published`.

## SOP Harian (Capture)
1. Buat note baru di `0. Fleeting/`.
2. Pastikan frontmatter punya `tags: [Fleeting]` (template sudah disiapkan).
3. Tulis 3 hal minimum:
   - `Capture`: apa yang kepikiran?
   - `Next`: langkah kecil selanjutnya (kalau ada).
   - Link kalau terkait note lain.

## SOP Sabtu/Minggu (Weekly Organize)
Target: `0. Fleeting/Fleeting Inbox.md` kosong dari hal yang "nggantung".

1. Buka `0. Fleeting/Fleeting Inbox.md`.
2. Untuk setiap note bertag `Fleeting`, pilih salah satu jalur:
   - `Delete`: kalau nggak penting / duplikat.
   - `Keep as Fleeting`: kalau masih ide mentah tapi layak disimpan.
   - `Distill`: tulis ringkasan 3-7 bullet, tambah link, rapikan judul kalau perlu.
   - `Express`: ubah jadi checklist, SOP, outline blog, atau draft yang bisa dieksekusi.
   - `Move to PARA`: pindahkan ke `1. Projects/` atau `2. Areas/` atau `3. Resouces/` sesuai fungsi, lalu hapus tag `Fleeting`.

3. Kalau note sudah pindah ke PARA:
   - Pastikan ada tag topik yang jelas.
   - Pastikan muncul di MOC tag terkait (lihat folder `3. Resouces/Personal Knowledge Management/MOCs/Tags/`).

## Mapping Fleeting -> PARA (aturan praktis)
- Ke `1. Projects/` bila ada outcome + deadline + next action nyata.
- Ke `2. Areas/` bila itu ongoing responsibility (kesehatan, finance, relationship, kerja).
- Ke `3. Resouces/` bila itu referensi/knowledge untuk dipakai lagi.
- Ke `4. Archive/` bila sudah selesai dan jarang dipakai, tapi ingin disimpan.

## Publish (Obsidian)
Obsidian bisa publish dengan 2 cara umum:
- `Obsidian Publish` (layanan berbayar): paling gampang untuk publish vault/notes ke web.
- Export/self-host: export Markdown lalu publish pakai static site generator (mis. Quartz/MkDocs/Hugo) atau platform lain.

Rule sederhana:
- Kalau note masih `Fleeting`, jangan publish.
- Publish setelah `Express` (sudah jadi output yang enak dibaca).

