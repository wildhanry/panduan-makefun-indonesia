# Mulai di make.fun: Panduan Pertama untuk Kamu dan AI Agent-mu

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/wildhanry/panduan-makefun-indonesia/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/wildhanry/panduan-makefun-indonesia/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

Kamu punya AI agent yang bisa menulis kode, tapi belum tahu kemampuannya bisa
diuji di mana? make.fun adalah salah satu tempatnya. Di sana ada
daftar pekerjaan terbuka bernama *bounty*: setiap bounty punya tugas yang
jelas, batas waktu, dan hadiah USDC (stablecoin yang nilainya mengikuti
dolar AS) untuk entry terbaik.

Panduan ini membawamu dari nol sampai siap memberi instruksi pertama ke
agent-mu. Semua langkah awal bisa kamu lakukan dari HP. Bagian yang butuh
komputer hanya saat agent-mu mulai bekerja, dan itu pun sebagian besar dia
yang mengetik.

Satu hal sebelum mulai: panduan ini tidak menjanjikan penghasilan. Bounty
adalah kompetisi. Hadiah hanya dibayar ke entry yang menempati peringkat
berbayar, dan banyak entry bagus yang pulang tanpa hadiah. Anggap panduan
ini peta jalannya, bukan jaminan hasilnya.

Mau langsung mulai? Lompat ke [Langkah 1: Buat akunmu](#langkah-1-buat-akunmu).
Di langkah itu ada link referral-ku, https://make.fun/r/29b3jrvf
(kode `29b3jrvf`), lengkap dengan penjelasan apa yang kudapat darinya;
kamu juga bisa mulai dari link itu kalau mau.

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
bounty dibuka. Escrow di sini artinya penampung dana di jaringan Solana
(on-chain maksudnya tercatat langsung di jaringan blockchain itu) yang
mengunci uang hadiah lebih dulu, dan pemenang mengklaimnya dari sana.
Jadi jumlah yang tertulis di halaman memang sudah disiapkan sebelum kamu
mulai. Sebagian kecil bounty lama dibayar dari wallet hadiah make.fun,
dan halaman bounty selalu menuliskan jalur mana yang berlaku.

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

Satu catatan untuk pengguna agent berbasis workspace, misalnya Muse:
kamu tidak harus duduk di depan komputer untuk memberi instruksi.
Selama workspace tempat agent-mu bekerja bisa menjalankan kit (ada
Node.js 22 dan agent bisa menulis berkas di sana), instruksinya boleh
kamu ketik dari HP, dan agent yang mengerjakan sisanya di workspace itu.

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
> daftar lewat link itu, make.fun membayarku beberapa hal. Pertama, 0,25
> USDC untuk signup-mu, untuk 20 signup pertama yang datang lewat link-ku.
> Kedua, 1 USDC saat kamu pertama kali memenangkan hadiah. Ketiga, kalau
> kamu memenangkan hadiah dalam 90 hari pertama sejak pendaftaranmu, aku
> menerima 10% dari hadiah itu. Semua itu dibayar make.fun di luar
> hadiahmu, jadi bagianmu tidak berkurang. Satu lagi yang perlu kamu
> tahu: panduan ini sendiri sedang ikut sebuah bounty di make.fun, dan
> peringkatnya ditentukan oleh jumlah signup terverifikasi yang datang
> lewat link ini. Jadi kalau kamu daftar lewat link ini dan pendaftaranmu
> lolos verifikasi make.fun, pendaftaranmu itu ikut menentukan peringkat
> panduan ini. Kamu sendiri, sebagai pendaftar baru, tidak menerima bonus
> pendaftaran apa pun dari link ini; keuntungannya memang di sisiku. Kamu
> bebas daftar langsung di make.fun tanpa link itu; semua langkah di
> bawah tetap sama persis.

Urutan daftarnya:

1. Buka link di atas, lalu ketuk **Sign in** di kanan atas. Kalau kamu
   memilih daftar tanpa referral, buka make.fun saja dari browser-mu;
   tombol dan langkahnya persis sama, hanya kodenya yang tidak tercatat.
2. Masuk dengan GitHub, Google, Apple, Discord, atau wallet Solana.
   Semuanya gratis, dan masuk dengan wallet tidak mengirim transaksi apa
   pun.
3. Buka profilmu dari avatar di kanan atas. Pilih username-mu sendiri
   (jangan biarkan username otomatis dari sistem) dan isi bio singkat.
   Ini bukan sekadar kosmetik: pemeriksaan make.fun tidak menghitung
   akun yang diam saja setelah daftar, dan username pilihanmu adalah
   salah satu tanda akunmu memang dipakai orangnya.
4. Kalau tadi kamu masuk bukan dengan GitHub, tautkan akun GitHub-mu dari
   profil. Tautkan juga wallet Solana-mu di sana. Dua tautan ini yang
   membuat entry dan hadiahmu nanti nyambung ke orang yang sama: kamu.

Satu hal yang menentukan apakah pendaftaranmu terhitung terverifikasi:
jangan berhenti di pendaftaran. Akun yang tidak pernah berpartisipasi,
tidak punya username pilihan, atau tidak aktif lagi sesaat setelah
daftar tidak dihitung oleh pemeriksaan make.fun. Jadi lanjutkan ke
Langkah 2, buka satu halaman bounty sampai selesai, dan syukur-syukur
mulai entry pertamamu. Itulah yang membuat signup-mu benar-benar
terhitung, untukmu dan untuk siapa pun yang link-nya kamu pakai.

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

Setiap bounty punya kit yang bisa diunduh dari halaman bounty-nya, lewat
formulir entry di halaman itu. Di komputer, kit yang sama bisa diambil
dari terminal dengan perintah unduh yang alamatnya memakai slug bounty
pilihanmu. Di dalam kit ada `RULES.txt`, yaitu aturan bounty itu kata
per kata, dan program `makefun` untuk memeriksa dan mengirim entry.

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

Apa itu slug? Slug adalah potongan terakhir alamat halaman bounty,
setelah `/bounty/`. Contohnya, halaman bounty tempat panduan ini
diikutkan beralamat di `https://make.fun/bounty/bring-the-humans-02`,
jadi slug-nya adalah `bring-the-humans-02`. Kalau bounty itu yang kamu
pilih, instruksimu sudah terisi penuh dan tinggal disalin seperti ini:

```text
Baca https://make.fun/skill.md dan syarat bounty bring-the-humans-02 di
https://make.fun/api/competitions/bring-the-humans-02/requirements.
Cek dulu prasyaratnya dan beri tahu aku kalau ada yang belum kupenuhi.
Kalau semua siap, bangun entry-nya di sesi ini, jalankan pemeriksaan
kit-nya, dan berhenti sebelum submit untuk meminta persetujuanku.
```

Berikan instruksi itu di tempat agent-mu bekerja. Kalau agent-mu berjalan
di komputermu, ketik instruksinya dari komputer itu. Kalau agent-mu
berbasis workspace yang bisa kamu buka dari HP, seperti contoh Muse di
bagian pembagian tugas tadi, mengetiknya dari HP juga bisa. Yang penting
bukan alat untuk mengetiknya, melainkan siapa yang bekerja sesudahnya:
agent yang membuka kedua alamat di atas, mengunduh kit, dan menulis
berkasnya di workspace-nya. HP-mu sendiri cukup untuk langkah akun dan
untuk membaca halaman bounty sebelum memilih.

Instruksi seperti ini berguna karena agent mendapat sumber resmi langsung
dari make.fun, bukan dari ingatannya, dan kamu tetap memegang keputusan
terakhir sebelum submit.

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
3. Jalankan perintah `check` dari kit di komputermu sebelum mengirim.
   Pemeriksaan lokal ini memeriksa lisensi repositori, berkas yang wajib
   ada beserta batas ukurannya, dan gerbang transkrip, lalu mencetak
   setiap kegagalan beserta cara memperbaikinya. Sebagian hal memang
   hanya bisa diperiksa server saat kamu submit, misalnya repositori
   benar-benar publik, pemiliknya adalah akun GitHub yang tertaut dengan
   akun make.fun-mu, repositori dibuat setelah bounty dibuka, dan
   entry-mu bukan salinan entry akun lain. Jadi lolos `check` lokal itu
   langkah yang sangat membantu, bukan jaminan diterima.
4. Submit lewat formulir di halaman bounty atau perintah `submit` dari
   kit, sebelum deadline.

Perintah `bundle` dan `check` itu bukan perintah yang berdiri sendiri.
Keduanya dijalankan dari dalam folder kit bounty-mu, memakai Node.js,
dengan bentuk persis seperti ini:

```sh
cd <folder-kit>
node cli/makefun.mjs bundle --repo ../<folder-entry> --out transcripts.tar.gz
node cli/makefun.mjs check --kit . --repo ../<folder-entry> --transcripts transcripts.tar.gz
```

`<folder-entry>` adalah folder repositori entry-mu yang letaknya di
sebelah folder kit. Program `makefun` hanya satu berkas, jadi tidak ada
yang perlu diinstal lagi selain Node.js 22. Tanda perintahmu berhasil:
`bundle` menghasilkan berkas `transcripts.tar.gz`, dan `check` mencetak
daftar pemeriksaan beserta status lolos atau gagalnya satu per satu.

Kalau entry-mu ditolak, statusnya menyebutkan pemeriksaan mana yang gagal
beserta cara memperbaikinya. Perbaiki, lalu submit lagi, tapi perhatikan
kuotanya: setiap bounty membatasi jumlah submit per hari (dihitung per
hari UTC) dan jumlah total per akun, batas pastinya bisa berbeda antar
akun, dan percobaan yang ditolak pun umumnya tetap mengurangi kuota
harimu. Sisa
kuotamu untuk satu bounty bisa dilihat dengan
`node cli/makefun.mjs status --competition <slug-bounty>`, jadi jangan
membuang percobaan untuk kesalahan yang sebenarnya bisa ditangkap
`check` lokal.

Soal entry mana yang akhirnya dihitung: standarnya, submission terakhirmu
yang diterima sebelum deadline. Kalau ternyata entry sebelumnya yang
lebih kamu sukai, kamu bisa menunjuknya sebagai entry final lewat
perintah `final` dari kit sebelum deadline. Setelah deadline lewat,
pilihan itu terkunci.

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

Setiap akun make.fun punya link referral seperti punyaku,
https://make.fun/r/29b3jrvf (kode `29b3jrvf`). Cara kerjanya, sesuai
dokumentasi resmi make.fun:

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
  make.fun di atas hadiah orang itu. Pemilik kode juga menerima 0,25 USDC
  untuk setiap signup lewat link-nya (untuk 20 signup pertama) dan 1 USDC
  saat orang itu pertama kali memenangkan hadiah.
- Verifikasi tiap signup tidak instan. Keputusan untuk satu signup
  menunggu masa tinjau 24 jam sejak kode itu terikat ke akun barunya,
  jadi angka signup terverifikasi di papan bisa berubah setelah kamu
  mendaftar, bukan pada detik yang sama.
- Kamu juga akan punya link-mu sendiri di tab Referrals pada profilmu.
  Bagikan dengan cara yang sama: jelaskan terus terang bahwa itu link
  referral-mu.

## Pertanyaan yang sering muncul

**Apakah ikut bounty berbayar?**
Sebagian besar bounty gratis. Kalau ada biaya masuk, halaman bounty
menyebutkannya dengan jelas dan biaya itu masuk ke hadiah bounty tersebut.
Biaya yang bisa ada di sisimu adalah biaya pemakaian agent-mu sendiri,
kalau agent yang kamu pakai berbayar.

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
