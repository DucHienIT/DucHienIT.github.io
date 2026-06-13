# Portfolio — Nguyen Duc Hien

Personal portfolio website (single-page) cho Game Developer **Nguyen Duc Hien**.
Xây dựng bằng **HTML5 + CSS3 + Vanilla JavaScript** — không framework, không build tool. Toàn bộ nằm trong một file `index.html`.

## Xem thử

Mở thẳng `index.html` trên trình duyệt là chạy được ngay.

## Cấu trúc

```
portfolio/
├── index.html        ← toàn bộ HTML + CSS + JS
├── assets/
│   ├── avatar.jpg    ← ảnh profile (tự thêm — vuông, >= 400x400px)
│   └── cv.pdf        ← file CV cho nút Download CV (tự thêm)
└── README.md
```

> Trang tự động dùng `assets/avatar.jpg` nếu có; nếu không sẽ hiện placeholder chữ "NDH".
> Nút **Download CV** trỏ tới `assets/cv.pdf`.

## Tính năng

- Game-inspired dark theme (tím/neon), particle background động bằng Canvas
- Fully responsive (mobile-first, hamburger menu tại breakpoint 768px)
- Scroll-triggered fade-in (IntersectionObserver), smooth scroll, active nav highlight
- Hover effects trên cards & badges

## Deploy lên GitHub Pages

```bash
# 1. Tạo repo trên GitHub (ví dụ tên: portfolio hoặc <username>.github.io)

# 2. Push code
git init
git add .
git commit -m "Initial portfolio"
git remote add origin https://github.com/<username>/<repo>.git
git push -u origin main

# 3. Repo → Settings → Pages → Source: Deploy from branch → main → / (root) → Save

# 4. Truy cập sau ~1 phút:
# https://<username>.github.io/<repo>/
```
