# PRD — Dana Desa Terbuka

Nov 23, 2026 · @Jewan Enjoyer

## Ringkasan

**Dana Desa Terbuka** membantu warga desa memahami ke mana uang desanya pergi. Cukup foto baliho atau dokumen APBDes, lalu AI mengubah tabel anggaran yang rumit menjadi penjelasan sederhana, visual, dan bisa ditanya lewat voice note. Hasilnya: warga datang ke musyawarah desa dengan pertanyaan yang tepat, bukan dengan curiga atau diam saja.

**One-liner:** *Uang desa adalah uang warga, dan setiap warga berhak memahaminya.*

**Konsep inti:** AI berperan sebagai "penerjemah anggaran", bukan "penuduh". Ia membaca angka, mengelompokkannya ke dalam bahasa sehari-hari, membandingkan dengan tahun lalu dan desa sekitar, lalu membantu warga menyusun pertanyaan yang sopan dan berbasis data untuk forum resmi desa.

**Subtema Hackvidia:** utama *AI for Community Impact* (tata kelola desa yang lebih transparan dan partisipatif). Pendukungnya *AI for Inclusive Access* (warga desa dengan literasi dan akses internet terbatas) dan *AI for Learning & Self-Growth* (literasi anggaran publik).

**Prinsip desain:** AI tidak pernah menyimpulkan ada korupsi. Ia hanya menjelaskan, membandingkan, dan menandai hal yang *layak ditanyakan*. Penilaian tetap ada di tangan warga dan forum resmi desa.

## Masalah

Uang yang mengalir ke desa sangat besar dan sudah wajib dipublikasikan. Tapi informasinya hampir tidak bisa dipahami oleh warga yang seharusnya mengawasinya.

- **Dananya besar.** Pagu Dana Desa 2026 ditetapkan Rp60,57 triliun lewat PMK 7/2026. Sebesar 58,03% (Rp34,57 triliun) diarahkan untuk Koperasi Desa Merah Putih, dan sekitar Rp25 triliun sisanya menjadi pagu reguler ([Bisnis.com](https://ekonomi.bisnis.com/read/20260218/10/1953530/nasib-dana-desa-disorot-prabowo-mayoritas-dialokasikan-ke-kopdes-merah-putih), [JDIH Kemenkeu](https://jdih.kemenkeu.go.id/api/download/da4ae3ff-7568-4d40-9fc9-f762636d96b3/7%20Tahun%202026.pdf)). Komposisi baru ini membuat warga makin perlu memahami APBDes desanya sendiri.
- **Keterbukaan sudah diwajibkan.** Pasal 39 Permendagri 20/2018 mewajibkan kepala desa menyampaikan informasi APB Desa kepada masyarakat lewat media informasi. Minimal isinya APB Desa, pelaksana kegiatan, dan alamat pengaduan ([BPK Kalteng](https://kalteng.bpk.go.id/wp-content/uploads/2021/04/Yan-Safriansyah-Papan-Informasi-Kegiatan-Bentuk-Transparansi-Keuangan-Desa.pdf)).
- **Tapi bentuknya sulit dipahami.** Baliho APBDes biasanya berupa tabel padat dengan istilah seperti "Bidang Penyelenggaraan Pemerintahan Desa", "SiLPA", atau "Pembiayaan Netto". Warga melihatnya, tapi tidak tahu artinya, apalagi apakah angkanya wajar.
- **Pengawasan warga sangat dibutuhkan.** ICW mencatat sektor desa menyumbang kasus korupsi terbanyak sepanjang 2024, yaitu 77 dari 364 kasus yang dipantau ([RRI](https://rri.co.id/wamena/hukum/anti-korupsi/1890471/desa-menjadi-sektor-terbanyak-dengan-kasus-korupsi)).

Akibatnya, partisipasi warga di musyawarah desa sering hanya formalitas. Warga yang curiga tidak punya data untuk bertanya, dan perangkat desa yang jujur pun kesulitan menjelaskan anggarannya dengan bahasa yang dipahami warga.

## Target pengguna

Pengguna utama adalah warga desa yang ingin tahu atau terlibat dalam pembangunan desanya. Pengguna penting kedua adalah pemerintah desa yang ingin menjelaskan anggarannya dengan lebih baik, karena produk ini tidak dirancang untuk berhadapan dengan mereka.

| Persona | Situasi | Yang ia butuhkan |
| --- | --- | --- |
| **Pak Darto, 52, petani** | Melihat baliho APBDes di depan balai desa setiap tahun, tapi tidak paham isinya. Jalan ke sawahnya rusak sejak 3 tahun lalu. | Tahu apakah ada anggaran untuk jalannya, dan bagaimana mengusulkannya. Lebih nyaman bertanya lewat voice note berbahasa Jawa. |
| **Wulan, 24, pemuda desa / karang taruna** | Ingin desanya maju dan aktif di media sosial, tapi tidak mengerti istilah anggaran. | Ringkasan visual yang bisa dibagikan ke grup WhatsApp warga, dan cara bertanya yang tidak terkesan menuduh. |
| **Bu Siti, 38, kader posyandu** | Posyandunya kekurangan alat timbang, padahal katanya ada anggaran kesehatan. | Tahu berapa anggaran posyandu tahun ini dan tahun lalu, untuk dibawa ke musyawarah desa. |
| **Pak Hasan, 45, anggota BPD** | Bertugas mengawasi pemerintah desa, tapi tidak punya latar belakang keuangan. | Analisis cepat: pos mana yang naik tajam, mana yang jauh berbeda dari desa sekitar. |
| **Mas Rudi, 33, sekretaris desa** | Desanya sering dituduh tidak transparan, padahal laporannya lengkap. | Cara mudah mengubah APBDes jadi penjelasan yang dipahami warga, agar kepercayaan meningkat. |

## Produk serupa dan pembeda

Sistem untuk *mencatat* dan *mengawasi* keuangan desa sudah banyak, dan sebagian besar dibuat untuk pemerintah atau aparat penegak hukum. Yang belum ada adalah alat yang membantu **warga biasa memahami** angka-angka itu dengan bahasanya sendiri.

| Yang sudah ada | Apa yang dilakukan | Yang belum ada |
| --- | --- | --- |
| Siskeudes (Kemendagri & BPKP) | Aplikasi pencatatan dan pelaporan keuangan untuk perangkat desa | Alat internal; tidak dirancang untuk dibaca warga |
| [Jaga Desa (Kejaksaan & ABPEDNAS)](https://ekonomi.republika.co.id/berita/tdubk9416/tingkatkan-transparansi-dana-desa-kini-diawasi-lewat-aplikasi) | Pengawasan pengelolaan dana desa, terintegrasi dengan Siskeudes, ada kanal pengaduan | Bergantung pada desa yang menginput data; fokusnya pengawasan, bukan penjelasan untuk warga |
| [JAGA (KPK)](https://apps.apple.com/us/app/jaga/id1171294913?l=fr) | Aplikasi pencegahan korupsi untuk memantau layanan publik dan melapor penyimpangan | Cakupannya umum; tidak menerjemahkan APBDes ke bahasa sehari-hari |
| Website desa (SID dan sejenisnya), aplikasi kabupaten | Publikasi data desa, termasuk APBDes | Tabelnya sama sulitnya dengan baliho; banyak desa belum aktif memakainya |

**Lima pembeda Dana Desa Terbuka:**

1. **Dimulai dari apa yang sudah ada di depan warga.** Cukup foto baliho APBDes, tanpa menunggu desa memasukkan data ke sistem baru.
2. **Menjelaskan, bukan hanya menampilkan.** Istilah anggaran diterjemahkan jadi bahasa sehari-hari, termasuk lewat suara dan bahasa daerah.
3. **Memberi konteks.** Angka dibandingkan dengan tahun lalu, desa tetangga, dan aturan yang berlaku, sehingga warga tahu mana yang wajar.
4. **Mengubah curiga jadi pertanyaan.** AI membantu menyusun pertanyaan yang sopan dan berbasis data untuk musyawarah desa, bukan tuduhan di media sosial.
5. **Berpihak pada keterbukaan, bukan melawan desa.** Ada mode untuk perangkat desa agar bisa menjelaskan anggarannya lebih baik. Desa yang transparan mendapat manfaat, bukan ancaman.

Dana Desa Terbuka bisa melengkapi Jaga Desa: warga yang sudah paham dan menemukan kejanggalan bisa diarahkan ke kanal pengaduan resmi.

## Konsep inti dan cara kerja

Sistemnya mengubah satu foto baliho menjadi pemahaman warga dalam lima langkah: **tangkap, rapikan, terjemahkan, bandingkan, tanyakan**.

1. **Tangkap.** Warga memotret baliho APBDes, papan informasi kegiatan, atau mengunggah PDF dari website desa. Beberapa foto bisa digabung kalau balihonya besar.
2. **Rapikan.** AI membaca tabel dari foto, lalu menyusunnya ke struktur baku APBDes: pendapatan, belanja per bidang, dan pembiayaan. AI juga mengecek apakah penjumlahannya cocok dengan totalnya. Kalau ada angka yang ragu terbaca, AI meminta warga memastikannya dulu.
3. **Terjemahkan.** Istilah teknis diubah ke bahasa sehari-hari, dan angka besar diubah ke ukuran yang mudah dibayangkan. Contoh: "Pembinaan Kemasyarakatan Rp120 juta" menjadi "kegiatan warga seperti PKK, karang taruna, dan pengajian, sekitar Rp10 juta per bulan".
4. **Bandingkan.** Angka dibandingkan dengan APBDes tahun lalu (kalau sudah pernah difoto), desa-desa tetangga di database komunitas, dan aturan yang berlaku tahun itu.
5. **Tanyakan.** Warga bisa bertanya bebas lewat teks atau voice note. Untuk hal yang janggal, AI membantu menyusun pertanyaan yang sopan untuk musyawarah desa, BPD, atau kanal pengaduan resmi.

**Tanda "Layak Ditanyakan".** AI tidak memberi label "korupsi" atau "mencurigakan". Ia hanya memberi tanda netral dengan alasan yang jelas:

| Jenis tanda | Contoh | Pesan yang ditampilkan |
| --- | --- | --- |
| Lonjakan | Anggaran honor naik 80% dari tahun lalu | "Naik cukup besar. Mungkin ada kegiatan baru. Boleh ditanyakan alasannya." |
| Beda jauh dari desa sekitar | Biaya pembangunan jalan per meter dua kali lipat desa tetangga | "Lebih tinggi dari desa sekitar. Bisa jadi karena medan atau spesifikasi berbeda." |
| Angka tidak cocok | Jumlah rincian tidak sama dengan total bidang | "Penjumlahannya berbeda Rp15 juta. Mungkin salah cetak, perlu dicek." |
| Rincian kurang jelas | Kegiatan bernama "Lain-lain" bernilai besar | "Kegiatan ini belum dijelaskan. Boleh minta rinciannya." |
| Perubahan aturan | Komposisi anggaran berubah karena kebijakan baru tahun berjalan | "Ada aturan baru tahun ini yang memengaruhi pos ini. Ini penjelasannya." |

Setiap tanda selalu menyertakan **kemungkinan penjelasan yang wajar**. Tujuannya agar warga datang dengan rasa ingin tahu, bukan dengan tuduhan.

## Fitur

Fitur dibagi tiga kelompok. **Inti** membentuk satu alur utuh dari foto sampai pemahaman. **Unggulan** mengubah pemahaman jadi partisipasi. **Lanjutan** untuk setelah hackathon.

### Inti (MVP)

| Fitur | Apa yang dilakukan | Prioritas |
| --- | --- | --- |
| **Pindai APBDes** | Foto baliho atau unggah PDF. AI membaca tabel, menyusun strukturnya, mengecek penjumlahan, dan meminta konfirmasi untuk angka yang ragu terbaca. | MVP |
| **APBDes dalam Satu Layar** | Ringkasan visual: "Dari setiap Rp100.000 uang desa, Rp38.000 untuk pembangunan, Rp20.000 untuk pemerintahan, …" Setiap bidang bisa dibuka untuk melihat kegiatannya. | MVP |
| **Kamus Anggaran** | Ketuk istilah seperti SiLPA, Pembiayaan, atau Bidang Pemberdayaan untuk melihat artinya dalam satu kalimat sederhana. | MVP |
| **Tanya Desa** | Bertanya bebas lewat teks atau voice note, misalnya "Anggaran posyandu tahun ini berapa?" Jawaban selalu menunjuk baris anggaran sumbernya. | MVP |
| **Tanda Layak Ditanyakan** | Lonjakan, perbedaan dengan desa lain, angka tidak cocok, dan rincian kurang jelas, masing-masing dengan alasan dan kemungkinan penjelasan wajar. | MVP |

### Unggulan (dari paham menjadi ikut serta)

| Fitur | Apa yang dilakukan | Kenapa keren | Prioritas |
| --- | --- | --- | --- |
| **Bekal Musdes** | AI menyusun daftar pertanyaan yang sopan dan berbasis data untuk musyawarah desa atau BPD, siap dicetak atau dibagikan. | Mengubah curiga menjadi dialog yang sehat. | MVP (momen wow demo) |
| **Kartu Bagikan** | Infografis APBDes satu halaman yang rapi untuk dibagikan ke grup WhatsApp warga. | Pengetahuan menyebar ke seluruh desa, tidak berhenti di satu orang. | MVP |
| **Siaran Desa** | AI membuat naskah dan audio penjelasan APBDes berdurasi 2 menit dalam bahasa daerah, untuk radio komunitas, pengeras suara balai desa, atau voice note. | Menjangkau warga yang tidak bisa membaca tabel atau tidak punya smartphone. | Kalau sempat |
| **Cek Lapangan** | Warga memotret papan proyek dan kondisi fisiknya (misalnya jalan atau saluran air). AI mencocokkan volume dan lokasinya dengan anggaran, lalu menyimpannya sebagai catatan bertanggal. | Menghubungkan angka di kertas dengan kenyataan di lapangan. | Kalau sempat |
| **Mode Desa** | Perangkat desa mengunggah APBDes, lalu otomatis mendapat infografis, penjelasan, dan jawaban untuk pertanyaan warga yang sering muncul. | Desa yang jujur terbantu, bukan merasa diserang. Ini kunci adopsi. | Kalau sempat |

### Lanjutan (setelah hackathon)

| Fitur | Apa yang dilakukan | Prioritas |
| --- | --- | --- |
| **Usulan Musrenbang** | Membantu warga menyusun usulan kegiatan untuk tahun depan, lengkap dengan perkiraan biaya dari data desa lain. | Setelah MVP |
| **Lini Masa Multi-tahun** | Perubahan setiap pos anggaran dari tahun ke tahun dalam satu grafik. | Setelah MVP |
| **Peta Desa Tetangga** | Database komunitas APBDes dari banyak desa, untuk perbandingan yang lebih adil (desa dengan jumlah penduduk dan kondisi serupa). | Setelah MVP |
| **Jalur ke Kanal Resmi** | Panduan langkah ke BPD, pendamping desa, Jaga Desa, atau Ombudsman, lengkap dengan draf surat. | Setelah MVP |
| **Bot WhatsApp** | Semua fitur utama bisa dipakai lewat WhatsApp: kirim foto, terima ringkasan dan voice note. | Jangka panjang |
| **Integrasi Data Resmi** | Mengambil data langsung dari website desa atau sistem resmi jika tersedia, sehingga tidak perlu memotret. | Jangka panjang |

## Alur pengguna

Baris atas adalah alur memahami: dari foto baliho sampai bisa bertanya. Baris bawah adalah alur ikut serta: dari tanda yang janggal sampai pertanyaan dibawa ke forum resmi desa.

&#91;embedded content: alur pengguna · 7 langkah, 1 putaran tahunan\]

Ujung alurnya sengaja berada di luar aplikasi. Keberhasilan produk ini diukur dari percakapan yang terjadi di musyawarah desa, bukan dari lamanya warga memakai aplikasi.

## Rencana teknologi dan sumber data

Prinsip teknis utamanya: **angka dihitung oleh kode, penjelasan ditulis oleh AI**. AI membaca foto dan menulis penjelasan, sedangkan penjumlahan, perbandingan, dan persentase dihitung dengan kode biasa, supaya tidak ada angka yang dikarang.

| Lapis | Pilihan utama | Alternatif | Fungsi |
| --- | --- | --- | --- |
| Frontend | Next.js + Tailwind, PWA ringan untuk HP murah | Flutter | Kamera, ringkasan visual, chat, kartu bagikan |
| Membaca baliho | Model vision (Gemini, Claude, atau GPT) dengan output JSON sesuai skema APBDes | OCR open-source (PaddleOCR) + deteksi tabel | Mengubah foto menjadi data terstruktur |
| Validasi dan perhitungan | Fungsi Python/TypeScript biasa | — | Cek penjumlahan, hitung persentase, lonjakan, dan perbandingan |
| Pemetaan ke struktur baku | LLM + daftar bidang dan kegiatan baku APBDes sebagai referensi | Aturan kata kunci | Menyamakan istilah yang ditulis berbeda-beda oleh tiap desa |
| Penjelasan dan tanya jawab | LLM dengan RAG atas data APBDes desa itu + regulasi (Permendagri 20/2018, aturan Dana Desa tahun berjalan) | — | Jawaban selalu merujuk ke baris anggaran atau pasal sumbernya |
| Suara | STT: Whisper (mendukung bahasa Indonesia, dan perlu diuji untuk bahasa Jawa dan Sunda). TTS: Google Cloud TTS atau ElevenLabs | Teks saja | Tanya lewat voice note, Siaran Desa |
| Database | Supabase (Postgres + storage) | Firebase | APBDes per desa per tahun, untuk perbandingan |
| Grafik dan infografis | Recharts + ekspor gambar (html-to-image) | Chart.js | APBDes dalam Satu Layar, Kartu Bagikan |
| Deploy | Vercel | Railway | Link demo untuk juri |

**Data untuk demo:** kumpulkan 5–10 foto baliho APBDes sungguhan. Baliho ini adalah dokumen publik, jadi bisa difoto langsung di desa sekitar atau dicari dari website desa dan media sosial. Pilih beberapa desa yang bertetangga, agar fitur perbandingan bisa ditunjukkan. Siapkan juga dua tahun anggaran dari satu desa, untuk menunjukkan tanda lonjakan.

**Akurasi pembacaan:** kualitas foto baliho bervariasi (miring, silau, terpotong). Karena itu ada langkah konfirmasi: angka yang tingkat keyakinannya rendah disorot, dan warga diminta mencocokkan dengan balihonya sebelum analisis dijalankan.

## Prinsip human-centered, netralitas, etika, dan keamanan

Produk ini menyentuh kepercayaan antara warga dan pemerintah desa. Salah langkah sedikit bisa memicu fitnah atau konflik di kampung. Karena itu, prinsip di bawah adalah inti produk.

- **Tidak pernah menuduh.** AI tidak memakai kata "korupsi", "mark-up", atau "mencurigakan". Yang ada hanya tanda "layak ditanyakan", selalu disertai kemungkinan penjelasan yang wajar.
- **Jujur soal ketidakpastian.** Hasil pembacaan foto bisa salah. Setiap angka bisa ditelusuri ke bagian foto aslinya, dan angka yang ragu wajib dikonfirmasi warga.
- **Netral secara politik.** Produk menjelaskan isi anggaran dan aturan yang berlaku tanpa menilai kebijakan pemerintah pusat, daerah, atau desa. Tidak berpihak pada calon kepala desa mana pun, terutama menjelang pilkades.
- **Mendorong jalur resmi.** Pertanyaan diarahkan ke musyawarah desa, BPD, pendamping desa, atau kanal pengaduan resmi, bukan ke media sosial. Kartu Bagikan hanya berisi ringkasan data dan penjelasan, tanpa tanda "layak ditanyakan", agar tidak mudah dipelintir.
- **Melindungi warga yang bertanya.** Pertanyaan bisa disusun dan disimpan tanpa identitas. Tidak ada fitur yang menampilkan siapa saja yang menanyakan apa ke pihak desa.
- **Hanya dokumen publik.** Produk hanya memproses dokumen yang memang wajib dipublikasikan (APBDes, papan kegiatan). Data pribadi seperti nama penerima bantuan tidak ditampilkan atau dianalisis.
- **Desa sebagai mitra.** Mode Desa memberi perangkat desa kesempatan menjelaskan sebelum dipertanyakan. Desa juga bisa menambahkan klarifikasi resmi pada setiap tanda.
- **Ramah untuk semua warga.** Bahasa sederhana, suara, bahasa daerah, tulisan besar, dan tetap berfungsi di HP murah dengan sinyal lemah.

## Metrik keberhasilan

Saat hackathon, ada dua hal yang perlu dibuktikan: AI bisa membaca baliho sungguhan dengan akurat, dan warga benar-benar jadi lebih paham setelah memakainya.

**Saat hackathon:**

- **Akurasi pembacaan:** persentase angka yang terbaca benar dari 5–10 foto baliho asli (target ≥ 95% setelah langkah konfirmasi).
- **Uji pemahaman warga:** 10 warga atau mahasiswa diberi 5 pertanyaan tentang satu APBDes (misalnya "Berapa anggaran kesehatan?" atau "Bidang mana yang terbesar?"). Mereka menjawab dua kali, sekali dengan baliho asli dan sekali dengan aplikasi. Bandingkan jumlah jawaban benar dan waktu yang dibutuhkan.
- **Kualitas penjelasan:** penilaian dari satu pendamping desa atau perangkat desa tentang apakah penjelasan AI akurat dan adil.

**Setelah peluncuran:**

- Jumlah desa yang APBDes-nya sudah dipindai warga
- Jumlah Bekal Musdes yang benar-benar dibawa ke musyawarah desa
- Jumlah desa yang memakai Mode Desa secara sukarela
- Survei kepercayaan warga terhadap pemerintah desa, sebelum dan sesudah memakai aplikasi (target: naik, bukan turun)

## Scope hackathon dan skenario demo

Yang wajib jadi adalah satu alur utuh: foto baliho sungguhan, ringkasan visual, tanya jawab dengan voice note, tanda layak ditanyakan, lalu Bekal Musdes. Akurasi membaca baliho asli adalah fondasinya, jadi uji sejak hari pertama.

- **Wajib:** Pindai APBDes, APBDes dalam Satu Layar, Kamus Anggaran, Tanya Desa (teks + voice note), Tanda Layak Ditanyakan, Bekal Musdes, Kartu Bagikan.
- **Kalau sempat:** Siaran Desa (audio bahasa Jawa atau Sunda), Cek Lapangan, Mode Desa.
- **Tidak dikerjakan:** Bot WhatsApp, integrasi data resmi, Peta Desa Tetangga skala besar, Usulan Musrenbang.

**Pembagian tim (contoh 4 orang):**

| Peran | Tanggung jawab |
| --- | --- |
| Frontend | Kamera dan konfirmasi angka, ringkasan visual, chat, Kartu Bagikan |
| Backend + AI | Pembacaan foto ke JSON, validasi dan perhitungan, RAG regulasi, tanya jawab |
| Data + domain | Mengumpulkan foto baliho asli, menyusun daftar bidang dan istilah baku, merangkum regulasi |
| Riset + pitch | Uji pemahaman ke 10 warga, wawancara pendamping desa atau perangkat desa, deck, video cadangan |

**Skenario demo 3 menit:**

1. **Hook (20 detik):** tunjukkan foto baliho APBDes sungguhan di layar besar. "Siapa di ruangan ini yang bisa menjelaskan isi baliho ini dalam 30 detik?"
2. **Pindai (30 detik):** foto baliho itu dengan HP. Dalam hitungan detik muncul "Dari setiap Rp100.000 uang desa, …"
3. **Tanya lewat suara (40 detik):** voice note berbahasa Jawa: "Anggaran posyandu piro?" Jawaban muncul dengan suara, menunjuk baris anggaran sumbernya.
4. **Tanda dan Bekal Musdes (50 detik):** tampilkan satu tanda lonjakan dengan kemungkinan penjelasan wajarnya. Lalu tekan "Susun pertanyaan", dan muncul pertanyaan sopan yang siap dibawa ke musyawarah desa.
5. **Dampak (40 detik):** hasil uji pemahaman ("jawaban benar naik dari X ke Y"), kutipan perangkat desa atau pendamping desa, dan visi Mode Desa: transparansi yang membantu desa, bukan menyerangnya.

**Cadangan:** rekam video demo lengkap, dan siapkan hasil pindaian yang sudah tersimpan kalau kamera atau koneksi bermasalah.

## Keberlanjutan, mitra, dan model bisnis

Produk transparansi publik paling kuat kalau **gratis bagi warga** dan didanai oleh pihak yang mendapat manfaat dari tata kelola desa yang baik.

| Sumber keberlanjutan | Bentuk kerja sama | Kenapa mereka tertarik |
| --- | --- | --- |
| Pemerintah kabupaten (DPMD) | Lisensi Mode Desa untuk semua desa di kabupaten, plus dashboard ringkasan | Membantu pembinaan desa dan meningkatkan kepercayaan publik |
| Pendamping desa dan program pemberdayaan | Alat bantu untuk sosialisasi APBDes ke warga | Pekerjaan sosialisasi jadi lebih cepat dan menjangkau lebih banyak warga |
| Lembaga donor dan program tata kelola | Hibah untuk pengembangan, perluasan bahasa daerah, dan riset dampak | Sesuai dengan misi transparansi dan partisipasi warga |
| Organisasi masyarakat sipil dan kampus (KKN) | Mahasiswa KKN memakai aplikasi untuk sosialisasi APBDes di desa tempat KKN | Program KKN yang lebih bermakna dan terukur |
| Media lokal | Data APBDes yang sudah rapi untuk liputan berbasis data | Bahan liputan yang akurat |

**Tahapan pengembangan:**

1. **Hackathon:** pindai baliho, ringkasan, tanya jawab, tanda, Bekal Musdes.
2. **Pilot (3 bulan):** 5–10 desa di satu kecamatan bekerja sama dengan pendamping desa. Uji Mode Desa dan Siaran Desa.
3. **Program KKN:** kerja sama dengan kampus agar mahasiswa KKN memindai dan menyosialisasikan APBDes di desa-desa tempat KKN. Ini cara cepat membangun database perbandingan.
4. **Skala kabupaten:** kerja sama dengan DPMD, bot WhatsApp, dan integrasi data resmi.

## Pertanyaan terbuka untuk diskusi

Bagian ini sengaja dibiarkan terbuka untuk dibahas bersama tim.

- [ ] **Nama produk:** tetap "Dana Desa Terbuka", atau yang lebih akrab seperti "Melek Desa", "Baca APBDes", atau "Uang Kita"?
- [ ] **Pengguna utama untuk demo:** warga biasa, BPD, atau perangkat desa? Masing-masing butuh cerita pitch yang berbeda.
- [ ] **Desa mana yang jadi studi kasus?** Ada anggota tim yang punya akses ke desa asal atau desa KKN?
- [ ] **Seberapa jauh tanda "layak ditanyakan"?** Terlalu banyak tanda bisa memicu kecurigaan, terlalu sedikit membuat fitur ini tidak berguna. Perlu ditentukan ambang yang adil.
- [ ] **Perbandingan antar desa:** desa dengan jumlah penduduk, luas, dan medan yang berbeda tidak adil dibandingkan langsung. Variabel apa yang dipakai untuk mencari "desa serupa"?
- [ ] **Bahasa daerah apa yang didukung dulu?** Jawa dan Sunda paling banyak penuturnya, tapi kualitas STT/TTS-nya perlu diuji.
- [ ] **Validasi domain:** pendamping desa, perangkat desa, atau dosen akuntansi sektor publik siapa yang bisa memeriksa penjelasan AI?

## Sumber

- [Nasib Dana Desa, Disorot Prabowo, Mayoritas Dialokasikan ke Kopdes Merah Putih](https://ekonomi.bisnis.com/read/20260218/10/1953530/nasib-dana-desa-disorot-prabowo-mayoritas-dialokasikan-ke-kopdes-merah-putih) — Bisnis.com
- [PMK Nomor 7 Tahun 2026 tentang Pengelolaan Dana Desa](https://jdih.kemenkeu.go.id/api/download/da4ae3ff-7568-4d40-9fc9-f762636d96b3/7%20Tahun%202026.pdf) — JDIH Kemenkeu
- [Papan Informasi Kegiatan, Bentuk Transparansi Keuangan Desa](https://kalteng.bpk.go.id/wp-content/uploads/2021/04/Yan-Safriansyah-Papan-Informasi-Kegiatan-Bentuk-Transparansi-Keuangan-Desa.pdf) — BPK Perwakilan Kalimantan Tengah
- [Desa Menjadi Sektor Terbanyak dengan Kasus Korupsi](https://rri.co.id/wamena/hukum/anti-korupsi/1890471/desa-menjadi-sektor-terbanyak-dengan-kasus-korupsi) — RRI
- [Tingkatkan Transparansi, Dana Desa Kini Diawasi Lewat Aplikasi](https://ekonomi.republika.co.id/berita/tdubk9416/tingkatkan-transparansi-dana-desa-kini-diawasi-lewat-aplikasi) — Republika
- [JAGA](https://apps.apple.com/us/app/jaga/id1171294913?l=fr) — App Store (KPK)
