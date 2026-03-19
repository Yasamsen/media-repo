🚀 Yasam CDN

«Simple • Fast • Auto Media CDN powered by GitHub»

"GitHub repo size" (https://img.shields.io/github/repo-size/Yasamsen/media-repo?color=blue)
"GitHub stars" (https://img.shields.io/github/stars/Yasamsen/media-repo?style=social)
"GitHub forks" (https://img.shields.io/github/forks/Yasamsen/media-repo?style=social)

---

🌐 Overview

Yasam CDN adalah sistem CDN sederhana berbasis GitHub yang dirancang untuk:

- 📡 Menyimpan media (image & video)
- ⚡ Menyediakan API JSON otomatis
- 🔄 Pipeline otomatis (download → compress → upload → API)
- 🚀 Performa cepat dengan parallel processing

Cocok untuk:

- Bot WhatsApp 🤖
- Website gallery 🌐
- API anime / waifu 🎌
- Backend ringan ⚡

---

🎯 Features

📥 Smart Downloader

- Auto detect semua link dari JSON (nested support)
- Parallel download (multi-thread)
- Retry otomatis jika gagal
- Skip file rusak / kosong

---

🗜️ Smart Compressor

- 🖼️ Image: resize + optimize (ImageMagick)
- 🎥 Video: compress (FFmpeg)
- Menurunkan size tanpa kehilangan kualitas signifikan

---

📤 Auto Uploader

- Upload ke GitHub via API
- Rename otomatis (000, 001, 002...)
- Anti duplicate & anti overwrite
- Support image & video

---

📄 Auto API Generator

- Generate "api.json" per folder
- Update otomatis setiap upload
- Format clean & siap dipakai

---

🗑️ Folder Manager

- Delete folder recursive
- Hapus semua file + api.json
- Clean tanpa sisa

---

⚡ Repository Structure

media-repo/
 ├── fubuki/
 │    ├── 000.png
 │    ├── 001.png
 │    └── api.json
 ├── images/
 │    ├── 000.jpg
 │    └── api.json

---

🌐 API Example

Contoh endpoint:

https://raw.githubusercontent.com/Yasamsen/media-repo/main/fubuki/api.json

---

📄 API Response

{
  "status": true,
  "creator": "yasamDev",
  "total": 5,
  "data": [
    "https://raw.githubusercontent.com/.../000.jpg",
    "https://raw.githubusercontent.com/.../001.jpg"
  ]
}

---

⚙️ Installation (Termux)

pkg update && pkg upgrade -y
pkg install jq curl imagemagick ffmpeg util-linux -y

---

🚀 Usage

1️⃣ Download Media dari JSON

./download.sh

---

2️⃣ Upload ke GitHub

./tool.sh

---

3️⃣ Delete Folder

./tool.sh

---

🔐 Configuration

Edit konfigurasi di script:

TOKEN="your_github_token"
OWNER="username"
REPO="repository"
BRANCH="main"

---

⚡ Performance

- 🚀 Parallel download (multi-thread)
- 🧠 Smart filtering & validation
- 📦 Compression otomatis
- ⚡ Optimized untuk penggunaan mobile (Termux)

---

💡 Use Cases

- CDN anime / waifu image 🎌
- Backend API bot WhatsApp 🤖
- Storage gratis berbasis GitHub 💾
- Web gallery ringan 🌐
- Media hosting alternatif ⚡

---

⚠️ Notes

- Gunakan GitHub Token dengan akses "repo"
- Hindari thread terlalu besar (rate limit)
- Gunakan compress sesuai kebutuhan kualitas

---

🛠️ Tech Stack

- Bash Script 🖥️
- jq (JSON Parser)
- curl (HTTP Client)
- ImageMagick (Image Processing)
- FFmpeg (Video Processing)

---

🔮 Future Plans

- 🎲 Random API endpoint ("/random")
- 🌐 Web dashboard (upload UI)
- 📊 Statistik & monitoring
- 🧠 Smart AI compression
- 📁 Multi-repo CDN system

---

👨‍💻 Author

Made with ❤️ by yasamDev

---

⭐ Support

Kalau project ini membantu:

- ⭐ Star repository
- 🍴 Fork project
- 🚀 Share ke teman

---

🔥 Final Words

«Build your own CDN with zero cost, full control, and high performance 😳✨»

---
