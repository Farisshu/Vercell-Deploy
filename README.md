# Embedded Study Hub 🎯

Web app pribadi untuk belajar dan mengorganisir materi embedded systems (CAN, SPI, FreeRTOS, MISRA-C, dll).

## 🚀 Quick Start

### Local Development

```bash
# Install dependencies
npm install

# Run development server
npm run dev

# Build for production
npm run build

# Start production server
npm start
```

### Deploy to Vercel (3 klik!)

1. Push code ke GitHub repository
2. Buka [vercel.com](https://vercel.com)
3. Import repository → Deploy otomatis!

## 📁 Struktur Folder

```
embedded-study-hub/
├── app/                    # Next.js App Router
│   ├── layout.tsx         # Root layout + theme
│   ├── page.tsx           # Dashboard utama
│   ├── study/[slug]/      # Halaman materi
│   ├── progress/          # Tracking progress
│   └── settings/          # Pengaturan
├── content/               # Markdown files
│   ├── protocols/         # CAN, SPI, Modbus
│   ├── rtos/             # FreeRTOS
│   ├── toolchain/        # PlatformIO, Git
│   └── japanese/         # Istilah teknis JP
├── components/            # UI components
├── lib/                   # Utilities
└── public/               # Static assets
```

## 📝 Cara Tambah Materi Baru

### 1. Buat folder konten

```bash
content/protocols/nama-topik/
├── index.md              # Konten utama (EN)
├── index.ja.md          # Versi Jepang (optional)
└── quiz.json            # Quiz (optional)
```

### 2. Template Markdown

```markdown
---
title: "Nama Topik"
category: "protocols"
tags: ["can", "embedded", "communication"]
level: "Beginner"
estimatedTime: 30
status: "Not Started"
---

## Overview

Penjelasan singkat tentang topik ini.

## Details

### Sub-topic 1

Konten dengan support:

- Code blocks dengan syntax highlighting
- Diagram Mermaid
- Gambar dan video embed

\`\`\`c
// Contoh kode C
void setup() {
  // initialization
}
\`\`\`

### Diagram Example

\`\`\`mermaid
graph TD
    A[Start] --> B[Process]
    B --> C[End]
\`\`\`
```

### 3. Template Quiz (quiz.json)

```json
{
  "questions": [
    {
      "question": "Pertanyaan?",
      "options": ["A", "B", "C", "D"],
      "correct": 0,
      "explanation": "Penjelasan jawaban"
    }
  ]
}
```

## 🎨 Fitur

### 📚 Dashboard Materi
- Navigasi per kategori
- Filter by status, level, tag
- Search global
- Progress tracking

### 📝 Content Viewer
- Markdown rendering
- Syntax highlighting (C/C++, Python, bash)
- Mermaid diagrams
- Code copy button

### 🎮 Interactive Learning
- Checklist per sub-topik
- Quiz multiple choice
- Progress bar
- Badge system

### 🌐 Japanese Support
- Toggle EN/JP
- Furigana support
- Bilingual content ready

## 💾 Data Storage

- **Default**: localStorage (browser-based)
- **Optional**: Supabase (sync antar device)

### Export/Import Progress

Di halaman Settings, bisa export progress sebagai JSON untuk backup.

## 🎯 Roadmap

- [x] Basic structure & dashboard
- [x] Content viewer dengan Markdown
- [x] Quiz system
- [x] Progress tracking
- [ ] Supabase integration
- [ ] PWA offline support
- [ ] Text-to-speech untuk JP
- [ ] Auto-link ke GitHub repos

## 📊 Tech Stack

- **Framework**: Next.js 14 (App Router)
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **Markdown**: remark + rehype
- **Diagrams**: Mermaid.js
- **Deploy**: Vercel

## 🙏 Credits

Dibuat untuk persiapan intern di HORIBA Kyoto - Software Design Dept.

---

**Happy Learning! 🇯🇵✨**
