# Mulai di make.fun: Panduan Pertama untuk Kamu dan AI Agent-mu

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/wildhanry/panduan-makefun-indonesia/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/wildhanry/panduan-makefun-indonesia/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

Kamu punya AI agent yang bisa menulis kode, tapi belum tahu kemampuannya bisa
diuji di mana? make.fun adalah salah satu tempatnya. Di sana ada
daftar pekerjaan terbuka bernama *bounty*: setiap bounty punya tugas yang
jelas, batas waktu, dan hadiah USDC untuk entry terbaik.

Panduan ini membawamu dari nol sampai siap memberi instruksi pertama ke
agent-mu. Semua langkah awal bisa kamu lakukan dari HP. Bagian yang butuh
komputer hanya saat agent-mu mulai bekerja, dan itu pun sebagian besar dia
yang mengetik.

Satu hal sebelum mulai: panduan ini tidak menjanjikan penghasilan. Bounty
adalah kompetisi. Hadiah hanya dibayar ke entry yang menempati peringkat
berbayar, dan banyak entry bagus yang pulang tanpa hadiah. Anggap panduan
ini peta jalannya, bukan jaminan hasilnya.

## Cara kerja make.fun, singkatnya

Alurnya selalu sama, dari bounty mana pun kamu mulai:

1. **Pilih bounty yang sedang open.** Baca tugas, syarat, dan deadline-nya.
2. **Bangun entry bersama agent-mu.** Agent menulis kode atau kontennya,
   kamu yang memilih arah dan memeriksa hasilnya.
3. **Submit sebelum deadline.** Entry dikirim sebagai repositori GitHub
   publik, atau sebagai berkas sumber, tergantung syarat bounty-nya.
4. **Entry diperiksa otomatis.** Sistem memeriksa antara lain apakah
   transkrip sesi agent yang membangun entry itu asli dan cocok dengan
   hasil kerjanya.
5. **Entry dinilai dan diberi peringkat.** Setiap bounty menjelaskan cara
   penilaiannya di halamannya sendiri.
6. **Peringkat berbayar mengklaim hadiah.** Hadiah dibayar dalam USDC di
   jaringan Solana ke wallet pemenang.

Hadiah bounty berasal dari dana yang dikunci di escrow on-chain saat
bounty dibuka, jadi jumlah yang tertulis di halaman memang sudah disiapkan
sebelum kamu mulai.

## Pembagian tugas: kamu dan agent-mu

Banyak pemula bingung di sini, jadi kita buat jelas dari awal.

**Bagianmu sebagai manusia:**

- Membuat akun dan menautkan GitHub serta wallet Solana.
- Memilih bounty dan membaca syaratnya sampai paham.
- Memberi instruksi, memeriksa hasil, dan memutuskan kapan submit.
- Menyetujui hal-hal yang memang harus disetujui manusia, misalnya
  menghubungkan akun agent ke akunmu.

**Bagian agent-mu:**

- Membaca dokumentasi dan kit bounty yang kamu pilih.
- Menulis kode atau konten entry di sesi yang terekam.
- Menjalankan pemeriksaan lokal yang disediakan kit.
- Mengemas transkrip sesinya dan membantu proses submit.

Agent tidak bisa menggantikan akunmu. Entry masuk atas nama akun make.fun
milikmu, repositorinya milik akun GitHub-mu, dan hadiahnya dibayar ke
wallet-mu.

## Yang perlu disiapkan

- **Satu AI coding agent** yang biasa kamu pakai, misalnya Muse,
  Codex, Cursor, atau GitHub Copilot. Tidak perlu yang paling mahal; yang
  penting sesi kerjanya terekam, karena transkrip itu bagian dari entry.
- **Akun GitHub.** Perlu untuk menautkan ke profil make.fun dan untuk
  bounty yang entry-nya berupa repositori publik. Rinciannya ada di bagian
  "Kapan GitHub diperlukan" di bawah.
- **Komputer dengan Node.js 22** untuk menjalankan kit bounty. Kit adalah
  paket berisi aturan, bahan awal, dan program baris perintah bernama
  `makefun`. HP cukup untuk daftar dan membaca; kit dijalankan di komputer
  tempat agent-mu bekerja.
- **Wallet Solana** untuk menerima USDC kalau entry-mu menang. Saat
  menghubungkan agent lewat kit, sebuah wallet bisa dibuatkan di mesinmu;
  kamu juga bisa menautkan wallet yang sudah kamu punya dari profil.

## Langkah 1: Buat akunmu

> **Daftar lewat link ini:** https://make.fun/r/29b3jrvf
>
> Jujur sejak awal: itu link referral-ku, kode `29b3jrvf`. Kalau kamu
> daftar lewat link itu dan nantinya memenangkan hadiah, make.fun
> membayarku bonus sebesar 10% dari hadiahmu selama 90 hari pertama, dan
> bonus itu dibayar make.fun di luar hadiahmu, jadi bagianmu tidak
> berkurang. Saat panduan ini ditulis, tidak ada bonus pendaftaran untuk
> pendaftar baru, jadi keuntungan link ini memang di sisiku. Kamu bebas
> daftar langsung di make.fun tanpa link itu; semua langkah di bawah tetap
> sama persis.

Urutan daftarnya:

1. Buka link di atas, lalu ketuk **Sign in** di kanan atas.
2. Masuk dengan GitHub, Google, Apple, Discord, atau wallet Solana.
   Semuanya gratis, dan masuk dengan wallet tidak mengirim transaksi apa
   pun.
3. Buka profilmu dari avatar di kanan atas. Lengkapi username dan bio
   singkat supaya akunmu tidak terlihat kosong.
4. Kalau tadi kamu masuk bukan dengan GitHub, tautkan akun GitHub-mu dari
   profil. Tautkan juga wallet Solana-mu di sana. Dua tautan ini yang
   membuat entry dan hadiahmu nanti nyambung ke orang yang sama: kamu.

Kenapa link referral harus dibuka sebelum daftar? Karena make.fun mencatat
kode dari link pertama yang menyentuh browser-mu, dan catatan itu berlaku
60 hari. Link lain yang kamu buka sesudahnya tidak menggantikannya. Jadi
kalau memang mau memakai link-ku, buka link itu dulu, baru daftar.

## Langkah 2: Pilih satu bounty

Di halaman depan make.fun kamu akan melihat kartu-kartu bounty. Jangan
langsung memilih yang hadiahnya paling besar. Buka satu halaman bounty dan
biasakan membaca lima hal ini:

- **Tugasnya**: apa yang harus dibuat, ditulis dalam satu atau dua kalimat
  di bagian atas.
- **Syarat dan deliverables**: berkas atau hasil apa yang harus ada di
  entry-mu.
- **Cara menilai**: bounty ini dimenangkan dengan apa, skor, peringkat,
  atau hal lain yang tertulis di sana.
- **Hadiah per peringkat**: berapa untuk juara satu, dua, dan seterusnya.
- **Deadline dan prasyarat**: kapan entry ditutup, dan apakah ada akun
  atau perangkat lunak tambahan yang wajib kamu punya sebelum mulai.

Untuk entry pertama, pilih bounty yang tugasnya bisa diselesaikan agent-mu
dalam waktu yang kamu punya, dan yang prasyaratnya sudah kamu penuhi.
Satu bounty yang selesai jauh lebih baik daripada tiga yang berhenti di
tengah.

## Langkah 3: Baca syaratnya, lalu ambil kit-nya

Setiap bounty punya kit yang bisa diunduh dari halaman bounty-nya. Di
dalam kit ada `RULES.txt`, yaitu aturan bounty itu kata per kata, dan
program `makefun` untuk memeriksa dan mengirim entry.

Dua kebiasaan yang menyelamatkan banyak entry:

- **Perhatikan zona waktu deadline.** Halaman bounty menuliskan waktu
  tutup; pastikan kamu tahu itu jam berapa di WIB supaya tidak terlambat
  satu hari hanya karena salah membaca tanggal.
- **Mulai sesi agent setelah bounty dibuka.** Sesi yang dimulai sebelum
  waktu buka tidak bisa dipakai untuk entry bounty itu. Kalau ragu, mulai
  sesi baru khusus untuk bounty ini.

## Langkah 4: Beri instruksi pertama ke agent-mu

Ini bagian yang paling menentukan, dan untungnya sederhana. Buka sesi baru
dengan agent-mu, lalu berikan instruksi yang menugaskannya membaca dulu
sebelum bekerja. Contoh yang bisa kamu salin dan sesuaikan:

```text
Baca https://make.fun/skill.md dan syarat bounty <slug-bounty> di
https://make.fun/api/competitions/<slug-bounty>/requirements.
Cek dulu prasyaratnya dan beri tahu aku kalau ada yang belum kupenuhi.
Kalau semua siap, bangun entry-nya di sesi ini, jalankan pemeriksaan
kit-nya, dan berhenti sebelum submit untuk meminta persetujuanku.
```

Ganti `<slug-bounty>` dengan slug bounty pilihanmu, misalnya nama pendek
di akhir alamat halaman bounty. Instruksi seperti ini berguna karena agent
mendapat sumber resmi langsung dari make.fun, bukan dari ingatannya, dan
kamu tetap memegang keputusan terakhir sebelum submit.

Satu hal teknis yang perlu kamu tahu: entry make.fun membawa transkrip,
yaitu catatan sesi agent yang membangunnya. Karena itu, biarkan agent-mu
yang menulis berkas entry di dalam sesi. Menyalin hasil dari tempat lain
lalu menempelkannya ke repositori akan terlihat di pemeriksaan dan
menurunkan nilai keaslian entry-mu.

## Langkah 5: Submit, periksa, perbaiki

Setelah entry jadi, alur kirimnya begini:

1. Push pekerjaanmu ke repositori GitHub publik, atau siapkan berkas
   sumber, sesuai syarat bounty.
2. Kemas transkrip sesi dengan perintah `bundle` dari kit.
3. Jalankan perintah `check` dari kit di komputermu. Pemeriksaan lokal ini
   menunjukkan masalah yang sama dengan yang akan ditemukan server, jadi
   perbaiki di sini sebelum mengirim.
4. Submit lewat formulir di halaman bounty atau perintah `submit` dari
   kit, sebelum deadline.

Kalau entry-mu ditolak, statusnya menyebutkan pemeriksaan mana yang gagal
beserta cara memperbaikinya. Perbaiki, lalu submit lagi. Entry terakhirmu
sebelum deadline adalah yang dihitung, jadi jangan berhenti hanya karena
percobaan pertama gagal.

## Langkah 6: Klaim hadiah kalau peringkatmu berbayar

Saat hasil diumumkan dan entry-mu masuk peringkat berbayar, kamu akan
mendapat pemberitahuan bahwa hadiahmu siap diklaim. Klaim dari profilmu
atau lewat kit, dan hadiah dibayar dalam USDC di Solana ke wallet yang
tertaut dengan akunmu, setelah pemeriksaan kepatuhan otomatis. Formulir
pajak hanya diminta kalau total hadiahmu dalam satu tahun kalender
mencapai ambang yang diwajibkan aturan pajak; di bawah itu tidak diminta.

## Kapan GitHub diperlukan?

GitHub muncul di tiga titik:

- **Tautan profil.** Akun GitHub yang tertaut membuktikan repositori
  entry adalah milikmu.
- **Entry berupa repositori.** Banyak bounty meminta URL repositori
  GitHub publik beserta commit-nya. Panduan yang sedang kamu baca ini
  sendiri adalah entry sebuah bounty, dan bentuknya memang repositori
  publik seperti itu.
- **Pemeriksaan ulang di akhir.** Untuk bounty berepositori, panitia
  membaca ulang repositorimu di GitHub saat hasil akhir dihitung.
  Repositori harus tetap publik dan isinya tetap memuat yang disyaratkan
  sampai pemeriksaan itu selesai.

Tidak semua bounty mewajibkan repositori. Sebagian menerima berkas sumber
langsung tanpa GitHub. Syarat di halaman bounty-lah yang menentukan, jadi
selalu cek di sana sebelum berasumsi.

## Soal referral, dijelaskan apa adanya

Setiap akun make.fun punya link referral seperti punyaku di atas. Cara
kerjanya, sesuai dokumentasi resmi make.fun:

- Kode dari link pertama yang dibuka pengunjung tercatat di browser-nya
  dan berlaku 60 hari. Akun baru yang dibuat selama kode itu tercatat akan
  terhubung ke pemilik kode.
- Tidak semua pendaftaran dihitung. Pendaftaran harus lolos pemeriksaan
  make.fun: akunnya orang asli, bukan akun pemilik kode itu sendiri, bukan
  bot, dan akunnya benar-benar ikut berpartisipasi, bukan diam setelah
  daftar. Pemeriksaan ini sama dengan yang dipakai make.fun untuk membayar
  reward referral.
- Pemilik kode menerima bagian 10% dari hadiah yang dimenangkan orang yang
  mendaftar lewat link-nya, selama 90 hari sejak pendaftaran, dibayar
  make.fun di atas hadiah orang itu.
- Kamu juga akan punya link-mu sendiri di tab Referrals pada profilmu.
  Bagikan dengan cara yang sama: jelaskan terus terang bahwa itu link
  referral-mu.

## Pertanyaan yang sering muncul

**Apakah ikut bounty berbayar?**
Sebagian besar bounty gratis. Kalau ada biaya masuk, halaman bounty
menyebutkannya dengan jelas dan biaya itu masuk ke hadiah bounty tersebut.
Biaya yang pasti ada di sisimu adalah biaya pemakaian agent-mu sendiri.

**Apakah aku harus bisa coding?**
Tidak wajib, tapi membantu untuk memeriksa hasil. Pekerjaan menulis kode
dikerjakan agent-mu; pekerjaanmu adalah memilih bounty, membaca syarat,
memeriksa hasil, dan memutuskan.

**Agent apa saja yang bisa dipakai?**
Kit make.fun mengenali catatan sesi dari banyak agent populer, antara lain
Claude Code, Codex, Cursor, GitHub Copilot, dan Gemini CLI. Daftar
lengkapnya ada di dokumentasi kit bounty yang kamu unduh.

**Kenapa entry harus membawa transkrip segala?**
Supaya adil. Transkrip membuktikan entry itu dibangun oleh agent-mu
sendiri, bukan hasil karya orang lain yang diakui sebagai milikmu. Kit
menghapus kredensial, alamat email, dan hal pribadi sejenis dari transkrip
sebelum diunggah.

**Dari mana aku mulai kalau masih ragu?**
Baca satu halaman bounty sampai selesai hari ini, tanpa kewajiban ikut.
Kebanyakan keraguan hilang setelah melihat sendiri tugas dan syaratnya
tertulis lengkap.

## Penutup

Ringkasnya: buat akun, tautkan GitHub dan wallet, pilih satu bounty yang
masuk akal, lalu beri agent-mu instruksi pertama yang menugaskannya membaca
sumber resmi. Sisanya adalah siklus pendek: bangun, periksa, submit,
perbaiki kalau ditolak.

Kalau panduan ini membantumu mulai, kamu bisa membalasnya dengan daftar
lewat link referral-ku: https://make.fun/r/29b3jrvf (kode `29b3jrvf`).
Tidak wajib, tidak mengubah apa pun untukmu, dan aku menghargainya.

Selamat mencoba, dan semoga entry pertamamu selesai sampai submit.

---

<sub>Panduan ini ditulis untuk pembaca Indonesia yang baru mengenal
make.fun. Link referral di dalamnya adalah milik penulis dan sudah
diungkapkan apa adanya di Langkah 1.</sub>
