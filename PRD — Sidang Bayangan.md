# PRD — Sidang Bayangan

Nov 23, 2026 · @Jewan Enjoyer

## Ringkasan

**Sidang Bayangan** adalah tempat gladi resik sidang skripsi bersama panel dosen penguji AI. Para penguji ini sudah membaca skripsimu sampai halaman terakhir. Mereka bertanya lewat suara, menyela jawaban yang lemah, lalu memberi rapor tentang bagian skripsimu yang paling rawan diserang.

**One-liner:** *Rasakan sidang skripsimu sebelum hari H, supaya hari H terasa seperti sidang yang kedua.*

**Konsep inti:** AI membedah skripsi untuk menemukan titik lemahnya, misalnya metodologi, data yang tidak konsisten, atau kesimpulan yang tidak menjawab rumusan masalah. Lalu AI memerankan tiga penguji dengan karakter berbeda. Pertanyaan mereka bukan pertanyaan umum, tapi pertanyaan spesifik yang hanya bisa muncul dari skripsimu sendiri.

**Subtema Hackvidia:** utama *AI for Learning & Self-Growth*. Pendukungnya *AI for Health & Wellbeing* (mengurangi kecemasan menjelang sidang) dan *AI for Inclusive Access* (memberi akses latihan yang sama bagi mahasiswa yang pembimbingnya sibuk atau kampusnya minim pendampingan).

**Prinsip desain:** AI tidak pernah menulis atau memperbaiki skripsi untuk mahasiswa. AI hanya *bertanya dan menguji*. Mahasiswa tetap harus berpikir dan menjawab sendiri.

## Masalah

Sidang skripsi menentukan kelulusan, tapi mahasiswa hampir tidak pernah bisa berlatih menghadapinya dalam kondisi yang mirip aslinya.

- **Kecemasannya nyata.** Beberapa penelitian di Indonesia menemukan mahasiswa yang menyusun skripsi cenderung mengalami kecemasan tingkat sedang hingga tinggi ([Unesa, Jurnal Character](https://ejournal.unesa.ac.id/index.php/character/article/view/62208)).
- **Latihan yang ada tidak realistis.** Biasanya mahasiswa hanya membaca ulang skripsi, menghafal daftar "pertanyaan sidang yang sering muncul" dari internet, atau latihan dengan teman yang belum membaca skripsinya.
- **Pembimbing tidak punya waktu.** Satu dosen bisa membimbing banyak mahasiswa sekaligus, jadi gladi sidang satu per satu hampir mustahil.
- **Kelemahan ditemukan terlambat.** Inkonsistensi data antar bab atau metode yang kurang tepat sering baru ketahuan *saat* sidang, ketika sudah terlambat untuk disiapkan.

Akibatnya, banyak mahasiswa masuk ruang sidang dengan rasa takut terhadap hal yang tidak diketahui, bukan karena skripsinya buruk.

## Target pengguna

Pengguna utama adalah mahasiswa S1 tingkat akhir yang akan menghadapi seminar proposal atau sidang skripsi. Pengguna kedua adalah mahasiswa S2 (sidang tesis) dan dosen pembimbing yang ingin memantau kesiapan mahasiswanya.

| Persona | Situasi | Yang ia butuhkan |
| --- | --- | --- |
| **Nadia, 22, Manajemen** | Skripsi kuantitatif dengan SPSS. Paham hasilnya, tapi takut ditanya "kenapa pakai regresi berganda, bukan SEM?" | Latihan menjawab pertanyaan metodologi yang paling ia takutkan. |
| **Bayu, 23, Teknik Informatika** | Membuat aplikasi untuk skripsi. Jago coding, tapi gugup bicara di depan dosen dan sering menjawab berputar-putar. | Latihan bicara singkat dan terstruktur, plus umpan balik soal cara menjawab. |
| **Laras, 24, Pendidikan, kampus swasta di daerah** | Pembimbingnya mengajar di dua kampus dan jarang bisa ditemui. Tidak ada kakak tingkat yang bisa ditanya. | Pengganti gladi sidang yang tidak bisa ia dapatkan dari pembimbing. |
| **Pak Hendra, dosen pembimbing** | Membimbing 12 mahasiswa sekaligus. Tidak sempat menggelar gladi sidang untuk semuanya. | Laporan singkat: mahasiswa mana yang sudah siap, dan siapa yang perlu dibantu di bagian apa. |

## Produk serupa dan pembeda

Simulasi sidang berbasis AI sudah pernah dibuat, jadi kita tidak bisa menjual "AI yang bertanya soal skripsimu" sebagai hal baru. Pembeda kita ada pada **panel multi-penguji yang hidup, pembedahan kelemahan skripsi sebelum sidang, dan siklus latihan yang terarah**.

| Yang sudah ada | Apa yang dilakukan | Yang belum ada |
| --- | --- | --- |
| [Tugas akhir Telkom University](https://openlibrary.telkomuniversity.ac.id/pustaka/files/236723/abstraksi/pengembangan-simulasi-ujian-skripsi-berbasis-large-language-model-dan-retrieval-augmented-generation-dalam-bentuk-buku-karya-ilmiah.pdf) | Simulasi sidang berbasis LLM + RAG dari dokumen skripsi, dengan text-to-speech | Prototipe riset; satu penguji; belum ada analisis kelemahan dan siklus latihan |
| [SuperviseAI (Devpost)](https://devpost.com/software/superviseai) | Mock viva dari draf tesis, suara atau teks, skor kesiapan, dashboard pembimbing | Multi-penguji masih rencana; konteks luar negeri (viva), bukan sidang skripsi Indonesia |
| [Viva Mentor, University of Kent](https://blogs.kent.ac.uk/aiteam/?p=13) | Custom GPT untuk latihan viva mahasiswa doktoral | Teks saja, satu penguji, untuk S3 |
| ChatGPT/Gemini + prompt "jadilah dosen penguji" | Banyak artikel kampus yang mengajarkan cara ini ([contoh](https://masoemuniversity.ac.id/artikel/rekomendasi-cara-memakai-ai-buat-latihan-simulasi-tanya-jawab-sidang/)) | Harus menyusun prompt sendiri; tidak ada suara, panel, rapor, atau pelacakan perkembangan |

**Lima pembeda Sidang Bayangan:**

1. **Panel tiga penguji dengan karakter berbeda** yang bergantian bertanya, saling menyambung, dan menyela. Ini yang membuat suasananya terasa seperti sidang sungguhan.
2. **Peta Rawan sebelum sidang:** AI memeriksa konsistensi antar bab (rumusan masalah vs kesimpulan, angka di tabel vs teks, metode vs jumlah sampel) dan menunjukkan halamannya.
3. **Tingkat kesulitan bertahap**, dari penguji ramah sampai mode "dosen killer", supaya mental terlatih sedikit demi sedikit.
4. **Siklus latihan terarah:** sesi berikutnya fokus ke bagian yang kemarin jawabannya paling lemah.
5. **Dibuat untuk sidang skripsi Indonesia:** struktur BAB I–V, istilah dan kebiasaan sidang lokal, serta pedoman skripsi kampus masing-masing yang bisa diunggah.

## Konsep inti dan cara kerja

Sistemnya bekerja dalam tiga tahap: **membedah** skripsi, **menguji** lewat panel, lalu **melatih ulang** bagian yang lemah.

1. **Membedah skripsi.** PDF dipecah per bab, lalu AI menyusun "peta argumen": rumusan masalah, tujuan, hipotesis, metode, sampel, temuan utama, dan kesimpulan. Peta ini dipakai untuk mencari celah, seperti rumusan masalah yang tidak terjawab di kesimpulan, angka yang berbeda antar bab, metode yang kurang cocok dengan data, atau referensi yang sudah terlalu lama.
2. **Menguji lewat panel.** Tiga penguji AI membaca peta argumen dan Peta Rawan, lalu membagi "jatah serangan" sesuai perannya. Mereka bertanya lewat suara dan mendengarkan jawaban. Kalau jawabannya berputar-putar atau menghindar, mereka mengejar dengan pertanyaan lanjutan.
3. **Melatih ulang.** Setiap jawaban dinilai dengan rubrik yang transparan. Bagian yang lemah masuk antrean latihan berikutnya, sampai mahasiswa bisa menjawabnya dengan tenang.

**Panel penguji:**

| Penguji | Karakter | Fokus serangan | Contoh pertanyaan |
| --- | --- | --- | --- |
| **Ketua Sidang** | Tenang dan berwibawa, membuka dan menutup sesi | Kontribusi, kebaruan, dan manfaat penelitian | "Kalau penelitian ini tidak pernah dilakukan, apa yang hilang?" |
| **Penguji Metodologi** | Tegas, sering memotong, cenderung "killer" | Desain penelitian, sampel, instrumen, analisis statistik | "Sampel 87 orang dengan purposive sampling. Bagaimana Anda bisa menggeneralisasi hasilnya?" |
| **Penguji Substansi** | Teliti, membaca sampai lampiran | Konsistensi data, teori, dan kesimpulan | "Di halaman 54 nilai R²-nya 0,62, tapi di abstrak 0,65. Yang benar yang mana?" |

**Tiga tingkat kesulitan:** *Bersahabat* (pertanyaan dasar, penguji sabar), *Standar* (seperti sidang pada umumnya), dan *Killer* (menyela, menekan, mengejar setiap jawaban yang lemah). Mahasiswa disarankan naik tingkat secara bertahap.

**Batas yang dijaga:** penguji AI hanya boleh bertanya tentang isi skripsi dan bidang ilmunya. Ia tidak memberi jawaban yang "benar" selama sesi. Jawaban yang lebih baik hanya ditunjukkan di rapor setelah sesi, sebagai bahan belajar.

## Fitur

MVP hackathon terdiri dari lima fitur yang membentuk satu alur utuh, dari unggah skripsi sampai rapor. Fitur lainnya untuk pengembangan berikutnya.

| Fitur | Apa yang dilakukan | Prioritas |
| --- | --- | --- |
| **Bedah Skripsi** | Unggah PDF. AI membaca seluruh bab dan menyusun peta argumen (rumusan masalah, metode, temuan, kesimpulan) yang bisa dicek mahasiswa. | MVP |
| **Peta Rawan** | Daftar titik lemah skripsi, diurutkan dari yang paling berisiko, lengkap dengan nomor halaman dan alasannya. Contoh: "Rumusan masalah 3 tidak dijawab di Bab V." | MVP |
| **Ruang Sidang** | Sesi tanya jawab lewat suara dengan panel tiga penguji AI. Ada avatar sederhana tiap penguji, indikator siapa yang bicara, dan timer sidang. | MVP (inti demo) |
| **Tingkat Kesulitan** | Pilihan Bersahabat, Standar, atau Killer. Mengatur seberapa sering penguji menyela dan seberapa dalam mereka mengejar jawaban. | MVP |
| **Rapor Sidang** | Nilai tiap jawaban berdasarkan rubrik (tepat sasaran, berbasis data, mengakui keterbatasan, ringkas). Juga ada catatan cara bicara (jumlah "eee", kecepatan, durasi), dan contoh jawaban yang lebih kuat. | MVP |
| **Latihan Ulang Fokus** | Sesi singkat 5 menit yang hanya menguji bagian yang kemarin paling lemah. | Setelah MVP (versi sederhana bisa ikut demo) |
| **Mode Presentasi** | Mahasiswa presentasi dengan slide-nya sendiri. AI menilai alur presentasi, ketepatan waktu, dan menjadikan slide sebagai bahan pertanyaan. | Setelah MVP |
| **Pedoman Kampus** | Unggah pedoman skripsi dan rubrik penilaian prodi, supaya pertanyaan dan penilaian menyesuaikan standar kampus. | Setelah MVP |
| **Seminar Proposal dan Tesis** | Mode untuk seminar proposal (fokus ke Bab I–III dan rencana penelitian) dan untuk sidang tesis S2. | Jangka panjang |
| **Dashboard Pembimbing** | Dosen melihat ringkasan kesiapan mahasiswa bimbingannya, dengan izin mahasiswa. | Jangka panjang |
| **Sidang Berbahasa Inggris** | Untuk program internasional atau mahasiswa yang ingin melatih kemampuan akademik dalam bahasa Inggris. | Jangka panjang |

## Alur pengguna

Sesi pertama berjalan dari kiri ke kanan, dari unggah skripsi sampai rapor. Setelah itu, mahasiswa masuk ke putaran latihan ulang sampai siap menghadapi sidang sungguhan.

&#91;embedded content: alur pengguna · 5 langkah, 2 putaran\]

Di dalam Ruang Sidang ada putaran kecil: agen moderator memutuskan apakah penguji mengejar jawaban, menyerahkan giliran ke penguji lain, atau menutup sidang.

## Rencana teknologi

Semuanya memakai layanan AI siap pakai, jadi tidak perlu melatih model sendiri. Tantangan teknis terbesar ada di dua hal: **percakapan suara yang responsif** dan **pengaturan giliran tiga penguji**.

| Lapis | Pilihan utama | Alternatif | Fungsi |
| --- | --- | --- | --- |
| Frontend | Next.js + Tailwind | React + Vite | Halaman unggah, Peta Rawan, ruang sidang, rapor |
| Backend | FastAPI (Python) | Next.js API routes | Mengolah PDF, mengatur sesi dan agen penguji |
| Membaca skripsi | Kirim PDF langsung ke LLM yang mendukung input PDF dan konteks panjang (Claude atau Gemini) | PyMuPDF untuk ekstrak teks + RAG | Peta argumen dan Peta Rawan |
| Otak penguji | LLM yang sama, satu prompt persona per penguji + satu agen "moderator" | Satu LLM yang memerankan ketiganya | Menentukan siapa bertanya, mengejar jawaban yang lemah |
| Suara masuk (STT) | Deepgram atau Whisper, dengan timestamp per kata | Web Speech API di browser | Transkrip jawaban + menghitung "eee", jeda, kecepatan bicara |
| Suara keluar (TTS) | ElevenLabs atau Google Cloud TTS, tiga suara berbeda | TTS bawaan browser | Tiap penguji punya suara khasnya sendiri |
| Alternatif suara real-time | Gemini Live API atau OpenAI Realtime API | — | Kalau ingin percakapan yang bisa disela secara natural |
| Database + auth + storage | Supabase | Firebase | Menyimpan skripsi, sesi, dan rapor |
| Deploy | Vercel (frontend) + Railway atau Render (backend) | — | Link demo untuk juri |

**Cara kerja agen moderator:** setelah mahasiswa selesai menjawab, moderator membaca transkrip dan memutuskan langkah berikutnya: penguji yang sama mengejar jawaban (kalau lemah), penguji lain masuk dengan topik baru, atau Ketua Sidang menutup sesi. Ini yang membuat panel terasa "hidup", bukan sekadar tiga chatbot yang bergiliran.

**Mengakali latensi suara:** pakai streaming TTS dan isian pendek dari penguji ("Hmm, baik…") selagi pertanyaan berikutnya disiapkan. Di demo, jeda 2–3 detik masih terasa wajar karena dosen sungguhan juga berpikir sebelum bertanya.

## Prinsip human-centered, etika, dan integritas akademik

Produk ini harus membuat mahasiswa *lebih paham* skripsinya sendiri, bukan lebih bergantung pada AI. Aturan di bawah adalah bagian dari produk.

- **Menguji, bukan mengerjakan.** AI tidak menulis ulang, memperbaiki, atau menambah isi skripsi. Peta Rawan hanya menunjukkan *di mana* masalahnya, bukan menuliskan perbaikannya.
- **Bukan alat contekan saat sidang.** Tidak ada fitur "bisikan jawaban" real-time. Contoh jawaban hanya muncul di rapor setelah sesi latihan selesai.
- **Tegas tapi tidak merendahkan.** Mode Killer boleh menekan secara akademik, tapi tidak boleh menghina pribadi. Setelah sesi berat, selalu ada ringkasan hal yang sudah bagus.
- **Pengaturan rasa aman.** Mahasiswa bisa menjeda sesi kapan saja, dan disarankan mulai dari tingkat Bersahabat. Jika muncul tanda kecemasan berat, aplikasi menyarankan istirahat dan menunjukkan layanan konseling kampus.
- **Skripsi adalah karya yang belum terbit.** File hanya dipakai untuk sesi pengguna itu, tidak dipakai melatih model, dan bisa dihapus permanen kapan saja.
- **Jujur soal batas AI.** Ada pengingat bahwa penguji AI bisa salah memahami bidang yang sangat spesifik. Rapor bukan prediksi lulus atau tidak, dan aplikasi tidak memberi nilai sidang.
- **Dosen tetap pusatnya.** Dashboard pembimbing hanya aktif atas izin mahasiswa. Posisinya membantu pembimbing, bukan menggantikan bimbingan.

## Metrik keberhasilan

Saat hackathon, yang perlu dibuktikan ada dua: pertanyaan AI terasa relevan seperti pertanyaan dosen sungguhan, dan mahasiswa merasa lebih siap setelah latihan.

**Saat hackathon (uji coba ke 5–10 mahasiswa tingkat akhir yang memakai skripsinya sendiri):**

- **Relevansi:** persentase pertanyaan yang dinilai mahasiswa "mungkin benar-benar ditanyakan dosen" (target ≥ 70%)
- **Ketepatan Peta Rawan:** persentase temuan yang memang benar-benar masalah setelah dicek mahasiswa
- **Kesiapan:** skor "seberapa siap aku sidang" (skala 1–10) sebelum dan sesudah sesi
- **Validasi ahli (bonus):** satu atau dua dosen menilai apakah pertanyaannya "masuk akal untuk sidang"

**Setelah peluncuran:**

- Rata-rata jumlah sesi per mahasiswa sebelum sidang
- Perkembangan skor rapor dari sesi pertama ke sesi terakhir
- Survei setelah sidang asli: berapa persen pertanyaan dosen yang sudah pernah dilatih
- Jumlah kampus atau prodi yang memakai Dashboard Pembimbing

## Scope hackathon dan skenario demo

Yang wajib jadi adalah satu alur utuh: unggah skripsi, Peta Rawan, satu sesi sidang dengan suara, lalu rapor. Panel yang terasa hidup lebih penting daripada fitur yang banyak.

- **Wajib:** Bedah Skripsi, Peta Rawan, Ruang Sidang dengan tiga penguji bersuara berbeda, pilihan tingkat kesulitan, Rapor Sidang.
- **Kalau sempat:** Latihan Ulang Fokus, analisis "eee" dan kecepatan bicara, avatar dengan animasi saat bicara.
- **Tidak dikerjakan:** Mode Presentasi, Dashboard Pembimbing, pedoman kampus, mode bahasa Inggris.

**Pembagian tim (contoh 4 orang):** frontend dan ruang sidang, backend dan pengolahan PDF, prompt persona dan agen moderator, serta riset pengguna, uji coba, dan pitch.

**Siapkan sebelum demo:** 2–3 skripsi asli (minta izin ke kakak tingkat atau pakai skripsi anggota tim) dari bidang berbeda, misalnya kuantitatif sosial, teknik, dan kualitatif. Ini membuktikan sistemnya bekerja lintas bidang.

**Skenario demo 3 menit:**

1. **Hook (20 detik):** "Angkat tangan, siapa yang pernah deg-degan sidang?" Lalu tunjuk juri: "Bapak dan Ibu adalah orang yang paling ditakuti mahasiswa."
2. **Bedah (30 detik):** unggah skripsi asli. Dalam hitungan detik, Peta Rawan muncul: "Angka di Tabel 4.3 berbeda dengan abstrak, halaman 54."
3. **Sidang (80 detik):** sidang langsung di mode Killer. Penguji Metodologi menyela jawaban yang berputar-putar, lalu Penguji Substansi menyambung dengan temuan dari Peta Rawan. Ini momen wow.
4. **Rapor (30 detik):** tampilkan nilai per jawaban, catatan cara bicara, dan antrean latihan berikutnya.
5. **Penutup (20 detik):** kutipan dari mahasiswa uji coba, plus ajakan ke juri: "Mau coba jadi mahasiswanya?"

**Cadangan:** rekam video demo lengkap, untuk berjaga-jaga kalau koneksi atau API suara bermasalah.

## Pertanyaan terbuka untuk diskusi

Bagian ini sengaja dibiarkan terbuka untuk dibahas bersama tim.

- [ ] **Nama produk:** tetap "Sidang Bayangan", atau alternatif seperti "Gladi Sidang" atau "Meja Hijau"?
- [ ] **Fokus awal:** sidang skripsi saja, atau langsung termasuk seminar proposal? Seminar proposal terjadi lebih awal, sehingga pengguna bisa bertahan lebih lama.
- [ ] **Bidang ilmu:** semua prodi sejak awal, atau mulai dari satu rumpun (misalnya kuantitatif sosial) agar kualitas pertanyaannya terjamin?
- [ ] **Suara real-time vs bergiliran:** pakai API real-time yang bisa disela (lebih natural, lebih rumit), atau pola tanya-jawab bergiliran (lebih stabil untuk demo)?
- [ ] **Avatar:** ilustrasi sederhana, avatar 3D, atau cukup indikator suara? Avatar yang terlalu realistis bisa terasa aneh.
- [ ] **Model bisnis:** gratis untuk mahasiswa dengan batas sesi, lalu B2B ke kampus atau prodi (lisensi untuk persiapan sidang massal)?
- [ ] **Validasi:** dosen mana yang bisa diajak menilai kualitas pertanyaan sebelum hari H hackathon?

## Sumber

- [Perbedaan Tingkat Kecemasan Ditinjau dari Jenis Kelamin pada Mahasiswa yang sedang Menyusun Skripsi](https://ejournal.unesa.ac.id/index.php/character/article/view/62208) — Jurnal Character, Unesa
- [Pengembangan Simulasi Sidang Skripsi Berbasis LLM dan RAG (abstrak)](https://openlibrary.telkomuniversity.ac.id/pustaka/files/236723/abstraksi/pengembangan-simulasi-ujian-skripsi-berbasis-large-language-model-dan-retrieval-augmented-generation-dalam-bentuk-buku-karya-ilmiah.pdf) — Telkom University
- [SuperviseAI](https://devpost.com/software/superviseai) — Devpost
- [Can AI help a PhD student prepare for the unknown? (Viva Mentor)](https://blogs.kent.ac.uk/aiteam/?p=13) — University of Kent
- [Rekomendasi Cara Memakai AI buat Latihan Simulasi Tanya Jawab Sidang](https://masoemuniversity.ac.id/artikel/rekomendasi-cara-memakai-ai-buat-latihan-simulasi-tanya-jawab-sidang/) — Ma'soem University
