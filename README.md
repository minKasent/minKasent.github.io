# Nguyễn Đăng Khoa (@minKasent) — Dual-Mode Living System Portfolio

Trang Portfolio cá nhân được thiết kế theo triết lý **"Living System Architecture"** — kết hợp giữa **Recruiter Mode** (Bento Grid hiện đại, đọc nhanh trong 15 giây) và **Engineer Mode** (Sơ đồ Kiến trúc Hệ thống tương tác, mô phỏng luồng dữ liệu & KhoaOS CLI Terminal).

---

## ✨ Tính năng nổi bật

1. **Dual-Mode Switcher (`Recruiter Mode` ⚡ ↔ `Engineer Mode` 🛠️)**:
   - **Recruiter Mode:** Giao diện Bento Grid sang trọng, làm nổi bật tóm tắt năng lực 15 giây, số liệu thực tế, chứng chỉ quốc tế (Google Cloud Credly, Microsoft Learn, Holopin) và các dự án chủ lực.
   - **Engineer Mode:** Đưa **Interactive System Architecture Explorer** và **KhoaOS CLI Terminal** lên vị trí trung tâm với nền bản vẽ kỹ thuật (Blueprint Grid).
2. **Interactive System Architecture Explorer (`#architecture`)**:
   - Sơ đồ Node-Graph tương tác cho 3 hệ thống thực tế:
     - **PharmaWMS** (`Next.js 16` ↔ `Spring Boot 4.1 Modulith` ↔ `FEFO Engine` ↔ `PostgreSQL 17` ↔ `FastAPI + LightGBM AI`)
     - **Chronos-Dev** (`CLI Interceptor` ↔ `SHA-256 CAS Object Store` ↔ `Flight DAG` ↔ `Time Machine`)
     - **Crypto Exchange** (`Flutter 60/120FPS UI` ↔ `Pure Dart Domain` ↔ `WebSocket & Secure Storage`)
   - Nhấp vào từng Node để xem chi tiết quyết định kiến trúc (Architecture Decisions), SLA/Benchmark và đoạn code mẫu.
   - Nút **"Mô phỏng Luồng Request" (`Simulate Request Flow`)** chạy hiệu ứng truyền gói tin qua từng tầng kèm log thời gian thực.
3. **Live GitHub Telemetry & Contribution Snake**:
   - Tự động gọi GitHub REST API (`https://api.github.com/users/minKasent`) để lấy số lượng Repositories, Stars, Followers và hiển thị **Contribution Snake SVG** theo chế độ Sáng/Tối.
4. **KhoaOS Interactive Terminal & Command Palette (`Ctrl+K`)**:
   - Hỗ trợ gõ lệnh trực tiếp (`help`, `whoami`, `arch pharmawms`, `arch chronos`, `projects`, `skills`, `certs`, `sudo hire khoa`, `clear`) và hộp thoại tìm kiếm nhanh `Ctrl+K`.
5. **Song ngữ Việt - Anh (`VI` / `EN`) & Giao diện `Dark` / `Light`**.

---

## 🚀 Chạy dự án ở máy cục bộ (Local Development)

```bash
npm install
npm run dev
```

Mở trình duyệt tại `http://localhost:5173`.

---

## 🌐 Hướng dẫn Deploy lên GitHub Pages & Gắn Domain riêng

Dự án đã được cấu hình sẵn file workflow [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml) và đường dẫn tương đối (`base: './'` trong `vite.config.ts`).

### Bước 1: Đẩy code lên GitHub
```bash
git init
git add .
git commit -m "feat: initial dual-mode living system portfolio"
git branch -M main
git remote add origin https://github.com/minKasent/<ten-repo-cua-ban>.git
git push -u origin main
```

### Bước 2: Bật GitHub Pages
1. Vào **Settings** của repository trên GitHub → chọn mục **Pages** ở menu trái.
2. Tại phần **Build and deployment** → mục **Source**, chọn **GitHub Actions**.
3. Workflow `Deploy Portfolio to GitHub Pages` sẽ tự động chạy và xuất bản trang web của bạn!

### Bước 3: Gắn Custom Domain (nếu bạn dùng tên miền riêng)
1. Tạo thêm một file tên là `CNAME` đặt trong thư mục `public/CNAME` chứa tên miền của bạn (ví dụ: `khoanguyen.dev`).
2. Trong trang quản trị DNS của tên miền, trỏ bản ghi `CNAME` về `minkasent.github.io` (hoặc 4 IP chuẩn của GitHub Pages).
3. Nhập tên miền vào ô **Custom domain** trong **Settings → Pages** của GitHub và bật **Enforce HTTPS**.
