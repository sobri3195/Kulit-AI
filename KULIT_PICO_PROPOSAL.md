# Kulit — AI Deteksi *Steroid Misuse/Overuse* dari Foto Serial + Pola Belanja Obat

## 1) Pertanyaan klinis (PICO)

**P (Population):**
Pasien dermatitis/jerawat yang menggunakan topikal steroid, terutama steroid OTC, usia ≥12 tahun, datang ke layanan primer/klinik kulit.

**I (Intervention):**
Intervensi berbasis AI “Kulit” yang menggabungkan:
1. Analisis foto serial lesi (timeline) untuk deteksi pola memburuk yang konsisten dengan steroid misuse/overuse.
2. Kuesioner terstruktur terkait durasi, frekuensi, lokasi pemakaian, potensi steroid, serta gejala rebound.
3. Data pembelian/apotek (opsional, dengan consent) untuk melihat frekuensi refill, switching merek, dan pembelian multipel.
4. Output risk stratification + rekomendasi konseling terpersonalisasi untuk klinisi/pasien.

**C (Comparison):**
Konseling standar tanpa dukungan AI.

**O (Outcomes):**
- **Primer:** Penurunan kejadian steroid-induced dermatitis/atrofi dalam 3–6 bulan.
- **Sekunder:**
  - Kontrol gejala (mis. skor gejala dermatitis/akne sesuai protokol lokal).
  - Kepatuhan regimen (penggunaan obat sesuai rencana tapering/substitusi).
  - Kualitas hidup dermatologi (DLQI).
  - Penurunan pemakaian steroid potensi menengah-tinggi tanpa indikasi kuat.
  - Penurunan kunjungan ulang karena rebound flare.

---

## 2) Tujuan studi

### Tujuan utama
Menilai apakah penggunaan AI “Kulit” menurunkan insiden efek samping terkait misuse/overuse steroid topikal dibanding konseling standar.

### Tujuan tambahan
1. Menilai dampak AI pada kepatuhan terapi dan kualitas hidup (DLQI).
2. Mengevaluasi akurasi model dalam mengidentifikasi pasien berisiko tinggi.
3. Menilai kelayakan implementasi alur kerja AI di praktik rutin.

---

## 3) Hipotesis

- **Hipotesis utama:** Kelompok intervensi AI memiliki insiden steroid-induced dermatitis/atrofi lebih rendah dibanding kontrol.
- **Hipotesis sekunder:** Kelompok intervensi menunjukkan DLQI lebih baik, kepatuhan regimen lebih tinggi, dan kebutuhan steroid potensi tinggi yang tidak tepat lebih rendah.

---

## 4) Rancangan yang direkomendasikan

- **Desain:** Randomized controlled trial pragmatik (parallel-group, 1:1).
- **Setting:** Klinik kulit/layanan primer dengan volume pasien tinggi pengguna steroid topikal.
- **Durasi follow-up:** Minimal 12 minggu; ideal 24 minggu untuk menangkap rebound/atrofi.
- **Blinding:** Peserta/klinisi sulit dibutakan, namun adjudicator outcome klinis diupayakan blinded.

---

## 5) Definisi operasional outcome

1. **Steroid-induced dermatitis/atrofi (primer):**
   Ditetapkan oleh dokter berdasarkan kriteria klinis terstandar (mis. kulit menipis, telangiektasia, rosacea-like flare, perioral dermatitis terkait steroid).
2. **Kontrol gejala:**
   Perubahan skor gejala dari baseline ke minggu 12/24.
3. **Kepatuhan regimen:**
   Persentase hari sesuai regimen (self-report terstruktur + verifikasi resep/refill bila tersedia).
4. **DLQI:**
   Perubahan skor DLQI dari baseline ke endpoint.

---

## 6) Komponen AI “Kulit” (ringkas)

1. **Input multimodal:** Foto serial, jawaban kuesioner, metadata obat, data pembelian (opsional).
2. **Feature fusion:**
   - Visual progression features dari foto antar waktu.
   - Behavioral features (durasi pakai, escalation pattern).
   - Purchase behavior features (refill interval, OTC redundancy).
3. **Output:**
   - Skor risiko (rendah/sedang/tinggi).
   - Alasan utama prediksi (explainability ringkas).
   - Saran konseling: tapering, alternatif non-steroid, edukasi red flags.

---

## 7) Catatan implementasi etika & regulasi

- **Consent eksplisit** untuk foto serial dan integrasi data apotek.
- **Data minimization**: hanya data relevan klinis.
- **Keamanan data**: enkripsi at-rest/in-transit, audit log akses.
- **Human-in-the-loop**: AI sebagai decision support, bukan pengganti diagnosis.
- **Bias monitoring**: evaluasi performa lintas usia, jenis kulit, dan tingkat keparahan.

---

## 8) Rumusan singkat untuk proposal

> Pada pasien dermatitis/jerawat pengguna steroid topikal (khususnya OTC), apakah dukungan AI multimodal (foto serial + kuesioner pemakaian + data pembelian opsional), dibanding konseling standar tanpa AI, dapat menurunkan kejadian steroid-induced dermatitis/atrofi serta memperbaiki kontrol gejala, kepatuhan regimen, dan kualitas hidup (DLQI)?

