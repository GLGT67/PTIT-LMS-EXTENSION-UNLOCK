# PTIT LMS - Extension Unlock (v2.2.0)

Tiện ích mở rộng và UserScript mở khóa tính năng tua video (YouTube & Video nội bộ Next.js HTML5 môn Triết học BAS1152) trên hệ thống LMS PTIT.

- **Phát triển bởi:** [GLGT67](https://github.com/GLGT67)
- **Kho lưu trữ:** [https://github.com/GLGT67/PTIT-LMS-EXTENSION-UNLOCK](https://github.com/GLGT67/PTIT-LMS-EXTENSION-UNLOCK)

---

## 🎯 Các Tính Năng Nổi Bật

1. **Mở khóa tua video 100%:**
   - Triệt tiêu mã chặn click trên thanh trượt video (`preventDefault()` của React).
   - Ngắt các sự kiện ép giật lùi (Snapback `seeking` / `seeked` về `maxWatched`).
2. **Thanh công cụ HUD tiện lợi nổi trên video:**
   - **⏪ -10s / ⏩ +10s:** Tua nhanh hoặc lùi 10 giây.
   - **⏩ +1m:** Tua nhanh 1 phút.
   - **⚡ 2x / 🚀 5x:** Tăng tốc độ phát video.
   - **🎯 Xong:** Nhảy thẳng đến gần cuối video để hoàn thành bài giảng tức thì.
3. **Phím tắt điều khiển nhanh:**
   - Phím `→` / `←`: Tua tới / lùi 5 giây.
   - Phím `]` / `[` hoặc phím `+` / `-`: Tăng / giảm tốc độ xem (1x đến 16x).
4. **Bảng thông báo (Toast HUD):**
   - Hiển thị trực quan tốc độ và thời gian tua góc trên màn hình.

---

## 🛠 Hướng Dẫn Cài Đặt

### Cách 1: Nạp qua Chrome Extension (Khuyên dùng)
1. Mở Chrome / Edge / Cốc Cốc, truy cập: `chrome://extensions/`
2. Bật công tắc **Chế độ cho nhà phát triển (Developer mode)** ở góc trên cùng bên phải.
3. Bấm vào nút **Tải tiện ích đã giải nén (Load unpacked)** và chọn thư mục chứa mã nguồn này.
4. Truy cập trang bài giảng trên [LMS PTIT](https://lms.ptit.edu.vn/), bấm **F5** để kích hoạt!

### Cách 2: Cài qua Tampermonkey UserScript
1. Cài đặt tiện ích **Tampermonkey** từ Chrome Web Store.
2. Mở file `ptit_lms_unlock.user.js` bằng trình duyệt hoặc sao chép toàn bộ nội dung dán vào script mới trong Tampermonkey.
3. Bấm **Save / Install**. Xong!

---

## 📄 Cấu Trúc Dự Án
```text
├── manifest.json            # Cấu hình Manifest V3 của Chrome Extension
├── content_loader.js        # Content script nạp main.js vào MAIN World
├── main.js                  # Lõi mở khóa video, HUD controls & hotkeys
├── popup.html               # Giao diện popup extension hiển thị phím tắt & trạng thái
├── ptit_lms_unlock.user.js  # Bản UserScript độc lập dành cho Tampermonkey
├── icons/                   # Icon hiển thị của tiện ích
└── README.md                # Tài liệu hướng dẫn sử dụng
```

---

## 👤 Tác Giả & Bản Quyền
- **Developer:** [GLGT67](https://github.com/GLGT67)
- **License:** MIT
