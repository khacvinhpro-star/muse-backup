# Báo cáo nghiên cứu — File backup AFF Workflow 2026-11-15

Nguồn: `backup-aff-workflow-2026-11-15.zip` (141 KB)
Giải nén tại: `~/workspace/research/backup-aff-workflow-2026-11-15/`
Ngày nghiên cứu: 2026-11-17

## 1. Tổng quan

- 16 mục trong zip, 13 file thực
- Dung lượng sau giải nén: ~209 KB
- Ngày trong file: 14/11/2026, sao lưu ngày 15/11/2026, là kho mới nhất trong 3 kho
- Định dạng: 12 file .md, 1 file .yaml, 1 file .pdf, không có ảnh, không có video, không có file chat phụ

Danh sách file:
- `HUONG-DAN-KHOI-PHUC.md` — Hướng dẫn khôi phục toàn bộ tuyến làm video AFF trên tài khoản Muse mới
- `master-prompt-video-san-pham.md` — Master prompt làm video sản phẩm, số cảnh tùy chỉnh, mặc định 6 cảnh
- `skill-shortprompt_affiliate/SKILL.md` — Skill ShortPrompt Affiliate, cách dùng từ điển lệnh + master prompt
- `skill-shortprompt_affiliate/skill.yaml` — Khai báo skill shortprompt_affiliate
- `skill-shortprompt_affiliate/references/lenh-phan-1-affiliate.md` — Phần 1: lệnh định dạng affiliate, 9 combo sẵn, 10 luồng kể chuyện
- `skill-shortprompt_affiliate/references/lenh-phan-2-hinh-anh.md` — Phần 2: bộ công cụ hình ảnh, 17 nhóm
- `skill-shortprompt_affiliate/references/lenh-phan-3-camera-shot.md` — Phần 3: 3 lệnh camera + bảng loại shot
- `skill-shortprompt_affiliate/references/vi-du-va-khoi-chuan.md` — Phần 4: 8 ví dụ + khối VOICE LOCK và CTA chuẩn
- `skill-shortprompt_affiliate/references/nguon-CongNghe_ShortPrompt_AF_Tiktok_Shopee.pdf` — PDF gốc KKHome AI, 17 trang
- `vi-du-da-lam/1-ong-dung-nhang-go-tai-loc.md` — Ống đựng nhang gỗ Tài Lộc, 3 cảnh
- `vi-du-da-lam/2-moc-inox-dan-tuong.md` — Móc inox dán tường, 6 cảnh
- `vi-du-da-lam/3-mu-phao-trum-dau.md` — Mũ phao trùm đầu kèm khẩu trang, 6 cảnh
- `vi-du-da-lam/4-giay-vai-nu-denim-t110.md` — Giày vải nữ denim T110, 6 cảnh, Jeffrey chấm 9/10

## 2. Đây là kho gì?

Gói sao lưu khôi phục cho riêng tuyến làm video AFF (TikTok Shop / Shopee). Mục đích: nếu đổi tài khoản Muse mới, đưa gói này cho Muse mới và bảo khôi phục tuyến làm video AFF — cài lại skill vào ~/workspace/custom-skills/shortprompt_affiliate/, chép master prompt vào ~/workspace/your_files/, tạo 1 chat phụ tên “Làm video AFF”, sản phẩm lưu ở ~/workspace/aff-videos/<tên-sản-phẩm>/.

Skill ShortPrompt Affiliate là skill làm video/ảnh bán hàng bằng từ điển lệnh ngắn của KKHome AI. Công thức vàng: Lệnh định dạng (Phần 1) + Lệnh hình ảnh / camera (Phần 2-3) + Thoại tiếng Việt + CTA.

Hai khối chuẩn dán nguyên văn vào mọi prompt video:
- VOICE LOCK: giọng nữ miền Nam, ngọt ngào, trong trẻo, thân thiện, tràn năng lượng, chỉ nói tiếng Việt, lip-synced.
- CTA: 3 giây cuối, icon giỏ hàng TikTok Shop góc trái dưới, nhân vật chỉ xuống.

Workflow: nhận 1-5 ảnh sản phẩm + số cảnh (mặc định 6) + link tùy chọn, tự chọn kiểu video hợp nhất, làm storyboard trước với video từ 3 cảnh trở lên, viết kịch bản từng cảnh, render từng cảnh, upscale lên 1080x1920, kiểm tra bằng giải mã toàn bộ, ráp xfade 0,5s, giao video + caption/hashtag.

Mâu thuẫn nội bộ: master prompt ghi mặc định 5 giây/cảnh (6 cảnh = 30 giây), trong khi skill và cả 4 ví dụ đều dùng ~10 giây/cảnh (6 cảnh ≈ 57,5 giây).

## 3. 4 ví dụ đã làm

1. Ống đựng nhang gỗ Tài Lộc, 3 cảnh ~29s, faceless. Lỗi nhân đôi sản phẩm: cảnh 1 và 3 bị thành 2 ống khi quay toàn cảnh.
2. Móc inox dán tường, 6 cảnh 57,6s, problem-solution + test kéo thử. QC 6/6 cảnh khớp storyboard. Cảnh 1 lọt một phần khuôn mặt nghiêng ở mép phải.
3. Mũ phao trùm đầu kèm khẩu trang, 6 cảnh 57,6s, try-on có nhân vật. Lỗi lệch sản phẩm nghiêm trọng: cảnh 5 và 6 bị lệch thành mũ lông vành tai + khẩu trang rời, không còn là mũ phao liền khẩu trang.
4. Giày vải nữ denim T110, 6 cảnh 57,6s, try-on không lộ mặt. QC giày khớp ảnh gốc cả 6 cảnh, Jeffrey chấm 9/10.

Điểm chung: đều có bảng kịch bản + prompt từng cảnh + caption/hashtag + VOICE LOCK/CTA + tự kiểm tra + kết quả/QC. Đều tuân thủ không bịa, chỉ nêu đặc điểm nhìn thấy, phần chưa rõ ghi rõ là chưa rõ.

## 4. So sánh với Master Prompt v3 (kho 2026-11-09)

- Master Prompt v3: 1-4 cảnh x 10s, mặc định 2 cảnh ≈ 19,5s, cố định tay-only, không lộ mặt, 1 bối cảnh nhà thật.
- ShortPrompt: mặc định 6 cảnh ≈ 57,5s, tự chọn kiểu video theo sản phẩm, có nhân vật hoặc faceless.
- ShortPrompt có luật đổi cỡ cảnh cứng, storyboard trước, QC full-decode. Master Prompt v3 có cầu nối hành động dở dang + tham chiếu kép, ShortPrompt không có luật này.
- Giọng: cả hai đều khóa giọng nữ miền Nam, nhưng nguồn gốc khác nhau.
- CTA: v3 CTA bằng thoại ở cảnh cuối, ShortPrompt CTA bằng hình icon giỏ hàng 3 giây cuối.
- Caption: v3 4-5 tag, ShortPrompt 5-8 tag.

Kết luận: hai hệ thống bổ sung cho nhau, không thay thế nhau. Master Prompt v3 là khung ngắn, cố định, tay-only, đúng khung POV 20s của Kevin. ShortPrompt là từ điển lệnh + quy trình dài, linh hoạt.

## 5. So sánh với 2 kho trước

- UGC v2 vẫn thiếu: file này không nhắc tới UGC v2 hay Product-Focus v1. UGC v2 vẫn thiếu sau cả 3 kho.
- Trùng lặp: ống nhang và móc inox đã có kịch bản trong kho 9/11, file này là bản làm lại dài hơn, đầy đủ hơn. Giày denim T110 trùng chủ đề giày denim với video của Kevin, nhưng là sản phẩm khác.
- Mới: toàn bộ skill shortprompt_affiliate, master prompt số cảnh tùy chỉnh, 2 ví dụ mũ phao + giày denim T110 (13-14/11).
- Chat phụ: không có chat phụ nào được lưu sẵn, chỉ có hướng dẫn tạo 1 chat phụ mới tên “Làm video AFF”. Khác kho 9/11 (có 5 chat phụ).
- Vẫn thiếu sau cả 3 kho: UGC v2, Product-Focus v1, Poster Engine đầy đủ, SEO Engine PDF, file video thành phẩm.

## 6. Tái sử dụng cho Kevin — mẫu POV 20s bản v2

Dùng được ngay:
- Luật không bịa, chỉ nêu đặc điểm nhìn thấy.
- Luật sản phẩm đồng nhất tuyệt đối.
- Luật đổi cỡ cảnh: mở toàn/trung, xen POV demo, cận cảnh chỉ dùng ngắn.
- Storyboard trước cho video phức tạp, mỗi ô làm start frame.
- QC full-decode file upscale trước khi nối, chỉ render lại cảnh lỗi.
- Từ điển lệnh theo ngành và luồng kể chuyện làm ngân hàng hook/kiểu video.
- CTA bằng thoại + chỉ giỏ hàng ở cảnh cuối.

Chỉ tham khảo: 9 combo và Phần 2 hiệu ứng reveal/luxury/sci-fi, master prompt số cảnh tùy chỉnh, ví dụ mũ phao try-on có nhân vật.

Mâu thuẫn với quy tắc của Kevin, không áp:
- Thời lượng mặc định 6 cảnh ≈ 57,5s, mâu thuẫn khung cứng 20s / 2 cảnh x 10s của v2.
- Giọng đọc VOICE LOCK giọng nữ miền Nam, giọng của Kevin vẫn CHƯA XÁC NHẬN.
- CTA bằng hình icon giỏ hàng, mâu thuẫn luật nền sạch không thêm logo/chữ khác nếu hiểu theo nghĩa hẹp.
- Lệnh FloatingProduct, 360Spin, SmokeReveal/FireReveal có thể phá logic vật lý và tỉ lệ thực tế.
- Lệnh slowmotion, freeze, timelapse mâu thuẫn luật tốc độ thực 1x.
- Lệnh Indonesia / modest fashion không phù hợp thị trường của Kevin.
- Nhân vật nói trực tiếp, khớp miệng, Kevin làm faceless/POV tay-only.

## 7. Cảnh báo

- Đây là kho của Jeffrey (tuyến AFF của Jeffrey), nguồn lệnh là KKHome AI (© JennyKieu), không phải của Kevin. Chỉ học phương pháp, không dùng tài khoản, kênh, Drive, link hay thông tin cá nhân trong kho cho Kevin.
- Không gộp danh tính: file này gọi chủ kho là Jeffrey, hai kho trước gọi chủ kho là Nguyen / Khắc Vinh / KhaiKieu / anh Khải. Không kết luận Jeffrey và Khai/Nguyen là một người.
- Không tìm thấy email hay số điện thoại nào trong gói này. Không có mật khẩu / token / API key.

## 8. Khuyến nghị

1. Giữ Master Prompt v3 làm khung chuẩn duy nhất cho POV 20s của Kevin, lấy ShortPrompt làm ngân hàng lệnh bổ sung, không thay khung.
2. Bổ sung 2 luật ShortPrompt vào checklist QC 12 bước của v2: kiểm tra file upscale bằng giải mã toàn bộ, và kiểm tra cỡ cảnh đã thay đổi.
3. Không áp VOICE LOCK giọng nữ miền Nam và CTA icon giỏ hàng cho Kevin khi chưa có xác nhận.
4. Không tái tạo nguyên chat phụ “Làm video AFF” cho Kevin. Nếu Kevin muốn làn AFF dài hơn 20s thì tạo chat mới với tên và quy tắc của Kevin.
5. UGC v2 vẫn thiếu sau cả 3 kho, đừng đi tìm thêm ngay. Với video POV 20s hiện tại, Master Prompt v3 + ShortPrompt đã đủ.
