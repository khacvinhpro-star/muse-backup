# Báo cáo nghiên cứu — File backup KhaiKieu 2026-11-05

Nguồn: `backup-khaikieu-2026-11-05.zip` (81 KB)
Giải nén tại: `~/workspace/research/backup-khaikieu-2026-11-05/`
Ngày nghiên cứu: 2026-11-17

## 1. Tổng quan

- 14 mục trong zip, 9 file, 7 nội dung duy nhất (2 file trùng tuyệt đối)
- Dung lượng sau giải nén: ~200 KB
- Ngày sao lưu: 05/11/2026, sớm hơn kho 2026-11-09 bốn ngày
- Định dạng: 8 file .md, 1 file .yaml, không có ảnh, không có video, không có PDF

Danh sách file:
- `HUONG-DAN-KHOI-PHUC.md` — Hướng dẫn khôi phục phần làm phim trên tài khoản mới
- `THONG-TIN-CA-NHAN.md` — Thông tin cá nhân của chủ kho, không trích nội dung
- `films-khaikieu/README.md` — Cấu trúc thư mục phim và quy tắc lưu phim
- `skill-khai-kieu-film-workflow/SKILL.md` — Skill làm phim khai_kieu_film_workflow, tóm tắt workflow v3.3
- `skill-khai-kieu-film-workflow/skill.yaml` — Khai báo skill
- `skill-khai-kieu-film-workflow/references/workflow-v3.2.md` — Workflow gốc v3.2, 17/10/2026
- `skill-khai-kieu-film-workflow/references/workflow-v3.3-hoan-thien.md` — Workflow gốc v3.3 HOÀN THIỆN, 03/11/2026, bản chính
- `workflow/3._Workflow_Phim_KhaiKieu_Home_AI_with_Muse_2026_10_v3.2.md` — Bản sao y hệt v3.2
- `workflow/Workflow_Phim_KhaiKieu_Home_AI_with_Muse_2026_10_v3.3_HOAN_THIEN.md` — Bản sao y hệt v3.3 hoàn thiện

## 2. Đây là kho gì?

Gói sao lưu khôi phục cho riêng làn làm phim ngắn chữa lành KhaiKieu Home AI, không phải kho tổng hợp như file 2026-11-09. Mục đích: nếu tài khoản cũ không vào được nữa thì dùng gói này dựng lại phần làm phim trên tài khoản mới.

Phim theo workflow này: phim ngắn chữa lành, tiếng Việt, dọc 9:16, 1080x1920, nhân vật hư cấu do AI sinh, đăng kênh YouTube @KhaiKieuStudio. Trong gói chưa có phim nào được render, không có lịch sử chat, chat phụ cũ, cài đặt tài khoản, mật khẩu hay mã đăng nhập.

## 3. Pipeline làm phim (workflow v3.3 hoàn thiện)

Đầu vào: số phân cảnh, tên kênh, mô tả phim hoặc link YouTube để rút VIBE.

Pipeline 7 bước:
1. Nhận input, rút VIBE
2. Thiết kế nhân vật bằng Character DNA, sinh ảnh DNA full-body
3. Viết kịch bản: chia scene x 10s, timeline 3-beats-sống, Sound Design 3 lớp, Voice DNA riêng từng nhân vật
4. Poster: tự render 1-2 concept, nếu bị từ chối 2 lần thì giao khối lệnh Poster Engine + ảnh DNA
5. SEO & Revenue Package
6. Render từng scene 10s
7. Ráp crossfade 0,5s, xuất PREVIEW + GỐC, kiểm chứng QC

Mặc định cho @KhaiKieuStudio: 12 scenes x 10s, ráp crossfade 0,5s = 114,5s. Dàn nhân vật 2-5 người/phim, tối đa 2 người nói/scene. Mỗi scene bắt buộc 3 beats, mỗi beat đều có diễn + thoại, tối đa 20 từ/beat. Giữa mỗi lần đổi lượt nói có nhịp im lặng 0,5s + camera lướt mượt, cấm từ CUT.

Giọng đọc: giọng miền Nam mặc định, khóa bằng Bảng Voice DNA copy nguyên văn vào mọi scene. Trợ lý không nghe được audio nên người dùng phải tự kiểm chứng giọng.

Character DNA: ảnh DNA full-body là nguồn sự thật duy nhất, mọi prompt sau chỉ gán tag ảnh, không mô tả lại.

Poster: tiêu đề 3-7 từ dạng hook, không bao giờ là font, phải là hiện tượng vật lý sống từ chất liệu kịch bản, chiếm 15-20% chiều cao poster.

SEO: 3 tiêu đề mobile high-CTR, mô tả đa tầng, pinned comment, bộ tag lean, tên file snake_case + 1080P_60Fps.

Đóng gói: xuất GỐC 1080p + preview 540x960 + bản LIGHT khi mạng yếu, upload lên Google Drive, sửa scene thì cập nhật đúng file Drive cũ giữ nguyên link. Render tối đa 6 video / 1 message. CTA 3 giây cuối: icon chế tác từ chất liệu kịch bản + 2 pictogram ở góc trên bên phải, mô tả bằng hình dạng, không viết tên nút Like / Subscribe.

## 4. So sánh v3.2 vs v3.3

- v3.2 (17/10): thêm Luật 3 Beats Sống, sửa lỗi phim lờ đờ vì scene câm dài.
- v3.3 (02/11): giữ nguyên v3.2, thêm Luật Khóa Môi Theo Beat, sửa lỗi giọng của B, môi của A.
- v3.3 HOÀN THIỆN (03/11): giữ nguyên v3.3, thêm Luật Camera-First và Luật Cố Định Chất Giọng Xuyên Scene, sửa lỗi ở 0:43 phim Truyện 1.

Kết luận: dùng v3.3 hoàn thiện, v3.2 chỉ để tham chiếu.

## 5. So với kho sao lưu 2026-11-09

Có lấp được chỗ thiếu quan trọng nhất: báo cáo kho 2026-11-09 ghi file workflow gốc v3.3 không có trong zip. File này chính là file gốc đó, kèm cả v3.2 để đối chiếu.

Liên quan chat phụ Phim ngắn và skill workflow_phim: skill trong kho 2026-11-09 tên workflow_phim, làm phim cho kênh Chuyện Đời Qua Phim; skill trong file này tên khai_kieu_film_workflow, làm phim cho kênh @KhaiKieuStudio. Pipeline giống nhau về bản chất, nhưng tên skill, tên kênh và người phê duyệt khác nhau, không gộp thành một.

UGC v2 vẫn chưa có. Poster Engine đầy đủ và SEO Engine PDF vẫn thiếu trong cả hai kho.

## 6. Tái sử dụng cho Kevin

Dùng được cho mẫu POV 20s (học phương pháp):
- Tham chiếu kép: render cảnh sau từ frame cuối cảnh trước + ảnh gốc
- Khóa tuyệt đối bằng ảnh tham chiếu, không mô tả lại
- Camera-First và khóa môi theo beat, theo tinh thần: hành động/thoại bắt đầu sau khi khung hình đã đúng chủ thể
- QC từng cảnh, chỉ render lại cảnh lỗi
- Công thức thời lượng và crossfade 0,5s, cấu trúc 3 beats mở - đáp - chốt

Chỉ dùng cho phim dài: pipeline 12 scenes / 114,5s, nhân vật đa người, Character DNA, Voice DNA nhân vật hư cấu, Poster Engine, SEO phim, FlowKit.

Không nên dùng cho Kevin: mặc định kênh @KhaiKieuStudio, giọng Nam mặc định, cấu hình 12 scenes, CTA pictogram cuối phim. Giọng đọc của Kevin vẫn CHƯA XÁC NHẬN, không mặc định giọng Nam này.

## 7. Cảnh báo

- Đây là kho của KhaiKieu / anh Khải (Khắc Vinh), không phải của Kevin. Chỉ học phương pháp, không dùng tài khoản, kênh @KhaiKieuStudio, Drive hay danh tính này cho Kevin.
- File THONG-TIN-CA-NHAN.md chứa thông tin cá nhân của chủ kho, không chia sẻ, không copy, không dùng cho Kevin.
- Không có mật khẩu / token / API key trong gói này.
- Mâu thuẫn nhỏ chưa xác minh: workflow gọi người phê duyệt là Khai trong khi tài khoản ghi tên Jeffrey, không tự kết luận hai tên này là một người.

## 8. Khuyến nghị

1. Dùng file v3.3 HOÀN THIỆN làm nguồn gốc chuẩn cho skill phim, cập nhật skill workflow_phim theo file gốc, giữ tên kênh Chuyện Đời Qua Phim, không đổi sang @KhaiKieuStudio. Bỏ v3.2, chỉ giữ tham chiếu.
2. Không tái tạo nguyên chat phụ Làm phim KhaiKieu cho Kevin. Nếu Kevin muốn làm phim ngắn thì tạo chat mới với tên/kênh của Kevin, chỉ mang sang phương pháp.
3. Bổ sung 2 luật v3.3 hoàn thiện vào checklist QC mẫu POV 20s v2 theo tinh thần tương đương: kiểm tra hành động/thoại bắt đầu sau khi khung hình đã đúng chủ thể, và giọng đọc nhất quán xuyên suốt 2 cảnh.
4. Giữ nguyên 2 bản sao workflow, khi dọn kho giữ 1 bản duy nhất trong references/ kèm skill. Giữ zip gốc.
5. Poster Engine đầy đủ và SEO Engine PDF vẫn thiếu, chỉ đi tìm khi Kevin thực sự làm phim dài. Với video POV 20s hiện tại, caption + hashtag theo Master Prompt v3 đã đủ.
