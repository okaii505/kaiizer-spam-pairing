# KAIIZER Pairing Tools

> WhatsApp spam pairing code tool dengan 2 tema terminal (Normal & Hacker). Developer: **kaiitezy official**

![Version](https://img.shields.io/badge/version-2.1.0-brightgreen)
![Node](https://img.shields.io/badge/node-%3E%3D16.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Platform](https://img.shields.io/badge/platform-termux%20%7C%20linux%20%7C%20windows-lightgrey)

---

## Daftar Isi

- [Tentang](#tentang)
- [Fitur](#fitur)
- [Daftar Tema](#daftar-tema)
- [Preview](#preview)
- [Persyaratan](#persyaratan)
- [Instalasi](#instalasi)
- [Cara Pakai](#cara-pakai)
- [Struktur Project](#struktur-project)
- [Troubleshooting](#troubleshooting)
- [FAQ](#faq)
- [Lisensi](#lisensi)
- [Kontak](#kontak)

---

## Tentang

**KAIIZER Pairing Tools** adalah tools CLI (Command Line Interface) berbasis Node.js untuk mengirim **spam pairing code** ke nomor WhatsApp. Tools ini punya tampilan terminal yang bersih dan modern, dilengkapi **2 tema** (Normal dan Hacker), progress bar real-time, dan efek matrix rain untuk tema Hacker.

Semua dependency akan **otomatis ter-install** kalau belum ada, jadi lo ga perlu install manual satu-satu. Cukup jalankan, dan tools langsung siap dipakai.

---

## Fitur

- **2 Tema Terminal** — Normal (biru/cyan, bersih) dan Hacker (hijau, matrix)
- **Banner KAIIZER** — Tampil di setiap menu dengan warna sesuai tema
- **Spam Pairing Code** — Kirim pairing code berulang (max 20x per sesi)
- **Progress Bar Real-time** — Tampilan progress persentase saat proses spam
- **Matrix Rain Effect** — Efek hujan karakter ala The Matrix untuk tema Hacker
- **Auto-Install Dependency** — Module yang belum ada langsung di-install otomatis
- **Session Auto-Cleanup** — Folder session otomatis dihapus setelah selesai
- **Baileys Banner** — Banner library Baileys tetap muncul saat init socket

---

## Daftar Tema

| No | Nama Tema | Warna Utama | Efek Khusus |
|----|-----------|-------------|-------------|
| 1 | Normal | Biru / Cyan | - |
| 2 | Hacker | Hijau terminal | Matrix rain |

---

## Preview

```
  ██╗  ██╗ █████╗ ██╗██╗███████╗███████╗██████╗ 
  ██║ ██╔╝██╔══██╗██║██║╚══███╔╝██╔════╝██╔══██╗
  █████╔╝ ███████║██║██║  ███╔╝ █████╗  ██████╔╝
  ██╔═██╗ ██╔══██║██║██║ ███╔╝  ██╔══╝  ██╔══██╗
  ██║  ██╗██║  ██║██║██║███████╗███████╗██║  ██║
  ╚═╝  ╚═╝╚═╝  ╚═╝╚═╝╚═╝╚══════╝╚══════╝╚═╝  ╚═╝

  ╔═══════════════════════════════════════════════╗
  ║          KAIIZER PAIRING TOOLS                ║
  ║          Developer : kaiitezy official         ║
  ║          Version   : 2.1.0                     ║
  ╚═══════════════════════════════════════════════╝

  ── MAIN MENU ──

  [1] Spam Pairing Code
  [2] Ganti Tema  (sekarang: normal)
  [0] Keluar
```

---

## Persyaratan

- **Node.js** versi **16.0.0** atau lebih baru
- **npm** (biasanya sudah include sama Node.js)
- Koneksi internet stabil
- Terminal yang support **ANSI color** (Linux, macOS, Windows Terminal, Termux)

---

## Instalasi

### Cara 1 — Clone dari GitHub (direkomendasikan)

```bash
git clone https://github.com/kaiitezy/kaizer-pairing-tools.git
cd kaizer-pairing-tools
npm install
npm start
```

### Cara 2 — Download ZIP

1. Buka repo GitHub
2. Klik tombol **Code** → **Download ZIP**
3. Extract ZIP ke folder mana aja
4. Buka terminal di folder hasil extract
5. Jalankan:

```bash
npm install
npm start
```

### Cara 3 — Install global

```bash
npm install -g kaizer-pairing-tools
kaizer
```

---

## Cara Pakai

### 1. Jalankan tools

```bash
npm start
```

Atau langsung:

```bash
node spam.js
```

### 2. Pilih tema (opsional)

Masuk menu **`[2] Ganti Tema`**, pilih antara:

- **`[1] Normal`** — default, bersih, warna biru/cyan
- **`[2] Hacker`** — hijau terminal + efek matrix rain

### 3. Mulai spam pairing

Masuk menu **`[1] Spam Pairing Code`**, lalu:

1. Masukkan nomor target (contoh: `6281234567890`)
2. Masukkan jumlah spam (max **20**)
3. Konfirmasi dengan `iya` atau `y`
4. Tunggu proses selesai

### 4. Contoh output

```
  Masukkan nomor › 6281234567890
  Masukkan jumlah (max 20) › 4

  Target : 6281234567890
  Jumlah : 4x
  Lanjut? (iya/tidak) › iya

  Proses...

  ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░ 0%  (0/4)
  [1/4] 6281234567890 → YBAJYYCV
  ████████░░░░░░░░░░░░░░░░░░░░░░ 25%  (1/4)
  [2/4] 6281234567890 → NC6NWV7J
  ███████████████░░░░░░░░░░░░░░░ 50%  (2/4)
  [3/4] 6281234567890 → YYKL45TQ
  ███████████████████████░░░░░░░ 75%  (3/4)
  [4/4] 6281234567890 → C7CW1A5H
  ██████████████████████████████ 100%  (4/4)

  Selesai! (ok: 4, gagal: 0)
```

---

## Struktur Project

```
kaizer-pairing-tools/
├── .gitignore
├── LICENSE
├── README.md
├── package.json
└── spam.js
```

| File | Fungsi |
|------|--------|
| `spam.js` | File utama, semua logic tools |
| `package.json` | Manifest project & dependency |
| `README.md` | Dokumentasi (file ini) |
| `LICENSE` | Lisensi MIT |
| `.gitignore` | File yang diabaikan git |

---

## Troubleshooting

### Karakter banner rusak jadi `â–ˆ` / `â•”`

File lo kesave pakai encoding **Windows-1252 / ANSI**, bukan UTF-8. Solusinya:

**VS Code:**
1. Buka file `spam.js`
2. Pojok kanan bawah, klik tulisan `Windows-1252`
3. Pilih **"Save with Encoding"** → **UTF-8**
4. Save (Ctrl+S)

**Notepad++:**
1. Menu **Encoding** → **UTF-8**
2. Save

**Notepad Windows:**
1. **File → Save As**
2. Encoding dropdown → **UTF-8**
3. Save

### Error `Cannot find module 'chalk'`

Jalankan manual:

```bash
npm install chalk@4.1.2
```

Atau langsung:

```bash
npm install
```

### Error `EACCES permission denied` (Linux/Mac)

Jalankan dengan `sudo`:

```bash
sudo npm install -g kaizer-pairing-tools
```

Atau fix permission npm:

```bash
sudo chown -R $(whoami) ~/.npm
```

### Pairing code gagal terus

Beberapa kemungkinan:
- Nomor target salah (harus format internasional, contoh `628xxx`)
- Nomor target belum terdaftar di WhatsApp
- IP lo kena rate limit dari WhatsApp
- Library Baileys versi lama — coba update:

```bash
npm update @whiskeysockets/baileys
```

### Session folder menumpuk

Folder `kaizer_session_*` otomatis dihapus setelah selesai. Kalau ada yang tersisa, hapus manual:

**Linux/Mac:**
```bash
rm -rf kaizer_session_*
```

**Windows (PowerShell):**
```powershell
Remove-Item -Recurse -Force kaizer_session_*
```

---

## FAQ

**Q: Apakah tools ini aman?**
A: Tools ini cuma kirim request pairing code ke WhatsApp lewat library Baileys. Tidak menyimpan data apapun ke server eksternal. Semua proses lokal di komputer lo.

**Q: Apakah nomor target bisa diblokir?**
A: Pairing code yang dikirim cuma request, bukan login. Tapi kalau spam berlebihan, WhatsApp bisa nge-flag aktivitas. Gunakan dengan bijak.

**Q: Bisa spam lebih dari 20?**
A: Bisa, tapi tidak direkomendasikan karena bisa kena rate limit dari WhatsApp. Batas 20 sudah optimal.

**Q: Bisa jalan di Termux?**
A: Bisa. Install Node.js dulu:
```bash
pkg install nodejs
```
Lalu clone & install seperti biasa.

**Q: Bisa jalan di Windows?**
A: Bisa. Pastikan pakai **Windows Terminal** atau **PowerShell** (bukan CMD lama) biar ANSI color tampil sempurna.

**Q: Apakah butuh nomor WhatsApp sendiri?**
A: Tidak. Tools ini cuma kirim pairing code ke nomor target, bukan login pakai nomor sendiri.

**Q: Tema bisa ditambah sendiri?**
A: Bisa. Edit object `themes` di `spam.js`, tambahkan tema baru dengan format yang sama, lalu tambahkan pilihan di `menuTheme()`.

**Q: Session folder `kaizer_session_*` itu apa?**
A: Folder temporary yang dibuat Baileys untuk nyimpen auth state selama proses pairing. Otomatis dihapus setelah selesai.

**Q: Kenapa banner Baileys muncul saat proses?**
A: Itu banner dari library `@whiskeysockets/baileys` yang muncul saat `makeWaSocket()` dipanggil. Banner ini normal dan menandakan library berhasil di-load.

---

## Kontribusi

Kalau mau kontribusi:

1. Fork repo ini
2. Buat branch baru (`git checkout -b fitur-baru`)
3. Commit perubahan (`git commit -m "Tambah fitur baru"`)
4. Push ke branch (`git push origin fitur-baru`)
5. Buat Pull Request

---

## Lisensi

Project ini dilisensikan di bawah **MIT License** — lihat file [LICENSE](LICENSE) untuk detail.

```
MIT License

Copyright (c) 2025 kaiitezy official

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## Kontak

- **Developer:** kaiitezy official
- **GitHub:** [@okaii505](https://github.com/okaii505)
- **Telegram:** [t.me/p1atu](https://t.me/p1atu)

---

<div align="center">

**KAIIZER Pairing Tools** — dibuat dengan sedikit kopi dan banyak bug fix.

Kalau tools ini bermanfaat, jangan lupa kasih **star** di repo ini.

</div>
