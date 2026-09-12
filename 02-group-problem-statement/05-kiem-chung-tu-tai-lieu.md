# 02.5 — Kiểm chứng từ ảnh và tài liệu: FreshBox

## Phương pháp và mức bằng chứng

Trợ lý đã đọc ba ảnh học viên cung cấp, đối chiếu nội dung với yêu cầu bài lab và các nguồn research ngày 12/09/2026. Học viên xác nhận đây là ý tưởng nhóm. Chưa có người kiểm tra độc lập hoặc thử nghiệm thực địa được cung cấp.

[Ảnh 1 lưu trong repo](../assets/freshbox-y-tuong-nhom.png). Ảnh 2/3 được đọc trong cuộc trao đổi; thông tin sản phẩm được chép vào bảng dưới, không đưa các thanh tab và giao diện máy tính ngoài sản phẩm lên repo.

## Đối chiếu ý tưởng với yêu cầu có thể kiểm tra

| Nội dung trong tư liệu | Kết luận có căn cứ | Phần còn chưa biết | Xử lý trong thiết kế |
|---|---|---|---|
| Khung hình hộp, mở bốn bên | Đây là hình dạng nhóm muốn khảo sát | Chất liệu, tải, độ sâu, độ vừa tủ và luồng khí | Chỉ gọi là concept; đo vật lý trước khi chốt |
| Cảm biến ghi lúc đặt đồ vào | Có yêu cầu ghi sự kiện theo thời gian | Cảm biến cụ thể, nhận đúng món, nhiễu và sai số đồng hồ | Một món/vùng ở MVP; người dùng xác nhận ID |
| Thông tin/nhắc qua điện thoại | Nhóm muốn tra cứu và được nhắc từ xa | Giao thức, đường truyền khi đóng cửa tủ, trạng thái nhận | Thử kênh thông báo; hiển thị lần đồng bộ cuối |
| Các cỡ 26/38/50 cm trên ảnh 2 | Ba lựa chọn chiều ngang được minh họa | Chưa có dung sai hay số đo tủ; chưa biết chiều sâu | Không công bố tương thích mọi tủ |
| Chiều cao kéo lên/xuống | Có yêu cầu cơ khí điều chỉnh | Biên độ, khóa, độ bền và vệ sinh | Kiểm bằng mô hình hình dáng trước |
| Pin ở bốn trụ trong ảnh 3 | Bốn góc là vị trí nguồn được đề xuất | Loại pin, mạch quản lý, đấu nối, độ kín, nhiệt độ và thời lượng | Không coi ảnh là sơ đồ điện; cần thiết kế và thử nguồn |
| Hình quảng bá gợi ý giữ tươi/giảm lãng phí | Là mục tiêu mong muốn của concept | Chưa có dữ liệu chứng minh | Bài chỉ tuyên bố theo dõi và nhắc kiểm tra |
| Hình/nhãn minh họa có tên sản phẩm và thời gian | Là ví dụ hình ảnh | Không chứng minh AI/cảm biến nhận đúng tên hoặc mốc | Không đưa thành kết quả độ chính xác |

## Đối chiếu nghiên cứu và tác động lên bài

1. **Tính năng tương tự đã tồn tại:** NoWaste và Samsung có cách quản lý danh sách thực phẩm. FreshBox phải chứng minh lợi ích của phụ kiện và cách ghi nhận, không chỉ có màn hình đẹp.
2. **An toàn thực phẩm phụ thuộc nhiều yếu tố:** nguồn FDA/FoodSafety.gov khiến phạm vi được sửa thành ghi lịch sử và nhắc kiểm tra.
3. **Theo dõi tương tác vật phẩm là một bài toán riêng:** nghiên cứu CloudFridge là bằng chứng về hướng nghiên cứu; không chuyển các chỉ số của họ sang FreshBox.

Nguồn và giới hạn được ghi tại [research](02-validation-and-research.md).

## Tóm tắt kết quả

- **Đã có:** một concept nhóm với ba hình; mô tả yêu cầu; phân tích nguồn; các trường hợp cần kiểm tra.
- **Chưa có:** bằng chứng người dùng gặp khó khăn thường xuyên, nhóm thành viên đầy đủ, phần cứng, đo baseline, so sánh không AI/AI, thử pin và phản hồi hộ gia đình.
- **Quyết định:** giữ Not Yet cho triển khai; thực hiện validation và pilot theo kế hoạch.

Các kết quả trên là rà soát tài liệu của trợ lý. Không ghi “đã phỏng vấn 3 người”, “độ chính xác 95%” hoặc “giảm lãng phí 30%” khi chưa có phép đo.
