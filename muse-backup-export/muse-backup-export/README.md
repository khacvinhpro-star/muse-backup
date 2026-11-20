# Muse Backup — Skill và bộ nhớ của Kevin

Ngày xuất: 2026-11-20, cập nhật cả ngày hôm nay (13:41)
Tài khoản GitHub trong ảnh anh gửi: khacvinhpro-star

Đây là bản sao lưu skill và bộ nhớ dưới dạng file, không phải huấn luyện mô hình.
Tài khoản mới chỉ cần đọc lại các file này là dùng được như cũ.

## Cập nhật ngày 2026-11-20 (có trong bản này)

- GEM KOC Chốt Đơn TikTok nguyên văn, chat phụ riêng `KOC Chốt Đơn TikTok`.
- Kịch bản Dimark theo GEM: bản hay nhất 150 từ theo hook 1, và bản quay tay kiểu Paris 24s rút gọn 74 từ / 340 ký tự.
- Tờ quay tay Dimark 24s 1 trang: thoại 4 cảnh, checklist, caption + bình luận ghim.
- Quy tắc nói giá Dimark: chỉ nói "đang có giảm giá, khuyến mãi" chung chung, không nêu con số / phần trăm / giá thấp hơn giá thật, chỉ dùng khi shop thật sự đang khuyến mãi.
- Hạn chế video: công cụ tạo video báo không khả dụng với tài khoản ở khu vực này, là hạn chế lâu dài, không thử lại. Khi yêu cầu làm video, nói rõ hạn chế này trước, đề xuất làm ảnh / kịch bản thay thế.
- `MEMORY.md` đã cập nhật cả ngày hôm nay, gồm cả yêu cầu đưa lên GitHub này.

## Repo này chứa gì

- `MEMORY.md` — bộ nhớ dài hạn: quy tắc sản phẩm đồng nhất, vật lý, tỉ lệ, mẫu POV 20s v2, kiểu Paris, GEM KOC, quy tắc nói giá Dimark.
- `USER.md`, `SOUL.md`, `IDENTITY.md` — thông tin anh và phong cách trợ lý.
- `custom-skills/pov_product_review_videos/` — skill video review POV 20s.
- `custom-skills/paris_product_videos/` — skill video kiểu Paris 24s.
- `your_files/` — Master Prompt POV v2, Master Prompt kiểu Paris, GEM KOC, kịch bản Dimark, tờ quay tay 24s, các báo cáo sao lưu.
- `goals/` — GOAL.md và file mẫu của 3 goal: POV 20s, Paris, KOC Chốt Đơn TikTok.

## Không có trong repo này

- Không có mật khẩu, token, file `.env`, khóa API.
- Không có video gốc nặng (file zip 7 video 104MB đã bỏ ra).
- Không có chat phụ — chat phụ nằm trong hệ thống Muse, sang tài khoản mới phải tạo lại rồi dán master prompt từng chat vào.

## Cách đẩy lên GitHub

1. Tạo repo mới trên GitHub, đặt **Private** (riêng tư), ví dụ tên `muse-backup`.
2. Tải file zip này lên, giải nén, đẩy toàn bộ thư mục này lên repo.
   Hoặc dùng git:
   ```bash
   git init
   git add .
   git commit -m "Muse backup 2026-11-20"
   git branch -M main
   git remote add origin https://github.com/khacvinhpro-star/muse-backup.git
   git push -u origin main
   ```
   Nếu repo đã có bản cũ, thay toàn bộ bằng bản mới này rồi commit lại, vì bản này đã gồm cả ngày hôm nay.

## Cách nạp sang tài khoản khác

1. Tải repo này về máy, hoặc gửi link repo cho Muse ở tài khoản mới.
2. Nói với Muse ở tài khoản mới:
   > "Cài 2 skill trong thư mục custom-skills này, và đọc MEMORY.md này làm bộ nhớ của anh."
3. Copy file về đúng chỗ, nếu Muse hỏi:
   - Skill → `~/workspace/custom-skills/`
   - `MEMORY.md`, `USER.md` → thư mục home `~/`
   - File mẫu → `~/workspace/your_files/`
4. Tạo lại chat phụ theo danh sách trong MEMORY.md, dán master prompt từng chat vào.

## Cập nhật sau này

Mỗi lần skill hay quy tắc thay đổi, anh xuất lại các file đã đổi và đẩy lên repo, ghi ngày vào commit.
