# FreshBox — Ghi nhớ thực phẩm trong tủ lạnh

**Day 02 · Tìm đúng bài toán cho AI**

FreshBox là ý tưởng của nhóm về một khung đặt trong tủ lạnh, mở bốn bên, có cảm biến ghi nhận lúc đặt thực phẩm vào và gửi thông tin/nhắc nhở đến điện thoại. Bản phân tích này được cập nhật theo **ba ảnh ý tưởng do Phạm Minh Cương cung cấp**.

| Thông tin | Nội dung |
|---|---|
| Học viên | Phạm Minh Cương |
| Mã học viên | 2A202602825 |
| Đề tài nhóm | FreshBox — khung theo dõi thực phẩm trong tủ lạnh |
| Tên nhóm và các thành viên khác | Chưa được cung cấp; FreshBox là tên sản phẩm, không tự coi là tên nhóm |
| Ngày cập nhật bản phân tích | 12/09/2026 |
| Repo | [Day02-2A202602825-PhamMinhCuong](https://github.com/mcnb2005/Day02-2A202602825-PhamMinhCuong) |
| Quyền truy cập | Công khai |

![Sơ đồ ý tưởng FreshBox](assets/freshbox-so-do.svg)

## Vấn đề cần kiểm chứng

Người dùng tủ lạnh có thể quên thời điểm cất hoặc mở một món thực phẩm, khiến việc kiểm tra và lựa chọn món cần chú ý phụ thuộc vào trí nhớ. Nhóm muốn giảm công ghi chép và giúp người dùng nhìn lại lịch sử lưu trữ trên điện thoại.

**Ảnh xác nhận ý tưởng của nhóm, chưa xác nhận tần suất khó khăn, hiệu quả thiết bị hoặc kết quả phỏng vấn.** Ngày cất vào tủ, ngày mở bao bì và thông tin hạn dùng là những dữ liệu khác nhau. FreshBox theo dõi và nhắc kiểm tra; không kết luận thực phẩm còn an toàn để ăn chỉ từ thời gian hoặc hình ảnh.

## Hướng đề xuất

- **MVP:** cảm biến + định danh vật phẩm do người dùng xác nhận + lưu mốc thời gian + quy tắc nhắc việc. Mức chọn là **Rule/IoT**, chưa cần AI cho chức năng cốt lõi.
- **AI mở rộng:** thử OCR/nhận dạng nhãn để giảm thao tác nhập; luôn cho người dùng xác nhận hoặc sửa.
- **Quyết định phân tích:** **Not Yet cho triển khai sử dụng thực tế**. Đã có concept và research; còn thiếu kiểm chứng nhu cầu, baseline, thử cảm biến và thiết kế nguồn điện. Đây là đề xuất của bản phân tích, chưa thay cho quyết định nhóm.

## Hồ sơ bài nộp

| Phần | Tài liệu |
|---|---|
| 01 — Cá nhân | [Scan 8 vấn đề](01-individual-problem-scan/01-problem-scan.md) · [Top 3 Cards](01-individual-problem-scan/02-top-3-problem-cards.md) · [Workflow trước/sau](01-individual-problem-scan/03-workflows.md) |
| 02 — Nhóm | [Ý tưởng và hội tụ](02-group-problem-statement/01-convergence.md) · [Research và validation](02-group-problem-statement/02-validation-and-research.md) · [Problem Statement v0/v1](02-group-problem-statement/03-problem-statement.md) |
| 02 — Quyết định | [Rule/Workflow/Agent và pilot](02-group-problem-statement/04-solution-and-decision.md) · [Đối chiếu ảnh và nguồn](02-group-problem-statement/05-kiem-chung-tu-tai-lieu.md) · [Thiết kế FreshBox](02-group-problem-statement/06-freshbox-concept.md) |
| 03 — Cá nhân | [Dữ kiện và câu hỏi reflection](03-individual-reflection/README.md) · [Nhật ký hỗ trợ AI](03-individual-reflection/01-nhat-ky-ho-tro-ai.md) |

## Những chi tiết từ ảnh đã đưa vào bài

Khung mở bốn bên; thông báo qua điện thoại; ba lựa chọn chiều ngang minh họa **26 / 38 / 50 cm**; chiều cao có thể điều chỉnh; ý tưởng bố trí pin trong **bốn trụ góc**. Kích thước, kết cấu và pin mới là concept, chưa phải thông số chế tạo đã thử nghiệm.

Xem [ảnh ý tưởng gốc](assets/freshbox-y-tuong-nhom.png). Các lời nhắc tạo ảnh và khẩu hiệu trong ảnh được dùng làm tư liệu ý tưởng, không coi là kết quả kiểm chứng sản phẩm.

## Trạng thái hoàn thiện

- [x] Xác nhận tên, mã học viên và đề tài nhóm qua thông tin học viên cung cấp.
- [x] Chuyển các phần phân tích sang FreshBox; bổ sung sơ đồ, research, metric và kế hoạch pilot.
- [x] Phân biệt nội dung có nguồn, giả định thiết kế và dữ liệu chưa đo.
- [ ] Điền tên nhóm, danh sách thành viên và đóng góp trực tiếp của từng người.
- [ ] Học viên xác nhận ít nhất 5 vấn đề từ trải nghiệm thật; tự trình bày và challenge.
- [ ] Bổ sung phỏng vấn/khảo sát, baseline và kết quả thử nghiệm; chưa có trong dữ liệu được cung cấp.
- [ ] Nhóm xác nhận lựa chọn cuối và học viên tự viết bài học/reflection.
- [ ] Xác nhận hạn nộp, nơi nhận bài và gửi đường dẫn repo theo hướng dẫn lớp.

## Đề bài và nguồn

[README/rubric](https://github.com/VinUni-AI20k/K4A-Day02-AI-Product-Labs#readme) · [Worksheet](https://github.com/VinUni-AI20k/K4A-Day02-AI-Product-Labs/blob/main/01-worksheet.md) · [Danh mục nguồn FreshBox](02-group-problem-statement/02-validation-and-research.md).

Bản đề tài học tập cũ được thay bằng FreshBox theo thông tin mới của học viên; lịch sử thay đổi vẫn được lưu trong Git.
