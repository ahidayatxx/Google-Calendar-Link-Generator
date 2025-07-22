# Claude Project: Generator Link Google Calendar 📅

> **Generator link Google Calendar otomatis dengan dukungan acara berulang untuk Claude AI, ChatGPT, dan Google Gemini**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Indonesian](https://img.shields.io/badge/Language-Indonesian-red.svg)](README.md)
[![Claude Project](https://img.shields.io/badge/Claude-Project-orange.svg)](https://claude.ai)
[![ChatGPT](https://img.shields.io/badge/ChatGPT-Project-green.svg)](https://chatgpt.com)
[![Gemini](https://img.shields.io/badge/Google-Gemini-blue.svg)](https://gemini.google.com)

## 📖 Deskripsi

Project ini memungkinkan AI assistant (Claude, ChatGPT, atau Google Gemini) untuk secara otomatis membuat link Google Calendar yang dapat langsung diklik berdasarkan informasi acara yang diberikan pengguna. Mendukung **acara berulang** dengan berbagai pola pengulangan seperti mingguan, bulanan, harian, dan tahunan.

### ✨ Fitur Utama

- 🔗 **Generate link Google Calendar otomatis** yang dapat langsung diklik
- 🔄 **Dukungan acara berulang lengkap** (mingguan, bulanan, harian, tahunan)
- 🌏 **Konversi zona waktu otomatis** (WIB, WITA, WIT ke UTC)
- 📝 **URL encoding otomatis** untuk semua parameter
- ⏰ **Instruksi pengaturan reminder manual**
- 🎯 **Template respons yang konsisten**
- 📱 **Kompatibel dengan desktop dan mobile**

### 🎯 Contoh Penggunaan

**Input:**
```
Standup meeting setiap hari Senin jam 9 pagi selama 30 menit, sampai akhir tahun 2025
```

**Output:**
```
📅 Link Google Calendar (Acara Berulang)

Klik link berikut untuk menambahkan ke kalender:
https://calendar.google.com/calendar/render?action=TEMPLATE&text=Standup%20Meeting&dates=20250721T020000Z/20250721T023000Z&details=Standup%20meeting%20rutin%20setiap%20hari%20Senin%0ASampai%3A%2031%20Desember%202025&recur=RRULE:FREQ=WEEKLY;BYDAY=MO;UNTIL=20251231T235959Z

Detail Acara:
• Judul: Standup Meeting
• Waktu: 09:00 - 09:30 WIB
• Pengulangan: Setiap hari Senin
• Berakhir: 31 Desember 2025
```

## 🚀 Cara Penggunaan

### 1. Claude AI (Anthropic)

1. Buka [Claude.ai](https://claude.ai)
2. Buat **Project** baru
3. Copy isi file [`claude-project-instructions.md`](claude-project-instructions.md) ke **Project Instructions**
4. Simpan project
5. Mulai chat dengan memberikan informasi acara

### 2. ChatGPT (OpenAI)

1. Buka [ChatGPT](https://chatgpt.com)
2. Buat **Custom GPT** baru atau gunakan **Project**
3. Copy isi file [`chatgpt-custom-instructions.md`](chatgpt-custom-instructions.md) ke **Instructions**
4. Upload file [`knowledge-base.md`](knowledge-base.md) sebagai **Knowledge**
5. Aktifkan dan mulai gunakan

### 3. Google Gemini

1. Buka [Google Gemini](https://gemini.google.com)
2. Buat **Gem** baru
3. Copy isi file [`gemini-instructions.md`](gemini-instructions.md) ke **Instructions**
4. Simpan Gem
5. Mulai conversation

## 📁 Struktur File

```
📦 claude-gcal-generator/
├── 📄 README.md                           # File ini
├── 📄 LICENSE                             # Lisensi MIT
├── 📂 claude/
│   ├── 📄 claude-project-instructions.md  # Instruksi untuk Claude Project
│   └── 📄 claude-examples.md             # Contoh penggunaan Claude
├── 📂 chatgpt/
│   ├── 📄 chatgpt-custom-instructions.md # Instruksi untuk Custom GPT
│   ├── 📄 knowledge-base.md              # Knowledge base
│   └── 📄 chatgpt-examples.md            # Contoh penggunaan ChatGPT
├── 📂 gemini/
│   ├── 📄 gemini-instructions.md         # Instruksi untuk Google Gemini
│   └── 📄 gemini-examples.md             # Contoh penggunaan Gemini
├── 📂 docs/
│   ├── 📄 url-encoding-guide.md          # Panduan URL encoding
│   ├── 📄 timezone-conversion.md         # Panduan konversi zona waktu
│   ├── 📄 rrule-patterns.md              # Pola RRULE untuk pengulangan
│   └── 📄 troubleshooting.md             # Panduan troubleshooting
├── 📂 examples/
│   ├── 📄 single-events.md               # Contoh acara tunggal
│   ├── 📄 recurring-events.md            # Contoh acara berulang
│   └── 📄 advanced-patterns.md           # Pola pengulangan lanjutan
└── 📂 tests/
    ├── 📄 test-cases.md                  # Test cases
    └── 📄 validation-checklist.md       # Checklist validasi
```

## 🔧 Pola Pengulangan yang Didukung

### 📅 Mingguan
- Setiap hari tertentu (Senin, Selasa, dll.)
- Interval mingguan (setiap 2 minggu, dll.)

### 📆 Bulanan
- **Tanggal tetap:** Setiap tanggal 15, tanggal 10, dll.
- **Minggu tertentu:** Rabu minggu ke-2, Jumat terakhir, dll.

### 🗓️ Harian
- Setiap hari
- Interval harian (setiap 2 hari, setiap 3 hari)

### 📊 Tahunan
- Ulang tahun, hari raya
- Tanggal penting tahunan

### 🎯 Interval Khusus
- Bi-weekly (dua mingguan)
- Quarterly (triwulanan)
- Custom interval

## 🌏 Zona Waktu yang Didukung

| Zona Waktu | Keterangan | Konversi ke UTC |
|------------|------------|-----------------|
| **WIB** | Waktu Indonesia Barat | UTC+7 → UTC-7 |
| **WITA** | Waktu Indonesia Tengah | UTC+8 → UTC-8 |
| **WIT** | Waktu Indonesia Timur | UTC+9 → UTC-9 |

## 📱 Contoh Penggunaan Lengkap

### Acara Tunggal
```
Input: "Meeting dengan klien besok jam 2 siang selama 1.5 jam di kantor Jakarta"
Output: Link Google Calendar dengan detail lengkap
```

### Acara Mingguan
```
Input: "Standup meeting setiap Senin jam 9 pagi sampai akhir tahun"
Output: Link dengan RRULE mingguan
```

### Acara Bulanan
```
Input: "Rapat evaluasi setiap tanggal 15 jam 10 pagi selama 6 bulan"
Output: Link dengan RRULE bulanan tanggal tetap
```

### Acara dengan Google Meet
```
Input: "Meeting online setiap Rabu jam 2 siang dengan Google Meet"
Output: Link dengan lokasi "Google Meet" dan instruksi setup
```

## ⚠️ Keterbatasan dan Solusi

### 🔴 Keterbatasan Parameter URL Google Calendar
- **Parameter reminder tidak reliable** → Solusi: Instruksi pengaturan manual
- **RRULE kompleks kadang tidak berfungsi** → Solusi: Backup instruksi manual
- **Mobile browser berbeda dengan desktop** → Solusi: Instruksi untuk kedua platform

### 🟡 Workaround yang Disediakan
1. **Instruksi pengaturan manual** untuk setiap jenis acara
2. **Multiple format link** (clickable + copy-paste)
3. **Preview jadwal** untuk validasi
4. **Troubleshooting guide** lengkap

## 🛠️ Pengembangan

### Kontribusi
1. Fork repositori ini
2. Buat branch untuk fitur baru (`git checkout -b fitur-baru`)
3. Commit perubahan (`git commit -am 'Tambah fitur baru'`)
4. Push ke branch (`git push origin fitur-baru`)
5. Buat Pull Request

### Testing
- Jalankan test cases di folder `tests/`
- Validasi dengan checklist yang disediakan
- Test di berbagai browser dan device

### Roadmap
- [ ] Dukungan Google Workspace
- [ ] Template acara preset
- [ ] Integrasi dengan aplikasi kalendar lain
- [ ] API endpoint untuk integrasi
- [ ] Mobile app companion

## 📄 Lisensi

Project ini menggunakan lisensi [MIT](LICENSE) - lihat file LICENSE untuk detail lengkap.

## 🙏 Kontributor

- **[Nama Anda]** - *Initial work* - [@username](https://github.com/username)

Lihat juga daftar [kontributor](https://github.com/username/claude-gcal-generator/contributors) yang berpartisipasi dalam project ini.

## 📞 Dukungan

- 🐛 **Bug Reports:** [GitHub Issues](https://github.com/username/claude-gcal-generator/issues)
- 💡 **Feature Requests:** [GitHub Discussions](https://github.com/username/claude-gcal-generator/discussions)

## 🔗 Link Terkait

- [Dokumentasi Google Calendar API](https://developers.google.com/calendar)
- [RFC 5545 - iCalendar](https://tools.ietf.org/html/rfc5545)
- [RRULE Generator Tool](https://icalendar.org/rrule-tool.html)
- [Claude AI Projects](https://claude.ai/projects)
- [ChatGPT Custom GPTs](https://chat.openai.com/gpts)
- [Google Gemini](https://gemini.google.com)

---

**Dibuat dengan ❤️ untuk komunitas Indonesia** 🇮🇩

> **Tips:** Star ⭐ repositori ini jika berguna untuk Anda!
