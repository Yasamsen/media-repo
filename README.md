✨ Yasam CDN

«High-quality media delivery for images and videos — simple, fast, and reliable.»

---

🌐 Overview

Yasam CDN is a lightweight content delivery system built on top of GitHub’s raw infrastructure, designed for serving images and videos with minimal latency and zero backend complexity.

It provides a clean and predictable way to access media assets for modern applications.

---

⚡ Core Features

- 🚀 Fast Delivery — direct access via GitHub raw CDN
- 🖼️ Image Ready — supports JPG, PNG, WEBP
- 🎥 Video Ready — supports MP4, WEBM, MKV
- 📁 Structured Storage — organized by collection (folder-based)
- 🔗 Direct Linking — usable in HTML, apps, and APIs
- 📄 Per-Folder API — each collection exposes its own JSON endpoint
- 🌍 Global Access — available worldwide

---

📦 Repository Structure

media-repo/
 ├── <collection>/
 │    ├── 000.jpg
 │    ├── 001.png
 │    ├── 002.mp4
 │    └── api.json

Each folder acts as an independent media collection.

---

🔗 Direct Access

🖼️ Image

https://raw.githubusercontent.com/Yasamsen/media-repo/main/<collection>/000.jpg

🎥 Video

https://raw.githubusercontent.com/Yasamsen/media-repo/main/<collection>/002.mp4

---

📄 API Endpoint

https://raw.githubusercontent.com/Yasamsen/media-repo/main/<collection>/api.json

Response Format

{
  "status": true,
  "creator": "yasamDev",
  "total": 3,
  "data": [
    "https://raw.githubusercontent.com/.../000.jpg",
    "https://raw.githubusercontent.com/.../001.png",
    "https://raw.githubusercontent.com/.../002.mp4"
  ]
}

---

💻 Integration

JavaScript

const endpoint = "https://raw.githubusercontent.com/Yasamsen/media-repo/main/fubuki/api.json";

fetch(endpoint)
  .then(res => res.json())
  .then(({ data }) => {
    const random = data[Math.floor(Math.random() * data.length)];
    console.log(random);
  });

---

HTML Image

<img src="https://raw.githubusercontent.com/Yasamsen/media-repo/main/fubuki/000.jpg" />

---

HTML Video

<video controls>
  <source src="https://raw.githubusercontent.com/Yasamsen/media-repo/main/fubuki/002.mp4" type="video/mp4">
</video>

---

⚙️ Performance

- ⚡ Optimized for lightweight to medium workloads
- 🌍 Distributed via GitHub global infrastructure
- 📦 Direct file serving (no redirect layer)

---

⚠️ Considerations

- Public access only (no authentication layer)
- Not intended for large-scale streaming platforms
- Subject to GitHub rate limits

---

🎯 Use Cases

- 🤖 Media source for bots (WhatsApp / Telegram)
- 🌐 Static asset hosting
- 🎌 Anime / image CDN
- 📱 Mobile app media backend

---

👨‍💻 Author

yasamDev

---

💎 Final Note

«Minimal setup. Clean structure. Reliable delivery.»

A practical CDN solution for developers who value simplicity and control.
