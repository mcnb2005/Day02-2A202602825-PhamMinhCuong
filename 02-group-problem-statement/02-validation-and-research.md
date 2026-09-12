# 02.2 — Research và validation: FreshBox

Ngày tra cứu nguồn: **12/09/2026**. Các mô tả tính năng dưới đây dựa trên tài liệu của nhà cung cấp; chưa phải kết quả nhóm dùng thử sản phẩm.

## 1. Sổ bằng chứng

| Mã | Bằng chứng | Đã xác nhận được gì? | Không chứng minh được gì? |
|---|---|---|---|
| E1 | Ba ảnh do học viên gửi và xác nhận là ý tưởng nhóm | Concept, biến thể kích thước, pin bốn góc | Thiết bị tồn tại, chạy đúng, nhu cầu người dùng hoặc tuổi thọ pin |
| E2 | Tài liệu NoWaste, Samsung và FoodKeeper | Có những hướng quản lý thực phẩm để so sánh | FreshBox tốt hơn, rẻ hơn hoặc tiết kiệm bao nhiêu |
| E3 | Nguồn FDA/FoodSafety.gov | Cần xét điều kiện bảo quản; thời gian cất không đủ để kết luận an toàn | Thiết bị FreshBox đo được chất lượng thực phẩm |
| E4 | Phỏng vấn/quan sát và log thiết bị | Chưa có dữ liệu được cung cấp | Chưa thể báo cáo baseline, tỷ lệ lỗi hoặc giảm lãng phí |

## 2. Giải pháp và pattern đã có

| Hướng | Thông tin có nguồn | Phân tích cho FreshBox |
|---|---|---|
| Nhãn giấy + lịch nhắc | Phương án đối chứng do bản phân tích đề xuất: ghi ngày cất/mở, sắp món và đặt nhắc thủ công | Chi phí triển khai đơn giản; phải kiểm tra cách này có đủ trước khi thêm phần cứng |
| NoWaste | Mô tả nhà phát triển nêu danh sách tủ lạnh/ngăn đông/tủ đồ, quét mã và sắp theo ngày hết hạn. [Google Play](https://play.google.com/store/apps/details?id=com.khcreations.nowaste) | Đối chứng app quản lý danh sách. Cần đo công duy trì của người dùng; không giả định mọi app chỉ có nhập tay |
| Samsung Family Hub / View Inside | Tài liệu mô tả xem bên trong, thêm/sửa danh sách và đặt mốc theo dõi thực phẩm. [Samsung Support](https://www.samsung.com/us/support/answer/ANS10006842/) | Cho thấy hướng quản lý thực phẩm gắn với tủ đã tồn tại. FreshBox đề xuất phụ kiện cho tủ đang dùng, nhưng chưa có số liệu chi phí hoặc tương thích |
| FoodKeeper | Công cụ tra cứu thông tin bảo quản thực phẩm/đồ uống do USDA FSIS phối hợp phát triển. [FoodSafety.gov](https://www.foodsafety.gov/keep-food-safe/foodkeeper-app) | Dùng để kiểm tra cách diễn đạt hướng dẫn; không biến thành bộ phát hiện độ tươi của từng món |
| CloudFridge | Nghiên cứu trình bày testbed kết hợp cảm biến và phần mềm để theo dõi tương tác/vị trí vật phẩm. [Bài báo, abstract](https://arxiv.org/abs/1401.0585) | Gợi ý cần thử khả năng gắn sự kiện với đúng món. Không lấy kết quả nghiên cứu đó làm độ chính xác của FreshBox |

**Suy luận từ research:** khác biệt đáng thử của FreshBox là giảm công ghi nhận sự kiện trên tủ sẵn có. Đồng hồ, định danh và chất lượng dữ liệu cần giải quyết trước khi thêm AI.

## 3. Ranh giới liên quan đến bảo quản thực phẩm

FDA khuyến nghị giữ tủ lạnh ở mức 4°C hoặc thấp hơn, chú ý điều kiện bảo quản và không nhồi chặt đến mức cản lưu thông khí. Cơ quan này cũng nêu thực phẩm có thể gây bệnh dù chưa có biểu hiện hỏng rõ. [Nguồn FDA](https://www.fda.gov/consumers/consumer-updates/are-you-storing-food-safely).

Bảng thời gian bảo quản phân biệt từng loại và điều kiện. Vì vậy không dùng một công thức “đã cất X giờ thì còn an toàn” cho mọi món. [Bảng FoodSafety.gov](https://www.foodsafety.gov/food-safety-charts/cold-food-storage-charts).

**Ứng dụng vào thiết kế:** lưu riêng ngày cất, ngày mở, ngày chế biến nếu người dùng biết, thông tin nhãn và mốc nhắc. Không tuyên bố ăn được, không coi camera/cảm biến hiện diện là phép kiểm nghiệm thực phẩm. Chi tiết này là suy luận thiết kế của bản phân tích từ các nguồn trên.

## 4. Kết quả kiểm chứng hiện có

Đã đối chiếu yêu cầu trong ảnh với nghiên cứu và ghi các khoảng trống tại [hồ sơ đối chiếu](05-kiem-chung-tu-tai-lieu.md). Đây là rà soát tư liệu của trợ lý, không phải nghiên cứu người dùng hoặc thử phần cứng.

**Chưa có:** người tham gia, câu trả lời phỏng vấn, log cân/cảm biến, thời lượng pin, ngân sách linh kiện hoặc số liệu giảm lãng phí.

## 5. Giả định cần kiểm chứng

| Mã | Giả định | Bằng chứng cần lấy | Tín hiệu khiến đổi hướng |
|---|---|---|---|
| H1 | Người dùng thường thiếu mốc cất/mở và muốn tra lại | Một sự việc gần đây, cách xử lý và log quan sát | Người dùng không gặp hoặc nhãn giấy đã đủ |
| H2 | Công ghi nhận là lý do bỏ app | Bấm giờ nhập/cập nhật bằng cách hiện tại | Khó khăn chính nằm ở thói quen sử dụng thực phẩm, không phải ghi nhận |
| H3 | Sự kiện được gắn đúng món với ít xác nhận | Log có người quan sát, gồm trường hợp lấy/đặt lại và thay món | Cần xác nhận quá nhiều, sai ID hoặc reset mốc |
| H4 | Nhắc trên điện thoại có ích và đến đúng lúc | Nhắc đã gửi/đã nhận và phản hồi về mức phiền | Người dùng bỏ qua hoặc tắt thông báo |
| H5 | Khung và nguồn phù hợp với tủ | Đo ngăn tủ, thử đóng cửa, nhiệt độ/luồng khí, log năng lượng | Chiếm chỗ, cản sử dụng, mất kết nối hoặc phải thay pin quá thường xuyên |
| H6 | OCR làm giảm công nhập | So sánh nhập tay với ảnh nhãn + kiểm/sửa | Thời gian chụp/sửa cao hơn chọn tên |

## 6. Kế hoạch phỏng vấn nhanh

Đề xuất hỏi 3 người trực tiếp quản lý thực phẩm; hoặc survey 5–10 người nếu không phỏng vấn được. Đây là kế hoạch, không phải mẫu đã thu.

1. Lần gần nhất không nhớ một món được cất hoặc mở khi nào là lúc nào?
2. Bạn đã tìm thông tin và xử lý thế nào? Có ví dụ cụ thể không?
3. Bạn hiện dùng nhãn, trí nhớ hay app; bước nào tốn công?
4. Ai khác sử dụng tủ, họ có cập nhật khi lấy hoặc thay món không?
5. Loại thông tin nào bạn thực sự muốn xem trên điện thoại?
6. Nếu vẫn phải xác nhận món mỗi lần cất/lấy, bạn thấy có chấp nhận được không?
7. Một khung đặt trong tủ sẽ cản trở thao tác nào? Có thể đo ngăn tủ thực tế không?

| Người/mẫu | Ngày | Sự việc và cách đang xử lý | Thời gian/tần suất: đo hay ước lượng | Xác nhận | Phản bác | Thay đổi bài toán |
|---|---|---|---|---|---|---|
| P01 — chưa có dữ liệu | | | | | | |
| P02 — chưa có dữ liệu | | | | | | |
| P03 — chưa có dữ liệu | | | | | | |

Không hỏi dẫn dắt kiểu “Bạn có thích hộp thông minh này không?” để thay cho quan sát vấn đề. Ghi cả trường hợp không có nhu cầu.

## 7. Mẫu log thử nghiệm

| Mẫu | Phương án | ID/vùng | Hành động thực | Giờ chuẩn | Giờ hệ thống | Công xác nhận/sửa (giây) | Log đúng? | Nhắc đã nhận? | Lỗi/ngoại lệ |
|---|---|---|---|---|---|---|---|---|---|
| Chưa chạy | | | | | | | | | |

Người quan sát hoặc video có mốc thời gian là đối chiếu; không dùng chính log cảm biến làm đáp án cho cảm biến. Không lưu hình người hoặc thông tin không liên quan khi thử.

[Metric và cách tính](03-problem-statement.md) · [Pilot và điều kiện quyết định](04-solution-and-decision.md).
