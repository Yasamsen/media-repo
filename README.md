Yasam CDN

Minimalist, high-availability media CDN built on top of GitHub raw delivery.
Designed for fast distribution of images and videos with a simple, predictable structure.

---

Overview

Yasam CDN provides a lightweight approach to serving static media assets using GitHub as the storage layer and global delivery backbone.

It is suitable for:

- Frontend applications (web & mobile)
- Chat bot integrations
- Static websites & landing pages
- Media-based APIs

---

Key Characteristics

- Stateless delivery — direct access via raw URLs
- Structured storage — deterministic file naming
- Per-folder API — each collection exposes its own JSON index
- Globally accessible — served through GitHub infrastructure
- Zero backend required — no server-side runtime

---

Repository Layout

media-repo/
 ├── <collection>/
 │    ├── 000.jpg
 │    ├── 001.png
 │    ├── 002.mp4
 │    └── api.json

Each directory represents a logical collection of media.

---

Direct Asset Access

Image

https://raw.githubusercontent.com/Yasamsen/media-repo/main/<collection>/000.jpg

Video

https://raw.githubusercontent.com/Yasamsen/media-repo/main/<collection>/002.mp4

These URLs are publicly accessible and can be embedded directly in applications.

---

Collection API

Each folder exposes an index:

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

Integration Examples

HTML (Image)

<img src="https://raw.githubusercontent.com/Yasamsen/media-repo/main/fubuki/000.jpg" />

HTML (Video)

<video controls>
  <source src="https://raw.githubusercontent.com/Yasamsen/media-repo/main/fubuki/002.mp4" type="video/mp4">
</video>

JavaScript

const endpoint = "https://raw.githubusercontent.com/Yasamsen/media-repo/main/fubuki/api.json";

fetch(endpoint)
  .then(res => res.json())
  .then(({ data }) => {
    console.log(data);
  });

---

Performance Notes

- GitHub raw endpoints are globally cached
- Suitable for low to medium traffic workloads
- Latency depends on user proximity to GitHub edge nodes
- No guaranteed SLA (not a dedicated CDN service)

---

Best Practices

- Use optimized formats:
  - Images → "webp", "jpg"
  - Video → "mp4 (H.264)"
- Keep file sizes reasonable (<5MB recommended)
- Organize assets by logical grouping (per folder)
- Avoid frequent overwrites (prefer append-only pattern)

---

Limitations

- Rate limiting may apply under heavy usage
- Not intended for large-scale streaming
- No signed URLs / access control
- Public-only access model

---

Use Cases

- Media API for bots (WhatsApp / Telegram)
- Static asset hosting for frontend apps
- Lightweight image/video CDN
- Public dataset distribution

---

Author

yasamDev

---

License

This project uses GitHub as a storage and delivery layer.
Ensure your content complies with GitHub Terms of Service.

---

Summary

A simple, deterministic approach to serving media:

- predictable structure
- direct access
- no infrastructure overhead

«Practical CDN alternative for small to medium-scale projects.»
