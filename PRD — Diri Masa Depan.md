# PRD — Diri Masa Depan

Nov 23, 2026 · @Jewan Enjoyer

## Ringkasan

**Diri Masa Depan** adalah aplikasi yang mempertemukan anak muda dengan dirinya sendiri 20 tahun lagi. Pengguna bisa melihat wajahnya, mendengar suaranya, dan mengobrol dengannya. Cerita hidup "diri masa depan" itu dihitung dari kebiasaan keuangan pengguna hari ini.

**One-liner:** *Keputusan kecil hari ini, dijelaskan langsung oleh orang yang paling merasakan akibatnya: kamu sendiri di usia 40.*

**Konsep inti:** Ada dua kemungkinan masa depan. Yang pertama terjadi kalau kebiasaan sekarang berlanjut, yang kedua kalau pengguna mulai berubah. Keduanya hidup berdampingan, dan pengguna bisa melihat masa depannya bergeser setiap kali ia mengubah satu kebiasaan.

**Subtema Hackvidia:** utama *AI for Daily Living* (pengelolaan keuangan). Pendukungnya *AI for Health & Wellbeing* (mengurangi kecemasan tentang masa depan) dan *AI for Learning & Self-Growth* (literasi keuangan lewat pengalaman, bukan ceramah).

**Prinsip desain:** angka dihitung oleh kode, cerita ditulis oleh AI. Jadi semua angka yang diucapkan diri masa depan bisa dipertanggungjawabkan.

## Masalah

Anak muda tahu menabung itu penting, tapi "aku 20 tahun lagi" terasa seperti orang asing. Akibatnya, kesenangan hari ini hampir selalu menang. Paylater dan pinjol membuat godaan itu makin mudah: tinggal satu klik.

- **Data Indonesia:** menurut OJK, peminjam berusia 19–34 tahun menyumbang 48,65% kredit macet pinjol per Maret 2026. Rasio kredit macet (TWP90) naik dari 2,77% (Maret 2025) menjadi 4,52% (Maret 2026) ([Gebrak.id](https://www.gebrak.id/2026/05/gen-z-dan-milenial-paling-banyak-macet.html)).
- **Akar psikologisnya punya nama:** *future self-continuity*, yaitu seberapa terhubung seseorang dengan dirinya di masa depan. Makin rendah keterhubungannya, makin mudah ia mengorbankan masa depan.
- **Bukti bahwa ini bisa diubah:** dalam riset Hal Hershfield, orang yang melihat foto dirinya yang dituakan bersedia menabung sekitar 33% lebih banyak dari gajinya. Dalam eksperimen VR, angkanya sekitar dua kali lipat ([NYU Stern](https://www.stern.nyu.edu/experience-stern/faculty-research/hershfield-retirement-savings)).
- **Bukti bahwa AI bisa membantu:** proyek *Future You* dari MIT Media Lab (344 peserta, usia 18–30) menemukan bahwa satu sesi singkat mengobrol dengan AI "diri usia 60" menurunkan kecemasan dan meningkatkan keterhubungan dengan diri masa depan ([MIT Media Lab](https://www.media.mit.edu/publications/future-you-a-conversation-with-an-ai-generated-future-self-reduces-anxiety-negative-emotions-and-increases-future-self-continuity/)).

Literasi keuangan yang ada saat ini umumnya berupa ceramah, angka, dan infografis. Semua itu menyentuh logika, padahal masalahnya ada di emosi.

## Target pengguna

Pengguna utama adalah anak muda Indonesia usia 18–27 tahun yang mulai memegang uang sendiri: mahasiswa dan pekerja awal karier. Usia 40 dipilih sebagai titik masa depan karena masih terbayang (punya keluarga, rumah, orang tua yang menua), tidak sejauh usia 60.

| Persona | Situasi | Yang ia butuhkan |
| --- | --- | --- |
| **Rara, 21, mahasiswi** | Uang saku Rp2,5 juta + freelance desain. Aktif di 3 aplikasi paylater, sering checkout tengah malam. | Sadar dampak kebiasaan kecil tanpa merasa dihakimi. |
| **Dimas, 24, fresh graduate** | Gaji setara UMR, ikut membiayai adik dan orang tua (generasi sandwich). Belum punya dana darurat. | Rencana realistis yang tetap menghargai tanggung jawabnya ke keluarga. |
| **Sinta, 26, pekerja kantoran** | Penghasilan cukup, tapi gaya hidup naik terus. Ingin punya rumah, tapi tidak tahu mulai dari mana. | Melihat jalur konkret: kapan rumah itu mungkin dan apa yang harus diubah. |

## Produk serupa dan pembeda

Ide "ngobrol dengan diri masa depan" sudah dibuktikan oleh MIT, jadi kita tidak mengklaim idenya baru. Kebaruan kita ada di **pembuktian dengan angka nyata, dua masa depan yang bisa dibandingkan, dan konteks Indonesia**. Ini perlu disampaikan terbuka ke juri: riset MIT menjadi validasi, bukan ancaman.

| Aspek | Future You (MIT Media Lab) | Diri Masa Depan (kita) |
| --- | --- | --- |
| Sifat | Prototipe riset, satu sesi | Produk dengan siklus mingguan |
| Usia diri masa depan | 60 tahun | 40-an (20 tahun lagi) |
| Dasar cerita | Tujuan dan sifat pribadi | Proyeksi keuangan yang dihitung dari data pengguna |
| Jumlah masa depan | Satu | Dua: "kalau tetap begini" vs "kalau mulai berubah" |
| Interaksi "bagaimana kalau" | Tidak ada | Geser satu kebiasaan, ceritanya langsung berubah |
| Dari ngobrol ke aksi | Tidak ada | Misi kecil mingguan + check-in |
| Bahasa dan konteks | Inggris, umum | Bahasa Indonesia santai; paylater, pinjol, generasi sandwich, arisan |
| Bentuk | Teks + foto | Teks + suara + foto |

Produk literasi keuangan dan aplikasi budgeting lokal sudah banyak, tapi semuanya berbasis angka dan grafik. Sejauh penelusuran awal kami, belum ada produk lokal yang memakai pendekatan emosional "bertemu dirimu sendiri". Ini perlu dicek ulang sebelum pitch.

## Konsep inti dan cara kerja

Sistemnya punya empat lapis. Lapis bawah menghitung angka, lapis atas mengubah angka itu menjadi pengalaman yang menyentuh.

1. **Profil "aku sekarang":** usia, penghasilan atau uang saku, pengeluaran rutin, cicilan atau paylater, tabungan, tujuan hidup, dan hal yang paling ia pedulikan (keluarga, rumah, karier, kebebasan).
2. **Mesin proyeksi (kode biasa, bukan AI):** menghitung dua skenario selama 20 tahun dengan asumsi yang terlihat dan bisa diubah. Contohnya inflasi 3% per tahun, imbal hasil tabungan konservatif, dan bunga paylater. Hasilnya berupa angka di usia tertentu: dana darurat, total utang, kapan bisa DP rumah.
3. **Kenangan masa depan (AI):** dari angka tadi, AI menulis linimasa hidup yang konsisten. Contohnya: "Usia 29 aku akhirnya lunas paylater", "Usia 34 DP rumah di Bekasi". AI tidak boleh mengarang angka di luar hasil mesin proyeksi.
4. **Persona diri masa depan (AI):** karakter yang bicara sebagai pengguna di usia 40-an. Ia hangat, jujur, dan memakai gaya bahasa pengguna sendiri. Semua jawabannya bersandar pada linimasa dan angka di atas.

**Dua masa depan, bukan satu.** Diri masa depan versi "tetap begini" tidak digambarkan sengsara secara dramatis. Ia realistis dan sedikit menyesal: *"Aku masih ngontrak, dan tiap Lebaran mikir dulu sebelum kasih ke Ibu."* Versi "mulai berubah" bukan kaya raya, tapi lebih tenang. Perbedaan yang jujur dan masuk akal lebih menyentuh daripada menakut-nakuti.

**Contoh percakapan:**

> **Pengguna:** Aku mau beli HP baru pakai paylater 12 bulan, boleh nggak?
>
> **Diri masa depan:** Aku ingat HP itu. Cicilannya kelihatan kecil, Rp450 ribu sebulan. Tapi waktu itu kita juga masih punya dua cicilan lain. Coba deh tunggu 3 bulan sambil nabung setengahnya. Aku hitung, itu bikin dana daruratmu kebentuk 5 bulan lebih cepat.

## Fitur

MVP hackathon fokus ke lima fitur yang membentuk satu pengalaman utuh. Sisanya untuk pengembangan setelah hackathon.

| Fitur | Apa yang dilakukan | Prioritas |
| --- | --- | --- |
| **Kenali Aku** | Onboarding 3 menit lewat percakapan, bukan formulir panjang. Opsional: unggah screenshot mutasi e-wallet atau bank, lalu AI mengelompokkan pengeluarannya. | MVP |
| **Dua Masa Depan** | Mesin proyeksi + linimasa "kenangan masa depan" untuk kedua skenario, ditampilkan berdampingan. | MVP |
| **Wajah Masa Depan** | Selfie diubah jadi foto diri usia 40-an. Fotonya dipakai sebagai avatar saat mengobrol. | MVP |
| **Ngobrol dengan Aku** | Chat teks dan suara dengan diri masa depan. Bisa bertanya apa saja, dari "perlu beli motor nggak?" sampai "kita jadi nikah nggak?" | MVP |
| **Bagaimana Kalau…** | Slider kebiasaan (jajan kopi, paylater, nabung otomatis). Saat digeser, angka, linimasa, dan nada bicara diri masa depan ikut berubah. | MVP (momen wow) |
| **Misi Kecil** | 1–3 aksi konkret per minggu yang disarankan diri masa depan, misalnya "matikan satu paylater". Ada check-in mingguan. | Setelah MVP (versi sederhana bisa ikut demo) |
| **Surat dari Masa Depan** | Kartu cantik berisi pesan dari diri masa depan untuk dibagikan ke media sosial. Jadi jalur viral. | Setelah MVP |
| **Koneksi data otomatis** | Tersambung ke rekening atau e-wallet lewat open banking, jadi pengguna tidak perlu input manual. | Jangka panjang |
| **Dimensi lain** | Kesehatan (tidur, olahraga, rokok) dan karier, bukan hanya keuangan. | Jangka panjang |

## Alur pengguna

Sesi pertama berjalan dari kiri ke kanan. Setelah itu, pengguna masuk ke putaran mingguan: menjalankan misi, check-in, lalu kembali mengobrol.

&#91;embedded content: alur pengguna · 6 langkah, 2 putaran\]

Slider "Bagaimana Kalau" mengirim pengguna kembali ke Dua Masa Depan dengan proyeksi yang dihitung ulang. Di situlah pengguna merasakan bahwa masa depannya bisa diubah.

## Rencana teknologi

Pilih stack yang cepat dirakit dalam 24–48 jam dan memakai layanan AI siap pakai. Tidak perlu melatih model sendiri. Semua pilihan di bawah bisa ditukar dengan alternatifnya sesuai keahlian tim.

| Lapis | Pilihan utama | Alternatif | Fungsi |
| --- | --- | --- | --- |
| Frontend | Next.js + Tailwind, dibuat sebagai PWA mobile-first | React Native / Flutter | Tampilan onboarding, dua masa depan, chat, slider |
| Backend | Next.js API routes | FastAPI (Python) | Menyambungkan semua layanan, menyimpan sesi |
| Mesin proyeksi | Fungsi TypeScript/Python biasa | Spreadsheet sebagai prototipe | Menghitung dua skenario 20 tahun secara deterministik |
| LLM (otak persona) | Claude, Gemini, atau GPT lewat API dengan output terstruktur (JSON) | Model open-source via Groq/Together | Menulis linimasa, memerankan diri masa depan, membaca screenshot mutasi |
| Wajah masa depan | Model image editing via Replicate atau fal.ai | Ilustrasi bergaya kartun (lebih aman dan cepat) | Menuakan selfie jadi usia 40-an |
| Suara | Speech-to-text: Whisper atau Web Speech API. Text-to-speech: ElevenLabs atau Google Cloud TTS (bahasa Indonesia) | Teks saja | Mengobrol lewat suara |
| Database + auth | Supabase (Postgres, auth, storage) | Firebase | Profil, riwayat chat, misi |
| Deploy | Vercel | Railway / Render | Link demo yang bisa dibuka juri |

**Aturan teknis paling penting:** LLM hanya menerima hasil mesin proyeksi sebagai fakta dan dilarang membuat angka baru. Validasi sederhana: setiap angka di jawaban AI dicocokkan dengan data proyeksi sebelum ditampilkan.

## Prinsip human-centered, etika, dan keamanan

Produk ini menyentuh tiga hal yang sangat pribadi: wajah, uang, dan perasaan tentang masa depan. Karena itu, aturan di bawah adalah bagian dari produk, bukan tambahan.

- **Menyemangati, tidak menakut-nakuti.** Diri masa depan selalu berpihak pada pengguna. Versi "tetap begini" pun bicara dengan sayang, tidak menyalahkan.
- **Selalu "salah satu kemungkinan".** Setiap sesi diawali pengingat bahwa ini simulasi dari asumsi, bukan ramalan. Asumsinya bisa dilihat dan diubah.
- **Bukan nasihat keuangan.** Tidak merekomendasikan produk investasi, pinjaman, atau merek tertentu. Fokusnya kebiasaan, bukan jualan.
- **Data minimal dan bisa dihapus.** Selfie dihapus setelah foto masa depan jadi. Screenshot mutasi tidak disimpan, hanya ringkasan kategorinya. Ada tombol "hapus semua dataku".
- **Wajah dan suara hanya milik sendiri.** Hanya selfie pengguna sendiri yang boleh dipakai, dan foto hasilnya diberi tanda "dibuat AI". Kloning suara (jika ada) wajib opt-in dan hanya suara pengguna sendiri.
- **Peka terhadap kondisi sulit.** Jika pengguna menunjukkan tanda tertekan berat, misalnya terjerat banyak pinjol atau putus asa, diri masa depan berhenti bermain peran. Ia lalu mengarahkan ke bantuan nyata, seperti Kontak OJK 157 untuk masalah pinjol dan layanan konseling kesehatan jiwa.
- **Adil untuk semua kondisi.** Penghasilan kecil tidak boleh berujung masa depan yang suram. Proyeksi selalu menunjukkan langkah yang mungkin dilakukan dari titik mana pun. Generator wajah juga perlu diuji pada berbagai warna kulit agar tidak bias.
- **Usia 18+.** Pengguna di bawah 18 tahun tidak dilayani, karena menyangkut data wajah dan keuangan.

## Metrik keberhasilan

Saat hackathon, yang perlu dibuktikan adalah perubahan perasaan dan niat. Perubahan perilaku nyata baru bisa diukur setelahnya.

**Saat hackathon (uji cepat ke 10–20 mahasiswa, sebelum dan sesudah satu sesi):**

- Skor keterhubungan dengan diri masa depan (skala sederhana 1–7, diadaptasi dari skala *future self-continuity*)
- Niat menabung atau mengurangi paylater dalam 30 hari ke depan
- Persentase peserta yang menerima minimal satu misi
- Satu atau dua kutipan reaksi peserta untuk slide pitch

**Setelah peluncuran:**

- Retensi check-in mingguan (minggu ke-1 sampai ke-4)
- Persentase misi yang diselesaikan
- Perubahan rasio tabungan dan jumlah paylater aktif setelah 30 dan 90 hari (dilaporkan pengguna atau dari data yang tersambung)
- Tingkat berbagi "Surat dari Masa Depan"

## Scope hackathon dan skenario demo

Yang wajib jadi adalah satu alur utuh, dari onboarding sampai slider "bagaimana kalau". Lebih baik lima fitur yang halus daripada sembilan fitur yang setengah jadi.

- **Wajib:** onboarding singkat, mesin proyeksi, linimasa dua masa depan, satu foto wajah masa depan, chat teks + suara keluar (TTS), dan slider.
- **Kalau sempat:** input suara, baca screenshot mutasi, satu misi sederhana.
- **Tidak dikerjakan:** open banking, dimensi kesehatan dan karier, aplikasi native.

**Pembagian tim (contoh 4 orang):** frontend dan UI, backend dan mesin proyeksi, prompt dan persona AI, serta riset pengguna dan pitch.

**Skenario demo 3 menit:**

1. **Hook (20 detik):** "Siapa di sini yang pernah checkout paylater tengah malam?" Tampilkan data OJK soal kredit macet anak muda.
2. **Kenali Aku (30 detik):** pakai persona Rara yang sudah diisi sebelumnya, supaya demo tidak tergantung input langsung.
3. **Dua Masa Depan (40 detik):** dua wajah Rara di usia 41 berdampingan, dengan linimasa masing-masing.
4. **Ngobrol (50 detik):** Rara bertanya, "Aku mau beli HP pakai paylater, boleh?" Diri masa depannya menjawab dengan suara, membawa angka dari proyeksi.
5. **Bagaimana Kalau (30 detik):** geser slider "stop 1 paylater". Angka, linimasa, dan nada bicara langsung berubah. Ini momen wow.
6. **Penutup (10 detik):** tampilkan "Surat dari Masa Depan" dan satu kutipan dari peserta uji coba.

**Cadangan:** siapkan rekaman video demo, untuk berjaga-jaga kalau internet atau API bermasalah saat presentasi.

## Pertanyaan terbuka untuk diskusi

Bagian ini sengaja dibiarkan terbuka untuk didiskusikan bersama tim.

- [ ] **Nama produk:** tetap "Diri Masa Depan", atau yang lebih catchy seperti "Aku 2046" atau "Kabar dari Nanti"?
- [ ] **Fokus:** keuangan saja, atau langsung digabung dengan kesehatan atau karier? Lebih luas berarti lebih menarik, tapi lebih sulit dihitung dengan jujur.
- [ ] **Wajah realistis atau ilustrasi?** Foto realistis lebih menyentuh, tapi berisiko terasa aneh (*uncanny*) dan lebih berat soal privasi.
- [ ] **Dua masa depan, atau satu yang berubah?** Dua versi lebih dramatis untuk demo, satu versi lebih sederhana dan lebih tidak menghakimi.
- [ ] **Horizon waktu:** dipatok 20 tahun, atau pengguna bebas memilih (5, 10, 20 tahun)?
- [ ] **Kloning suara:** layak dipakai, atau cukup suara AI generik yang dituakan?
- [ ] **Model bisnis:** B2C freemium, atau B2B ke bank, kampus, dan program literasi keuangan OJK?
- [ ] **Risiko "menakut-nakuti":** bagaimana memastikan pengguna dengan penghasilan rendah tetap merasa punya harapan?

## Sumber

- [Future You: A conversation with an AI-generated future self…](https://www.media.mit.edu/publications/future-you-a-conversation-with-an-ai-generated-future-self-reduces-anxiety-negative-emotions-and-increases-future-self-continuity/) — MIT Media Lab
- [Back to the Future: Convincing People to Save](https://www.stern.nyu.edu/experience-stern/faculty-research/hershfield-retirement-savings) — NYU Stern (Hal Hershfield)
- [Gen Z dan Milenial Paling Banyak Macet Bayar Pinjol, OJK Ungkap Data Terbaru](https://www.gebrak.id/2026/05/gen-z-dan-milenial-paling-banyak-macet.html) — Gebrak.id, Mei 2026
