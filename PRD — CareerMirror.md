# PRD — CareerMirror

Nov 23, 2026 · @Jewan Enjoyer

## Ringkasan

**CareerMirror** adalah simulator kesiapan karier untuk mahasiswa dan lulusan baru. Pengguna memasukkan CV, minat, dan preferensinya. CareerMirror lalu menemukan peluang yang cocok (magang, kerja, program, kompetisi), menunjukkan seberapa siap ia untuk setiap peluang, mensimulasikan wawancara yang spesifik untuk peluang itu, dan memberi rencana konkret untuk menutup kesenjangannya.

**One-liner:** *Lihat dirimu dari kacamata perekrut, sebelum perekrut benar-benar melihatmu.*

**Konsep inti:** Semua fitur berpusat pada satu **Profil Karier** yang terus diperbarui. Profil ini dibangun dari bukti nyata (CV, portofolio, proyek), bukan dari pengakuan diri. Profil Karier dicocokkan dengan kebutuhan nyata industri dari data lowongan. Hasilnya adalah siklus: *temukan peluang → ukur kesiapan → latih wawancara → tutup kesenjangan → lamar*.

**Keunikan:** menghubungkan proses belajar, evaluasi kemampuan, dan kebutuhan industri dalam satu alur. Pengguna tidak hanya tahu *di mana* ia bisa melamar, tapi juga *seberapa siap* dan *apa yang harus dilakukan* agar siap.

**Subtema Hackvidia:** utama *AI for Learning & Self-Growth*. Pendukungnya *AI for Daily Living* (mempermudah proses mencari kerja) dan *AI for Inclusive Access* (mahasiswa dari kampus dengan pusat karier terbatas mendapat pendampingan yang setara).

## Masalah

Banyak mahasiswa tidak tahu seberapa siap mereka menghadapi dunia kerja, peluang apa yang realistis untuk dilamar, dan apa yang harus diperbaiki. Mereka baru sadar setelah ditolak berkali-kali, tanpa tahu alasannya.

- **Lulusan perguruan tinggi pun banyak yang menganggur.** Per Mei 2026, sekitar 1,03 juta lulusan D4 sampai S3 menganggur, atau 14,31% dari total 7,22 juta penganggur ([detikFinance, data BPS](https://finance.detik.com/berita-ekonomi-bisnis/d-8605483/bps-ungkap-1-juta-lulusan-s1-s3-di-ri-masih-nganggur)).
- **Masa tunggunya panjang.** Lulusan perguruan tinggi rata-rata butuh 19,8 bulan untuk mendapat pekerjaan. Salah satu penyebabnya adalah ketidaksesuaian kompetensi lulusan dengan kebutuhan industri (*skill mismatch*) ([Kompas, mengutip LPEM FEB UI](https://lestari.kompas.com/read/2026/07/28/143621786/tanoto-foundation-employability-mahasiswa-harus-diasah-sejak-menempuh)).
- **Anak muda paling terdampak.** Tingkat pengangguran usia 15–24 tahun naik menjadi 17,37% pada Mei 2026 ([CNBC Indonesia](https://cnbcindonesia.com/news/20260806131950-4-757114/tingkat-pengangguran-usia-15-24-terus-naik-paling-banyak-lulusan-smk)).

Dari sisi mahasiswa, masalahnya terasa seperti ini:

1. **Tidak tahu harus melamar ke mana.** Lowongan tersebar di banyak platform, dan sulit menilai mana yang realistis untuk profilnya.
2. **Tidak tahu posisinya di mata perekrut.** Penilaian diri sering terlalu tinggi atau terlalu rendah, dan penolakan jarang disertai alasan.
3. **Tidak tahu apa yang harus dipelajari.** Kursus dan bootcamp banyak, tapi tidak jelas mana yang benar-benar dibutuhkan untuk posisi yang diinginkan.
4. **Kurang latihan wawancara yang relevan.** Latihan yang ada biasanya umum, bukan untuk posisi dan perusahaan spesifik yang akan dilamar.

Mahasiswa dari kampus dengan pusat karier yang aktif dan jaringan alumni yang kuat punya keuntungan besar. Yang lain harus menebak-nebak sendiri.

## Target pengguna

Pengguna utama adalah mahasiswa semester 4 ke atas dan lulusan baru (0–2 tahun) yang sedang mencari magang atau pekerjaan pertama. Pengguna kedua adalah pusat karier kampus yang ingin memantau dan membantu kesiapan mahasiswanya.

| Persona | Situasi | Yang ia butuhkan |
| --- | --- | --- |
| **Raka, 21, Sistem Informasi semester 6** | Ingin magang sebagai Data Analyst, tapi tidak tahu perusahaan mana yang menerima mahasiswa dengan skill seperti dirinya. Sudah mengirim 15 lamaran, belum ada balasan. | Daftar peluang yang realistis, alasan kenapa belum dipanggil, dan apa yang harus diperbaiki dulu. |
| **Salsa, 23, lulusan Ilmu Komunikasi** | Lulus 4 bulan lalu, tertarik ke marketing atau UI writing, tapi bingung mana yang paling cocok. | Melihat beberapa jalur karier dengan tingkat kecocokan masing-masing, lalu berlatih wawancara untuk posisi pilihannya. |
| **Dimas, 22, Teknik Mesin, kampus swasta di daerah** | Kampusnya tidak punya pusat karier aktif, dan tidak ada alumni di perusahaan incarannya. | Pendampingan setara mentor: peluang yang sesuai, simulasi wawancara, dan proyek untuk memperkuat CV. |
| **Nadia, 20, Akuntansi semester 4** | Belum mau melamar, tapi ingin tahu dari sekarang apa yang dibutuhkan untuk jadi auditor di Big 4. | Peta kesenjangan jangka panjang dan rencana per semester. |
| **Bu Lina, staf pusat karier kampus** | Mengelola ribuan mahasiswa dengan tim kecil. Tidak tahu prodi mana yang paling butuh pembekalan. | Dashboard agregat: kesenjangan kompetensi terbanyak per prodi dan tingkat kesiapan per angkatan. |

## Produk serupa dan pembeda

Setiap bagian dari CareerMirror (portal lowongan, simulasi wawancara, analisis CV) sudah ada secara terpisah. Kekuatan CareerMirror ada pada **satu siklus yang tersambung**: peluang yang ditemukan menentukan wawancara yang dilatih, hasil wawancara menentukan kesenjangan, dan kesenjangan menentukan proyek yang dikerjakan.

| Yang sudah ada | Apa yang dilakukan | Yang belum ada |
| --- | --- | --- |
| [Dealls](https://moge.ai/product/dealls), Glints, Kalibrr | Portal lowongan dengan pencocokan berbasis AI dan mentoring | Tidak mengukur seberapa siap pengguna untuk tiap lowongan, dan tidak ada latihan wawancara yang spesifik |
| [Dibimbing AI Interview, Wawancara.ai, Google Interview Warmup](https://eraspace.com/artikel/post/tips-pakai-ai-untuk-simulasi-interview-kerja-bicara-jadi-lancar) | Simulasi wawancara dengan AI | Berdiri sendiri; tidak tersambung ke lowongan nyata, peta kesenjangan, dan rencana belajar |
| [Jobscan](https://www.jobscan.co/organizations/interview-readiness/) | Mencocokkan CV dengan deskripsi lowongan, latihan wawancara untuk pusat karier | Fokus pasar Amerika Serikat; belum menjangkau magang, program, dan kompetisi lokal |
| [IntervYou (mahasiswa UM)](https://rri.co.id/malang/iptek/2051938/mahasiswa-um-kembangkan-platform-ai-latihan-wawancara-kerja) | Simulasi wawancara + analisis CV | Belum ada pencarian peluang dan rubrik kesiapan yang transparan |

**Enam pembeda CareerMirror:**

1. **Peluang → kesiapan → wawancara dalam satu alur.** Setiap peluang punya skor kesiapan sendiri, dan wawancaranya disimulasikan dari deskripsi lowongan itu.
2. **Berbasis bukti, bukan pengakuan.** Skor dihitung dari CV, portofolio, GitHub, dan hasil wawancara. Setiap poin menunjuk ke buktinya.
3. **Rubrik transparan.** Pengguna tahu persis kenapa skornya 62, dan apa yang membuatnya naik.
4. **Peluangnya lebih dari sekadar lowongan kerja.** Termasuk magang, program pengembangan, kompetisi, beasiswa, dan proyek sukarela yang bisa memperkuat profil.
5. **Rencana yang bisa dikerjakan.** Kesenjangan diubah menjadi proyek portofolio konkret, lalu skornya diukur ulang setelah proyek selesai.
6. **Konteks Indonesia.** Data lowongan lokal, gaji dalam Rupiah, budaya wawancara di Indonesia, dan pusat karier kampus sebagai mitra.

## Konsep inti dan cara kerja

CareerMirror dibangun di atas tiga komponen yang saling terhubung: **Profil Karier** (siapa pengguna), **Peta Kebutuhan Industri** (apa yang dicari perekrut), dan **Mesin Pencocokan** (seberapa jauh jaraknya).

**1. Profil Karier dengan Tingkat Bukti.** Dari CV, portofolio, dan jawaban onboarding, AI menyusun daftar keterampilan pengguna. Setiap keterampilan diberi tingkat bukti, sehingga skor tidak bisa dinaikkan hanya dengan menulis kata kunci di CV.

| Tingkat bukti | Artinya | Contoh |
| --- | --- | --- |
| Diklaim | Hanya disebut di CV | "SQL" tertulis di bagian skills |
| Ada bukti | Didukung proyek, sertifikat, repo, atau pengalaman | Repo GitHub berisi analisis data penjualan memakai SQL |
| Teruji | Berhasil dijelaskan dan diterapkan saat simulasi wawancara | Mampu menjelaskan JOIN dan menulis query sederhana saat ditanya |

**2. Peta Kebutuhan Industri.** Dari kumpulan lowongan nyata, AI mengekstrak keterampilan yang paling sering diminta untuk setiap posisi dan level. Contoh: *"Dari 312 lowongan Junior Data Analyst bulan ini, 81% meminta SQL, 64% Excel lanjutan, 52% Power BI atau Tableau."*

**3. Mesin Pencocokan.** Untuk setiap peluang, mesin menghitung:

- **Syarat wajib:** jurusan, semester atau tahun lulus, lokasi, IPK minimum. Kalau tidak terpenuhi, peluang tidak ditampilkan, atau diberi tanda jelas.
- **Kecocokan keterampilan:** dibobot dengan tingkat bukti (Teruji > Ada bukti > Diklaim).
- **Kecocokan preferensi:** minat, tipe kerja, gaji, dan nilai-nilai yang penting bagi pengguna.

Hasilnya adalah **Skor Kecocokan** (seberapa sesuai peluang ini dengan pengguna) dan **Skor Kesiapan** (seberapa siap pengguna bersaing untuk peluang ini). Keduanya ditampilkan terpisah, karena peluang bisa sangat cocok dengan minat, tapi kesiapannya belum cukup.

**Siklus utamanya:** temukan peluang → lihat skor dan kesenjangan → latih wawancara untuk peluang itu → kerjakan proyek penutup kesenjangan → skor diperbarui → lamar dengan percaya diri.

## Input onboarding

Onboarding dibuat seperti percakapan singkat sekitar 5 menit, bukan formulir panjang. CV yang diunggah otomatis mengisi sebagian besar kolom, lalu pengguna cukup mengoreksi dan melengkapi.

| Input | Contoh | Dipakai untuk | Sifat |
| --- | --- | --- | --- |
| **CV** (PDF) | CV satu halaman | Bahan awal Profil Karier: pendidikan, pengalaman, keterampilan | Wajib |
| **Status akademik** | Kampus, jurusan, semester atau tahun lulus, IPK | Menyaring peluang berdasarkan syarat wajib | Wajib (IPK opsional) |
| **Minat dan posisi tujuan** | "Data Analyst", "UI/UX", atau "belum tahu" | Arah pencarian peluang. Kalau "belum tahu", masuk Mode Jelajah | Wajib |
| **Tipe peluang** | Magang, kerja penuh waktu, paruh waktu, freelance, management trainee, kompetisi, beasiswa, relawan | Jenis peluang yang dicari | Wajib |
| **Preferensi kerja** | Kota, remote/hybrid/onsite, bersedia pindah kota, gaji atau uang saku minimum | Menyaring dan mengurutkan peluang | Wajib |
| **Ketersediaan waktu** | Mulai kapan, berapa jam per minggu, bisa sambil kuliah atau tidak | Penting untuk magang dan kerja paruh waktu | Wajib |
| **Tautan bukti** | Portofolio, GitHub, LinkedIn, Behance, sertifikat | Menaikkan tingkat bukti keterampilan | Opsional, sangat disarankan |
| **Pengalaman non-formal** | Organisasi, kepanitiaan, proyek kuliah, lomba, usaha kecil | Sering tidak tertulis di CV, padahal menunjukkan soft skill | Opsional |
| **Kemampuan bahasa** | Inggris (skor TOEFL/IELTS kalau ada), bahasa lain | Syarat banyak lowongan dan program | Opsional |
| **Nilai dan gaya kerja** | 5 pertanyaan cepat: startup atau korporat, stabilitas atau belajar cepat, kerja sendiri atau tim | Mengurutkan peluang yang paling cocok dengan kepribadian | Opsional |
| **Target waktu** | "Mau dapat magang 2 bulan lagi" atau "persiapan untuk 1 tahun lagi" | Menentukan prioritas: lamar sekarang, atau persiapan dulu | Opsional |
| **Kebutuhan akomodasi** | Disabilitas, kebutuhan khusus, atau kondisi tertentu | Menampilkan peluang dan perusahaan yang inklusif | Opsional, privat |

**Mode Jelajah (untuk yang belum tahu minat):** AI mengajukan 10 pertanyaan tentang aktivitas yang disukai, mata kuliah favorit, dan proyek yang paling dinikmati. Lalu AI menyarankan 3 jalur karier, lengkap dengan alasannya dan skor kecocokan awal. Pengguna bisa memilih satu atau lebih jalur untuk mulai dicarikan peluang.

## Fitur

Fitur dibagi tiga kelompok. **Inti** membentuk satu siklus utuh dari CV sampai skor kesiapan. **Unggulan** membuat CareerMirror lebih dari sekadar alat latihan. **Lanjutan** untuk setelah hackathon.

### Inti (MVP)

| Fitur | Apa yang dilakukan | Prioritas |
| --- | --- | --- |
| **Profil Karier Otomatis** | Membaca CV dan tautan bukti, lalu menyusun daftar keterampilan lengkap dengan tingkat buktinya (Diklaim, Ada bukti, Teruji). Pengguna bisa mengoreksi. | MVP |
| **Radar Peluang** | Daftar peluang yang sesuai profil, masing-masing dengan Skor Kecocokan, Skor Kesiapan, alasan singkat, dan tenggat. Dikelompokkan menjadi "Siap dilamar", "Hampir siap", dan "Perlu persiapan". | MVP |
| **Detail Peluang** | Daftar kebutuhan lowongan dibandingkan dengan profil pengguna, dengan tanda hijau (terpenuhi), kuning (sebagian), dan merah (belum). Juga menunjukkan hal yang bisa membuat pengguna menonjol. | MVP |
| **Simulasi Wawancara Spesifik** | Wawancara yang dibuat dari deskripsi lowongan dan profil perusahaan yang dipilih. Ada dua tahap: HR (motivasi, perilaku, kecocokan budaya) dan User (teknis sesuai lowongan). Pewawancara menanyakan lanjutan kalau jawaban kurang dalam. Lewat suara atau teks. | MVP (momen wow demo) |
| **Analisis Jawaban dan Komunikasi** | Setiap jawaban dinilai dari struktur (misalnya metode STAR), relevansi dengan lowongan, bukti konkret, dan ketepatan teknis. Cara bicara juga dianalisis: kata pengisi, durasi, dan kejelasan. Contoh jawaban yang lebih kuat disusun dari pengalaman pengguna sendiri. | MVP |
| **Peta Kesenjangan** | Keterampilan yang kurang, per peluang dan untuk posisi tujuan secara umum, diurutkan dari yang paling berdampak. | MVP |
| **Career Readiness Score** | Skor kesiapan 0–100 dengan rubrik yang transparan (lihat bagian berikutnya). | MVP |
| **Rekomendasi Proyek** | 1–3 proyek portofolio berdurasi 1–2 minggu yang langsung menutup kesenjangan terbesar, lengkap dengan brief, contoh data, dan hasil akhir yang diharapkan. Setelah pengguna mengirim tautan hasilnya, AI meninjaunya dan tingkat bukti naik. | MVP |

### Unggulan

| Fitur | Apa yang dilakukan | Kenapa keren | Prioritas |
| --- | --- | --- | --- |
| **Kacamata Perekrut** | Simulasi cara perekrut membaca CV dalam beberapa detik pertama: apa yang terlihat, apa yang terlewat, dan kata kunci yang hilang dibandingkan lowongan. | Menjawab pertanyaan "kenapa aku belum dipanggil?" dengan jujur. | MVP |
| **Paket Lamaran** | Saran penyesuaian CV dan draf cover letter untuk lowongan tertentu, disusun hanya dari pengalaman nyata pengguna. | Menghemat waktu tanpa mengarang. | Kalau sempat |
| **Pelacak Lamaran** | Papan status lamaran (disimpan, dilamar, wawancara, diterima, ditolak), dengan pengingat tenggat dan follow-up. Setelah ditolak, ada refleksi singkat dan saran peluang alternatif. | Proses melamar terasa terarah, bukan menebak-nebak. | Kalau sempat |
| **Proyek Nyata untuk Komunitas** | Sebagian rekomendasi proyek berasal dari kebutuhan nyata UMKM, komunitas, atau organisasi nirlaba. Contohnya membuat dashboard penjualan untuk UMKM lokal. | Pengguna mendapat portofolio sungguhan, komunitas mendapat bantuan. | Setelah MVP |
| **Rencana Per Semester** | Untuk mahasiswa semester awal: mata kuliah pilihan, organisasi, proyek, dan magang yang sebaiknya diambil setiap semester menuju posisi tujuan. | Persiapan dimulai jauh sebelum lulus. | Setelah MVP |

### Lanjutan (setelah hackathon)

| Fitur | Apa yang dilakukan | Prioritas |
| --- | --- | --- |
| **Dashboard Pusat Karier** | Ringkasan agregat dan anonim per prodi dan angkatan: kesenjangan terbanyak, tingkat kesiapan, dan peluang yang paling diminati. | Jangka panjang (B2B) |
| **Sehari Jadi…** | Simulasi hari kerja dengan rekan kerja AI, untuk merasakan pekerjaannya sebelum melamar. | Jangka panjang |
| **Mode Video** | Analisis kontak mata, ekspresi, dan postur saat wawancara lewat kamera. | Jangka panjang |
| **Latihan Tes Rekrutmen** | Simulasi psikotes, tes logika, dan tes teknis yang umum di Indonesia. | Jangka panjang |
| **Notifikasi Peluang** | Pemberitahuan lewat WhatsApp atau email saat ada peluang baru dengan skor kecocokan tinggi. | Jangka panjang |
| **Sambung ke Alumni** | Menghubungkan pengguna dengan alumni kampusnya yang bekerja di posisi tujuan. | Jangka panjang |

## Career Readiness Score

Skor kesiapan (0–100) dihitung dari lima komponen dengan bobot yang terlihat oleh pengguna. Setiap poin menunjuk ke buktinya, dan selalu ada jawaban untuk pertanyaan "apa yang paling cepat menaikkan skorku?".

```latex
\text{Skor} = \sum_{i=1}^{5} w_i \times s_i \qquad (s_i \text{ dalam skala } 0\text{--}100,\ \textstyle\sum w_i = 1)
```

Contoh untuk Raka, mahasiswa Sistem Informasi yang menargetkan magang Junior Data Analyst:

| Komponen | Bobot | Cara menilai | Nilai Raka | Cara menaikkan |
| --- | --- | --- | --- | --- |
| **Keterampilan teknis** | 35% | Kecocokan dengan keterampilan yang paling sering diminta lowongan, dikali tingkat bukti (Teruji = 1,0; Ada bukti = 0,7; Diklaim = 0,3) | 58 | Buktikan Power BI lewat satu proyek dashboard |
| **Performa wawancara** | 25% | Rata-rata rubrik per jawaban: relevansi, struktur, bukti konkret, ketepatan teknis (masing-masing 1–4) | 64 | Latih pertanyaan perilaku dengan metode STAR |
| **Pengalaman dan portofolio** | 20% | Jumlah dan relevansi proyek, magang, organisasi, dan lomba | 55 | Tambahkan proyek analisis data dengan data nyata |
| **Komunikasi** | 10% | Kejelasan, keringkasan, kata pengisi, dan durasi jawaban | 70 | Kurangi jawaban yang lebih dari 2 menit |
| **Kualitas dokumen** | 10% | Struktur CV, cakupan kata kunci lowongan, pencapaian yang terukur | 72 | Ubah deskripsi pengalaman menjadi pencapaian yang terukur |
| **Total** | 100% |  | **62** (Hampir siap) |  |

**Kategori skor:** 0–49 *Perlu persiapan*, 50–74 *Hampir siap*, 75–100 *Siap dilamar*.

**Dua jenis skor:**

- **Skor per peluang:** dihitung terhadap kebutuhan satu lowongan tertentu. Dipakai di Radar Peluang.
- **Skor posisi:** dihitung terhadap kebutuhan umum suatu posisi dari seluruh data lowongan. Dipakai untuk memantau perkembangan dari waktu ke waktu.

**Prinsip rubrik:**

- Bobot di atas adalah asumsi awal. Bobot perlu divalidasi dengan praktisi HR, dan bisa berbeda per jenis posisi (misalnya portofolio lebih berat untuk desainer).
- Skor bukan prediksi diterima atau ditolak. Skor menunjukkan seberapa lengkap persiapan dibandingkan kebutuhan yang umum diminta.
- Pengguna selalu bisa melihat rincian setiap komponen sampai ke bukti yang dipakai, dan bisa mengajukan koreksi kalau ada yang keliru.

## Alur pengguna

Baris atas adalah alur menemukan: dari CV sampai satu peluang yang dipilih. Baris bawah adalah alur mempersiapkan: wawancara, skor, dan proyek, yang berulang sampai pengguna siap melamar.

&#91;embedded content: alur pengguna · 8 langkah, 1 putaran latihan\]

Setiap proyek yang diselesaikan menambah bukti di Profil Karier. Skor untuk semua peluang ikut diperbarui, sehingga peluang yang tadinya "Perlu persiapan" bisa naik menjadi "Siap dilamar".

## Rencana teknologi dan sumber data peluang

Prinsip teknisnya sama dengan prinsip produknya: **AI membaca dan menilai, kode menghitung**. LLM mengekstrak keterampilan dari CV dan lowongan, lalu memberi label pada jawaban wawancara. Skor kecocokan dan skor kesiapan dihitung dengan rumus yang transparan.

| Lapis | Pilihan utama | Alternatif | Fungsi |
| --- | --- | --- | --- |
| Frontend | Next.js + Tailwind | React Native | Onboarding, Radar Peluang, ruang wawancara, rapor |
| Backend | FastAPI (Python) | Next.js API routes | Parsing, pencocokan, orkestrasi wawancara |
| Membaca CV dan lowongan | LLM dengan output JSON terstruktur | Parser CV open-source + LLM | Mengekstrak pendidikan, pengalaman, keterampilan, dan syarat lowongan |
| Normalisasi keterampilan | Daftar keterampilan baku (misalnya taksonomi ESCO, ditambah sinonim bahasa Indonesia buatan tim) | Pengelompokan dengan embedding | Menyamakan "Ms. Excel", "Excel lanjutan", dan "spreadsheet" |
| Pencocokan peluang | Filter aturan (syarat wajib) + embedding similarity (pgvector) + rumus skor | Hanya LLM (kurang konsisten) | Radar Peluang dengan skor yang bisa dijelaskan |
| Wawancara | LLM dengan persona HR dan User, dibuat dari deskripsi lowongan | — | Pertanyaan spesifik dan pertanyaan lanjutan |
| Penilaian jawaban | LLM sebagai penilai dengan rubrik + contoh berlabel (few-shot) | — | Nilai per jawaban yang konsisten |
| Suara | STT: Whisper atau Deepgram. TTS: ElevenLabs atau Google Cloud TTS | Teks saja | Wawancara lewat suara, analisis cara bicara |
| Database | Supabase (Postgres + pgvector + auth) | Firebase + Pinecone | Profil, peluang, sesi, skor |
| Deploy | Vercel + Railway | Render | Link demo untuk juri |

**Sumber data peluang:**

- **Untuk hackathon:** kumpulkan 200–500 peluang nyata dari sumber publik secara manual atau semi-otomatis, untuk 3–4 posisi tujuan saja (misalnya Data Analyst, UI/UX, Digital Marketing). Tambahkan juga beberapa program magang, kompetisi, dan beasiswa. Simpan tanggal pengambilan dan tautan aslinya. Patuhi ketentuan penggunaan setiap situs.
- **Setelah hackathon:** kerja sama resmi atau API dengan portal lowongan, portal ketenagakerjaan pemerintah, pusat karier kampus, dan halaman karier perusahaan. Perusahaan dan penyelenggara program juga bisa memasang peluang langsung.

**Menjaga kualitas data:** peluang yang sudah lewat tenggat otomatis disembunyikan. Lowongan dengan ciri penipuan (meminta biaya, kontak pribadi saja, gaji tidak wajar) diberi tanda atau tidak ditampilkan.

## Prinsip human-centered, etika, privasi, dan keadilan

CareerMirror menyentuh hal yang sensitif: harga diri, masa depan, dan data pribadi. Aturan di bawah adalah bagian dari produk.

- **Jujur tapi tidak mematahkan semangat.** Skor rendah selalu disertai langkah konkret berikutnya dan perkiraan waktunya. Bahasanya "belum siap", bukan "tidak layak".
- **Tidak mengarang pengalaman.** Paket Lamaran dan contoh jawaban hanya disusun dari pengalaman yang benar-benar dimiliki pengguna. AI menolak menambahkan pengalaman, sertifikat, atau angka yang tidak ada.
- **Skor bukan vonis.** Skor tidak memprediksi diterima atau tidak, dan tidak pernah dibagikan ke perusahaan tanpa persetujuan eksplisit pengguna.
- **Adil untuk semua latar belakang.** Nama kampus, asal daerah, jenis kelamin, agama, usia, dan foto tidak dipakai dalam perhitungan skor. Model penilaian diuji secara berkala untuk memastikan tidak ada bias terhadap kelompok tertentu.
- **Peluang yang sehat.** Lowongan dengan syarat diskriminatif (misalnya "berpenampilan menarik" atau batas usia yang tidak relevan) diberi catatan. Lowongan dengan ciri penipuan disembunyikan.
- **Data milik pengguna.** CV, rekaman suara, dan hasil wawancara tidak dipakai untuk melatih model tanpa izin. Rekaman suara dihapus setelah dianalisis. Ada tombol "hapus semua dataku". Dashboard pusat karier hanya menampilkan data agregat dan anonim.
- **Menjaga kesehatan mental.** Proses mencari kerja bisa melelahkan. Setelah beberapa kali ditolak, Pelacak Lamaran menyarankan jeda dan menunjukkan kemajuan yang sudah dicapai, bukan hanya kegagalannya.
- **Akses untuk semua.** Fitur inti gratis untuk mahasiswa, bisa dipakai di HP dengan koneksi terbatas, dan mode teks tersedia bagi yang tidak nyaman berbicara.

## Metrik keberhasilan

Saat hackathon, yang perlu dibuktikan ada tiga: peluang yang disarankan memang relevan, simulasi wawancaranya terasa realistis, dan skornya masuk akal di mata praktisi.

**Saat hackathon (uji coba ke 10–20 mahasiswa tingkat akhir dengan CV mereka sendiri):**

- **Relevansi peluang:** persentase dari 10 peluang teratas yang dinilai pengguna "layak aku lamar" (target ≥ 70%).
- **Realisme wawancara:** skor 1–5 dari pengguna untuk pertanyaan "seberapa mirip dengan wawancara sungguhan?".
- **Kewajaran skor:** 1–2 praktisi HR atau staf pusat karier menilai 5 profil secara manual, lalu dibandingkan dengan skor CareerMirror.
- **Kejelasan langkah:** persentase pengguna yang bisa menyebutkan satu hal konkret yang akan ia kerjakan minggu ini setelah memakai aplikasi.

**Setelah peluncuran:**

- Kenaikan rata-rata Career Readiness Score setelah 30 hari
- Persentase proyek rekomendasi yang diselesaikan
- Rasio lamaran yang berlanjut ke tahap wawancara, dibandingkan sebelum memakai CareerMirror (dilaporkan pengguna lewat Pelacak Lamaran)
- Waktu sampai mendapat magang atau pekerjaan pertama
- Jumlah kampus yang memakai Dashboard Pusat Karier

## Scope hackathon dan skenario demo

Yang wajib jadi adalah satu siklus utuh: unggah CV, Radar Peluang, pilih satu peluang, simulasi wawancara spesifik, lalu skor dan rencana. Batasi ke 3–4 posisi tujuan, supaya data peluang dan kualitas pertanyaannya terjaga.

- **Wajib:** Profil Karier Otomatis, Radar Peluang (dengan Skor Kecocokan dan Skor Kesiapan), Detail Peluang, Simulasi Wawancara Spesifik (suara atau teks), Analisis Jawaban, Peta Kesenjangan, Career Readiness Score, Rekomendasi Proyek, Kacamata Perekrut.
- **Kalau sempat:** Mode Jelajah, Paket Lamaran, Pelacak Lamaran, analisis cara bicara.
- **Tidak dikerjakan:** Dashboard Pusat Karier, Mode Video, Latihan Tes Rekrutmen, notifikasi, Sambung ke Alumni.

**Pembagian tim (contoh 4 orang):**

| Peran | Tanggung jawab |
| --- | --- |
| Frontend | Onboarding, Radar Peluang, Detail Peluang, ruang wawancara, rapor skor |
| Backend + AI | Parsing CV dan lowongan, normalisasi keterampilan, pencocokan, persona wawancara, penilaian |
| Data + rubrik | Mengumpulkan 200–500 peluang, menyusun daftar keterampilan baku, menulis rubrik dan contoh berlabel |
| Riset + pitch | Uji coba ke mahasiswa, validasi ke praktisi HR atau pusat karier, deck, video cadangan |

**Skenario demo 3 menit:**

1. **Hook (20 detik):** "Rata-rata lulusan perguruan tinggi di Indonesia butuh hampir 20 bulan untuk mendapat pekerjaan. Salah satu penyebabnya: mereka tidak tahu apa yang kurang."
2. **Unggah CV (20 detik):** pakai CV asli salah satu anggota tim. Profil Karier muncul, lengkap dengan tingkat bukti setiap keterampilan.
3. **Radar Peluang (30 detik):** muncul 10 peluang dengan dua skor. Tunjukkan satu yang "Siap dilamar" dan satu yang "Perlu persiapan", beserta alasannya.
4. **Wawancara (60 detik):** pilih satu lowongan. Pewawancara User bertanya hal teknis dari deskripsi lowongannya, lalu mengejar jawaban yang kurang dalam. Ini momen wow.
5. **Skor dan rencana (30 detik):** skor kesiapan 62 dengan rincian per komponen, peta kesenjangan, dan satu proyek dashboard 1 minggu yang akan menaikkannya.
6. **Penutup (20 detik):** ringkas siklusnya, lalu tunjukkan visi Dashboard Pusat Karier untuk kampus.

**Cadangan:** rekam video demo lengkap, dan siapkan profil dan hasil wawancara yang sudah tersimpan kalau API lambat.

## Model bisnis dan pengembangan jangka panjang

Model yang paling sehat adalah **gratis untuk fitur inti mahasiswa**, dengan pendapatan dari kampus dan perusahaan yang mendapat manfaat dari lulusan yang lebih siap. Perusahaan boleh memasang peluang, tapi tidak bisa membeli akses ke skor pengguna.

| Segmen | Yang ditawarkan | Kenapa mereka mau membayar |
| --- | --- | --- |
| Mahasiswa | Gratis: profil, Radar Peluang, simulasi wawancara dengan batas sesi. Premium opsional: sesi tanpa batas, Mode Video, Paket Lamaran | Akses tetap terbuka; premium untuk yang butuh latihan intensif |
| Kampus dan pusat karier | Lisensi institusi: akses penuh untuk semua mahasiswa + Dashboard Pusat Karier | Meningkatkan keterserapan lulusan dan bahan evaluasi kurikulum |
| Perusahaan | Memasang peluang dan program magang; menjangkau kandidat yang memilih untuk ditemukan (opt-in) | Kandidat yang lebih siap dan lebih cocok, proses rekrutmen lebih efisien |
| Penyelenggara program, kompetisi, dan beasiswa | Promosi peluang kepada pengguna yang paling cocok | Pendaftar yang lebih relevan |

**Tahapan pengembangan:**

1. **Hackathon:** 3–4 posisi tujuan, 200–500 peluang, satu siklus utuh dari CV sampai rencana proyek.
2. **Pilot kampus (3 bulan):** satu pusat karier kampus, 100–300 mahasiswa. Validasi rubrik bersama praktisi HR, tambah posisi tujuan.
3. **Rilis publik:** Mode Jelajah, Pelacak Lamaran, Paket Lamaran, notifikasi peluang, dan kerja sama data dengan portal lowongan.
4. **Skala institusi:** Dashboard Pusat Karier untuk banyak kampus, Proyek Nyata untuk Komunitas, Sambung ke Alumni, dan simulasi hari kerja.

## Pertanyaan terbuka untuk diskusi

Bagian ini sengaja dibiarkan terbuka untuk dibahas bersama tim.

- [ ] **Posisi tujuan untuk demo:** 3–4 posisi mana yang dipilih? Sebaiknya yang paling banyak diminati mahasiswa di kampus kita dan datanya mudah dikumpulkan.
- [ ] **Fokus utama pitch:** "menemukan peluang" atau "mengukur kesiapan"? Keduanya ada, tapi pitch 3 menit butuh satu cerita utama.
- [ ] **Jenis peluang:** semua jenis (kerja, magang, kompetisi, beasiswa), atau magang dan kerja saja di versi awal?
- [ ] **Bobot rubrik:** apakah bobot awal (35/25/20/10/10) masuk akal? Siapa praktisi HR yang bisa diajak memvalidasi?
- [ ] **Suara atau teks untuk wawancara utama?** Suara lebih realistis, teks lebih stabil saat demo.
- [ ] **Sumber data peluang:** dikumpulkan manual, semi-otomatis, atau lewat kerja sama? Perlu dicek ketentuan penggunaan setiap sumber.
- [ ] **Hubungan dengan perusahaan:** apakah perusahaan boleh melihat profil kandidat yang memilih untuk ditemukan? Kalau iya, bagaimana menjaga agar skor tidak jadi alat diskriminasi?

## Sumber

- [BPS Ungkap 1 Juta Lulusan S1-S3 di RI Masih Nganggur](https://finance.detik.com/berita-ekonomi-bisnis/d-8605483/bps-ungkap-1-juta-lulusan-s1-s3-di-ri-masih-nganggur) — detikFinance
- [Tanoto Foundation: Employability Mahasiswa Harus Diasah Sejak Menempuh Kuliah](https://lestari.kompas.com/read/2026/07/28/143621786/tanoto-foundation-employability-mahasiswa-harus-diasah-sejak-menempuh) — Kompas
- [Tingkat Pengangguran Usia 15-24 Terus Naik, Paling Banyak Lulusan SMK](https://cnbcindonesia.com/news/20260806131950-4-757114/tingkat-pengangguran-usia-15-24-terus-naik-paling-banyak-lulusan-smk) — CNBC Indonesia
- [Dealls](https://moge.ai/product/dealls) — moge.ai
- [Tips Pakai AI untuk Simulasi Interview Kerja](https://eraspace.com/artikel/post/tips-pakai-ai-untuk-simulasi-interview-kerja-bicara-jadi-lancar) — Eraspace
- [Interview Readiness](https://www.jobscan.co/organizations/interview-readiness/) — Jobscan
- [Mahasiswa UM Kembangkan Platform AI Latihan Wawancara Kerja](https://rri.co.id/malang/iptek/2051938/mahasiswa-um-kembangkan-platform-ai-latihan-wawancara-kerja) — RRI
