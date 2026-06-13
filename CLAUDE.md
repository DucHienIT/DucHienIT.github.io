# CLAUDE.md — Portfolio Website: Nguyen Duc Hien

## Mục tiêu dự án

Build một **personal portfolio website** dạng single-page (SPA) cho Game Developer Nguyen Duc Hien.
Deploy miễn phí lên **GitHub Pages** tại `https://<username>.github.io`.

---

## Tech Stack

- **HTML5 + CSS3 + Vanilla JavaScript** — không dùng framework, không cần build tool
- Không dùng React, Vue, hay bất kỳ bundler nào (Vite, Webpack...)
- Tất cả gom vào **một file duy nhất**: `index.html`
- Có thể dùng Google Fonts (import qua `<link>`) và Lucide Icons (CDN)

---

## Cấu trúc thư mục sau khi build

```
portfolio/
├── index.html        ← toàn bộ HTML + CSS + JS nằm đây
├── assets/
│   └── avatar.jpg    ← ảnh profile (người dùng tự thêm sau)
└── README.md
```

---

## Thông tin cá nhân (lấy từ CV)

```
Họ tên:     Nguyen Duc Hien
Vai trò:    Game Developer
Ngày sinh:  17/03/2002
Điện thoại: 0948047842
Email:      nguyenduc345345@gmail.com
LinkedIn:   https://www.linkedin.com/in/hiengamedev
Địa chỉ:    Tang Nhon Phu, Ho Chi Minh
```

---

## Nội dung các section (theo thứ tự trên trang)

### 1. Hero / Header
- Tên lớn: **Nguyen Duc Hien**
- Subtitle: `Game Developer · Unity · Mobile`
- Tagline ngắn (lấy từ Career Objective): *"Building scalable, addictive mobile games — growing toward Lead."*
- Nút CTA: `[View Projects]` (scroll đến Projects) và `[Contact Me]` (scroll đến Contact)
- Ảnh avatar tròn (placeholder nếu chưa có ảnh)

### 2. About
- Đoạn giới thiệu ngắn từ Career Objective
- Highlight số liệu nổi bật dạng stat cards:
  - `2+ years` — Professional Experience
  - `2` — Games Shipped (Android + iOS)
  - `1` — Acceleration Program (CrazyLabs)

### 3. Skills
- Hiển thị dạng **tag / badge** có icon:
  - Unity
  - C# / OOP
  - Design Patterns
  - Data Structures & Algorithms
  - Git
  - AI-assisted Coding (Claude)
  - Mobile Optimization (FPS, Memory, Load Time)
  - Troubleshooting & Problem Solving
  - Android & iOS Deploy

### 4. Experience (Timeline)

**IMBA Games** — Game Developer · 07/2023 – Present
- Develop & optimize gameplay features for Hybrid Casual mobile games
- Independently capture & produce CPI marketing videos for prototype games
- Design & implement core mechanics: simple, addictive, scalable
- Build & deploy for Android and iOS
- Optimize performance: FPS, memory usage, loading time
- Collaborate with Game Designers, Artists, Marketing teams

**CrazyHub – CrazyLabs Acceleration Program** · April 2024 – July 2024
- Participated in product acceleration program
- Focus: developing & testing Hybrid Casual game products

### 5. Projects

**State Protector** · July 2025 – August 2025
- Tower defense action game: protect a moving train from enemy waves
- Developed: core gameplay mechanics, enemy AI behaviors, combat systems
- Stack: Unity (C#)
- Optimized performance for mobile; built scalable systems for future content
- AppMagic link: https://appmagic.rocks/iphone/state-protector/6749788490
- Hiển thị dạng **card** có nút `[View on AppMagic →]`

### 6. Education

**Ho Chi Minh City University of Technology and Engineering**
- Ngành: Information Technology · 2020 – 2024
- Tham gia academic competitions và Hackathons

### 7. Contact
- Email: nguyenduc345345@gmail.com
- LinkedIn: https://www.linkedin.com/in/hiengamedev
- Phone: 0948047842
- Nút `[Download CV]` — link đến file PDF CV (người dùng tự thêm sau)

---

## Visual Design

### Phong cách
- **Game-inspired dark theme** — tối, hiện đại, có chút pixel/neon vibe
- Không quá flashy, vẫn đọc được và professional

### Màu sắc
```
--bg-primary:     #0d0f14   (nền chính, gần đen xanh)
--bg-card:        #151820   (card / section nền)
--accent:         #7c3aed   (tím game — primary CTA, highlight)
--accent-glow:    #a855f7   (glow effect, hover)
--text-primary:   #f1f5f9   (text trắng)
--text-secondary: #94a3b8   (text mờ)
--border:         #1e2433   (border nhẹ)
--green:          #22c55e   (badge "Present", status online)
```

### Typography
- **Display / Heading:** `'Space Grotesk'` (Google Fonts) — bold, techy
- **Body:** `'Inter'` (Google Fonts) — clean, readable
- **Code / Tag:** `'JetBrains Mono'` (Google Fonts) — cho skill badges

### Signature element
Một **subtle animated background** ở Hero section: các hạt nhỏ (particle dots) chuyển động chậm bằng Canvas hoặc CSS animation — gợi lên cảm giác game engine / space.

---

## Responsive

- Mobile-first: breakpoint chính tại `768px`
- Navigation: hamburger menu trên mobile
- Cards: 1 cột trên mobile, 2–3 cột trên desktop
- Timeline: full-width trên mobile

---

## Animations / Interactions

- Scroll-triggered **fade-in** cho mỗi section (IntersectionObserver)
- **Smooth scroll** khi click nav links
- Hover effect trên project cards: subtle lift + border glow
- Active nav link highlight khi scroll qua section

---

## Deploy lên GitHub Pages (hướng dẫn cho người dùng)

Sau khi Claude Code sinh ra code, người dùng làm theo các bước:

```bash
# 1. Tạo repo mới trên GitHub tên: <username>.github.io
#    Hoặc bất kỳ tên repo nào, ví dụ: portfolio

# 2. Init git và push
git init
git add .
git commit -m "Initial portfolio"
git remote add origin https://github.com/<username>/<repo>.git
git push -u origin main

# 3. Bật GitHub Pages
# Vào repo → Settings → Pages
# Source: Deploy from branch → main → / (root) → Save

# 4. Truy cập sau ~1 phút tại:
# https://<username>.github.io/<repo>/
```

---

## Những gì KHÔNG làm

- Không dùng backend, database, hay server-side code
- Không dùng npm install hay node_modules
- Không tách file CSS/JS riêng (giữ tất cả trong `index.html` cho đơn giản)
- Không dùng jQuery

---

## Ghi chú cho Claude Code

1. Đọc toàn bộ file `CLAUDE.md` này trước khi viết bất kỳ dòng code nào.
2. Sinh ra **một file duy nhất** `index.html` hoàn chỉnh, có thể mở thẳng trên trình duyệt.
3. Dùng đúng màu sắc, font, và design token đã định nghĩa ở trên.
4. Sau khi sinh xong, tự review lại: mobile responsive, tất cả links đúng, animations hoạt động.
5. Không hỏi thêm — hãy dùng hết thông tin trong file này để build.