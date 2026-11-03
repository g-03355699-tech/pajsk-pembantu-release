# PAJSK Pembantu — Muat Turun

Chrome extension untuk membantu guru mengisi **PAJSK** dalam SPPB (moeissppb.moe.gov.my): isi automatik dari Excel/CSV, isi pukal satu kelas, eksport CSV dan semakan data murid yang belum lengkap.

## ⬇️ [Muat turun versi terkini (zip)](https://github.com/g-03355699-tech/pajsk-pembantu-release/raw/main/pajsk-pembantu.zip)

Versi semasa: lihat [`latest.json`](latest.json). Versi lama ada dalam folder [`versi/`](versi/).

## Pemasangan kali pertama
1. Muat turun zip di atas dan unzip ke satu folder tetap (cth. `Documents\pajsk-pembantu`).
2. Chrome → `chrome://extensions` → hidupkan **Developer mode**.
3. **Load unpacked** → pilih folder `pajsk-pembantu`.
4. Pin ikon **PAJSK Pembantu** pada toolbar.
5. Jika halaman SPPB sudah terbuka, tekan **F5** supaya butang hijau **PAJSK** muncul.

## Cara guna (ringkas)
1. Ikon → **Import data & tetapan** → pilih fail Excel (cth. eksport *table2excel*). Murid dipadankan ikut No. KP.
2. Pastikan fail ada lajur **Jawatan Khas** jika mahu tab Ekstra Kurikulum diisi.
3. Tetapkan **nilai lalai** setiap komponen: Jawatan (cth. `AHLI AKTIF`), Pelibatan, Komitmen (maks. 4), Khidmat, Kehadiran.
4. SPPB → Keputusan → PAJSK → kelas → buka seorang murid → butang **PAJSK** → **💾 Isi & Simpan semua tab** → semak setiap tab.
5. Tetapan bahagian 3: sahkan padanan nama aktiviti (fail ↔ SPPB).
6. Halaman Senarai Murid → **▶ Mula isi pukal**, atau dari halaman murid → **⏩ Isi & simpan murid ini dan seterusnya**.
7. **🔍 Semak data** dan **⬇ Eksport CSV** pada halaman Senarai Murid.

## Kemas kini
Extension menyemak versi baharu secara automatik. Apabila ada, ikon menunjukkan lencana **NEW** dan notis kuning muncul dalam popup dan panel PAJSK.
1. Klik **Muat turun versi baharu**.
2. Unzip dan **gantikan fail dalam folder yang sama** (data dan tetapan anda kekal).
3. `chrome://extensions` → tekan ↻ **Reload** pada PAJSK Pembantu.
4. Tekan F5 pada halaman SPPB.

> Sentiasa semak borang sebelum menyimpan, terutamanya kali pertama. Semua data murid diproses dan disimpan dalam pelayar anda sahaja — tiada data dihantar ke pelayan lain.

## 📞 Hubungi
- **Cikgu Ibrahim bin Kadri** — SM Sains Kuala Selangor
- WhatsApp: [019-300 2591](https://wa.me/60193002591?text=Salam%20Cikgu%20Ibrahim%2C%20berkenaan%20PAJSK%20Pembantu.)
- Emel: [ibrahim.kadri@kusess.edu.my](mailto:ibrahim.kadri@kusess.edu.my?subject=PAJSK%20Pembantu)

## 📝 Changelog

### v1.8.1 — 3 Nov 2026
- **Betulkan:** *Isi & simpan murid ini dan seterusnya* tersekat selepas murid pertama. Apabila butang *Seterusnya* ditekan, SPPB memaparkan dialog **"Amaran — … Klik OK sekiranya anda pasti untuk berganti murid"**; extension kini menekan **OK** secara automatik (semua tab sudah disimpan sebelum itu).

### v1.8.0 — 3 Nov 2026
- Butang baharu di halaman murid: **⏩ Isi & simpan murid ini dan seterusnya** — isi & simpan semua tab, tekan *Seterusnya* SPPB, ulang sehingga murid terakhir.
- Semasa isi pukal: **⏩ Simpan & Auto (tanpa jeda)** untuk berhenti menjeda pada setiap tab, dan **⏸ Jeda untuk semak** untuk kembali menjeda.
- Dialog SPPB **"Berjaya! Rekod telah berjaya ditambah"** ditutup secara automatik (butang OK) dan digunakan untuk mengesahkan simpanan; dialog ralat menghentikan proses.

### v1.7.1 — 3 Nov 2026
- Betulkan ralat **Extension context invalidated** yang muncul di `chrome://extensions` apabila extension dikemas kini atau dimuat semula (↻) semasa halaman SPPB masih terbuka. Halaman lama kini memaparkan notis kecil *"Tekan F5 untuk menyambung"*.

### v1.7.0 — 3 Nov 2026
- **Setiap tab disimpan sebelum ke tab seterusnya.** SPPB hanya menyimpan tab yang sedang dibuka — sebelum ini isian tab lain boleh hilang. Kini: isi Kelab → Simpan → isi Badan Beruniform → Simpan → Sukan → Simpan → Ekstra → Simpan.
- Panel murid: **💾 Isi & Simpan semua tab** dan **✎ Isi tab ini sahaja** (tanpa simpan, untuk disemak).
- Isi pukal: pilihan jeda kini **pada setiap tab** (*Simpan & Teruskan* / *Langkau tab* / *Langkau murid*); kemajuan tab yang sudah disimpan dipaparkan dan disambung semula jika halaman dimuat semula.
- Komponen tanpa aktiviti yang suis DITAKSIRnya dimatikan juga disimpan.

### v1.6.0 — 3 Nov 2026
- **Perkhidmatan dipadankan dengan tepat** daripada Jawatan Khas murid (cth. *Pengawas Biasa* → *PENGAWAS/PENGAWAS PUSAT SUMBER/…\|7*, *PRS* → *…/PRS/…\|5*). Nilai lalai di Tetapan tidak lagi menggantikan Jawatan Khas.
- Jika padanan **tidak pasti** (cth. *AJK Kelas/Kamar*, *J/k Pusat Media*), ruangan tidak diisi dan nama itu ditanda **⚠ Perlu dipetakan** di Tetapan → bahagian 3.
- **Semakan sebelum isi pukal**: senarai nama yang belum dipetakan dipaparkan sebelum mula.
- Betulkan: data yang diimport dengan versi lama kini turut membaca lajur Jawatan Khas.
- Betulkan: suis DITAKSIR bagi komponen tanpa aktiviti kini dimatikan dengan lebih andal; jika gagal, ralat dipaparkan dan borang tidak disimpan.

### v1.5.0 — 3 Nov 2026
- **Betulkan:** Jawatan kadang-kadang tidak diisi (terutama Badan Beruniform) kerana senarai jawatan lambat dimuatkan oleh SPPB selepas aktiviti dipilih. Extension kini menunggu dan cuba semula; jika jawatan tetap gagal, ia dikira ralat dan borang **tidak** disimpan.
- **Jawatan sandaran** dalam nilai lalai: cth. AHLI AKTIF, jika tiada dalam senarai aktiviti itu → AHLI BIASA.
- **Eksport / import tetapan** (Tetapan → bahagian 5): simpan atau kongsi nilai lalai, peta padanan dan tetapan sebagai fail .json. Data murid hanya disertakan jika ditanda.

### v1.4.0 — 3 Nov 2026
- Tetapan → Ekstra Kurikulum: dropdown **Perkhidmatan** lalai dan dropdown **TIMSS dan PISA**.
- Padanan Jawatan Khas → kategori Perkhidmatan SPPB (cth. *Pengawas Biasa* → *PENGAWAS/PENGAWAS PUSAT SUMBER/…\|7*); kategori yang tidak pasti boleh dipilih dalam bahagian 3 Tetapan.
- Nilai lalai **Jawatan** kini dropdown untuk semua komponen. Jawatan khusus (cth. LANS KOPERAL, BRASS BAND bagi Badan Beruniform) ditambah ke senarai secara automatik selepas dropdown Jawatan SPPB dibuka sekali; pilihan *Lain-lain* untuk menaip sendiri.

### v1.3.0 — 3 Nov 2026
- Tab **Ekstra Kurikulum** lengkap: **Anugerah Khas** (termasuk Emas/Perak/Gangsa Anugerah Remaja Perdana), **Khidmat Masyarakat**, **Program NILAM** dan **TIMSS/PISA**.
- Tetapan → Nilai lalai kini ada tab **Ekstra Kurikulum**.
- Lajur baharu dalam fail: `Anugerah Khas`, `Khidmat Masyarakat` (cth. `KEJIRANAN:2; ALAM SEKITAR:1`), `NILAM` (1–5), `TIMSS PISA`.

### v1.2.0 — 3 Nov 2026
- Sokongan tab **Ekstra Kurikulum**: lajur *Jawatan Khas* dalam fail (Pengawas, AJK Kelas, PRS, J/K Pusat Media dll.) diisi ke dropdown **Perkhidmatan**.
- Suis DITAKSIR Ekstra dimatikan bagi murid yang tiada jawatan khas.
- Semak data dan Eksport CSV kini merangkumi Ekstra Kurikulum.

### v1.1.0 — 3 Nov 2026
- **Semakan kemas kini automatik**: lencana NEW pada ikon, notis versi baharu dalam popup dan panel PAJSK, pautan "Semak kemas kini".

### v1.0.1 — 3 Nov 2026
- Popup memaklumkan jika halaman SPPB perlu dimuat semula (F5).
- Contoh jawatan ditukar kepada AHLI AKTIF.

### v1.0.0 — 3 Nov 2026
- Keluaran pertama: isi automatik dari Excel/CSV, isi pukal satu kelas, eksport CSV, semakan data, padanan nama aktiviti dan peta manual.
