# 🚀 HỆ THỐNG TRANG BÌNH CHỌN 1-CHẠM & TỰ ĐỘNG COPY HASHTAG (TRÁNH CHẶN LINK FACEBOOK)

Dự án này được thiết kế riêng để giải quyết vấn đề: **Gửi link Facebook trực tiếp qua tin nhắn / bình luận bị Facebook chặn (Spam Flag)**.

Giải pháp: Sử dụng một trang đích trung gian (Landing page) có gắn mã QR. Khi người bình chọn quét mã QR hoặc bấm vào link:
1. Hệ thống hiển thị thông tin thí sinh / bài dự thi uy tín, rõ ràng.
2. Có **1 NÚT DUY NHẤT** ("BÌNH CHỌN NGAY"):
   - Tự động sao chép toàn bộ Hashtag & Mã dự thi vào clipboard (bộ nhớ tạm).
   - Tự động mở bài viết Facebook (ưu tiên bật App Facebook trên điện thoại).
   - Người dùng chỉ cần ấn Like -> Share công khai và Dán (Paste) là xong!

---

## 📁 Cấu Trúc Thư Mục

```text
Binh chon/
├── index.html        # Trang giao diện bình chọn chính (Tối ưu 100% cho mobile)
├── config.js         # File cấu hình thông tin (Tên thí sinh, Link FB, Hashtag, SBD)
├── qr-tool.html      # Công cụ tạo Poster & Mã QR để in hoặc đăng story
└── README.md         # Hướng dẫn chi tiết
```

---

## ⚙️ Hướng Dẫn Cấu Hình (Chỉ cần sửa file `config.js`)

Mở file [config.js](file:///e:/Code/Web/Binh%20chon/config.js) bằng bất kỳ trình soạn thảo nào và cập nhật các trường:

```javascript
const VOTE_CONFIG = {
  // 1. Tên cuộc thi
  contestName: "CUỘC THI BÌNH CHỌN ẢNH ĐẸP 2026",
  
  // 2. Thông tin thí sinh
  candidateName: "Nguyễn Văn A",
  candidateId: "SBD: 1234",
  candidateRole: "Thí sinh bảng A",
  
  // 3. Ảnh đại diện thí sinh (có thể để link ảnh hoặc tên file ảnh cùng thư mục)
  avatarUrl: "https://... hoặc anh-thi-sinh.jpg",
  
  // 4. Đường link bài viết Facebook cần vote
  facebookPostUrl: "https://www.facebook.com/...",

  // 5. Nội dung & Hashtag cần TỰ ĐỘNG COPY khi bấm nút
  copyContent: `#BinhChon2026 #ThiSinh1234 #NguyenVanA #CuocThiAnhDep
Tôi bình chọn cho thí sinh Nguyễn Văn A - SBD 1234!`,

  // 6. Tên hiển thị trên nút bấm chính
  ctaButtonText: "BÌNH CHỌN NGAY (Mở FB & Copy Hashtag)"
};
```

---

## 🌐 Cách Đưa Trang Web Lên Mạng Miễn Phí (Trong 1 Phút)

Vì đây là web tĩnh siêu nhẹ (HTML/CSS/JS thuần), bạn có thể đưa lên mạng hoàn toàn miễn phí mà không cần thuê hosting:

### Cách 1: Vercel (Khuyên dùng - Nhanh nhất)
1. Cài Vercel CLI (nếu chưa có): `npm install -g vercel`
2. Mở terminal tại thư mục này và chạy: `vercel`
3. Chọn các tùy chọn mặc định (`Enter` liên tục), trong 20 giây bạn sẽ có đường link dạng `https://binhchon-xyz.vercel.app`.

### Cách 2: Netlify Drop (Không cần gõ lệnh)
1. Truy cập: [https://app.netlify.com/drop](https://app.netlify.com/drop)
2. Kéo thả cả thư mục `Binh chon` vào ô tải lên.
3. Netlify sẽ cấp ngay 1 đường link miễn phí hoạt động 24/7.

### Cách 3: Cloudflare Pages hoặc GitHub Pages
- Tạo repository trên GitHub và bật GitHub Pages trong phần Settings -> Pages.

---

## 📱 Cách Lấy Mã QR & Poster Để Gửi Cho Mọi Người

1. Sau khi đưa web lên mạng và có đường link (ví dụ: `https://ten-ban.vercel.app`).
2. Mở file [qr-tool.html](file:///e:/Code/Web/Binh%20chon/qr-tool.html) trên trình duyệt.
3. Dán đường link web của bạn vào ô **URL**.
4. Bấm **Cập nhật xem trước** -> Bấm **Tải ảnh Poster** hoặc **Chỉ tải QR**.
5. Gửi ảnh QR này cho bạn bè, người thân qua Zalo, Messenger, đăng bài Facebook hoặc Story. Quét QR sẽ không bao giờ bị Facebook chặn!
