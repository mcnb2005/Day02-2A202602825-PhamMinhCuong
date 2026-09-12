# 02.4 — Chọn Rule/Workflow/Agent và quyết định FreshBox

## 1. Ma trận giải pháp

| Mức | Phương án cụ thể | Khi nào đủ? | Đánh đổi | Kết luận đề xuất |
|---|---|---|---|---|
| No AI / sửa quy trình | Nhãn ngày cất/mở, khu vực món cần chú ý, lịch nhắc nhập tay | Ít món, một người quản lý và duy trì nhãn tốt | Cần tự ghi và nhìn lại | Là đối chứng bắt buộc |
| Rule | Cảm biến, ID xác nhận, đồng hồ, lịch sử và nhắc theo mốc đã chọn | Chuỗi bước cố định, không cần hiểu ngữ nghĩa phức tạp | Vẫn cần xác nhận món, quản lý nguồn/mạng | **Chọn làm lõi MVP** |
| Workflow có AI | Rule + người dùng chụp nhãn → OCR gợi ý → kiểm/sửa → lưu | Công nhập nhãn thật sự là điểm nghẽn | Chụp ảnh, nhận dạng sai và công sửa có thể lớn | Thử riêng nếu baseline cho thấy cần |
| Agent | Tự nhận mọi món, lập kế hoạch bữa ăn, quyết định mua/bỏ và hành động nhiều bước | Chỉ xét khi có nhu cầu mới, dữ liệu và quyền rõ | Vượt phạm vi; dễ quyết định trên lịch sử sai | Không chọn |

Cảm biến và kết nối điện thoại là tự động hóa/IoT, không tự động được gọi là AI. Ghi timestamp và so lịch nhắc là bài toán quy tắc. OCR có thể hỗ trợ đọc nhãn, nhưng không xác định chất lượng bên trong thực phẩm.

## 2. Độ mơ hồ và phức tạp

- **Ghi sự kiện/nhắc:** độ mơ hồ thấp nếu chỉ có một món trong một vùng và người dùng xác nhận; Rule đủ.
- **Nhiều món/đổi hộp/lấy rồi đặt lại:** mơ hồ tăng vì chưa biết danh tính sự kiện; giải quyết bằng giới hạn vùng và xác nhận trước khi thêm AI.
- **Đọc nhãn:** có thể cần Workflow có AI để gợi ý nội dung, người dùng giữ quyền sửa.
- **Kết luận an toàn để ăn:** ngoài phạm vi FreshBox; lịch sử không đầy đủ không được biến thành lời bảo đảm.

## 3. Quyết định hiện tại

**Not Yet cho triển khai sử dụng thực tế.** Có thể chuẩn bị và thực hiện kiểm chứng nhu cầu, mô hình hình dáng và thử nghiệm sự kiện có kiểm soát. Chưa có kết quả đủ để tuyên bố hệ thống hoạt động hoặc giảm lãng phí.

| Điều kiện | Hiện trạng |
|---|---|
| Ý tưởng nhóm | Đã được học viên xác nhận bằng ba ảnh |
| Actor và khó khăn thật | Có giả thuyết; chưa có phỏng vấn được cung cấp |
| Baseline và lợi ích | Đã thiết kế phép đo; chưa có số liệu |
| Cảm biến và định danh | Có đề xuất một vùng/một món; chưa có log thử |
| Kích thước và pin | Có concept; chưa có bản vẽ chế tạo hoặc phép thử |
| Owner và review | Vai trò được đề xuất; tên người nhận chưa được cung cấp |
| So với không AI | Có phương án đối chứng và research; chưa đo thực tế |

Đây là kết luận của bản phân tích. Quyết định được cả nhóm thống nhất cần ghi sau.

## 4. Pilot nhỏ nhất

### Bước A — Kiểm chứng nhu cầu trước phần cứng

Hỏi 3 người quản lý thực phẩm hoặc survey 5–10 người. Quan sát một lần cất/tra món theo cách hiện tại; ghi rõ số đo trực tiếp hay hồi tưởng. Nếu nhãn giấy đã đủ hoặc người dùng không cần thông tin này, sửa quy trình thay vì mặc định làm thiết bị.

### Bước B — Thử luồng bằng thao tác mô phỏng

Dùng hộp/vật mô phỏng, nhãn ID và điện thoại; người điều phối bấm tạo sự kiện thay cảm biến. Mục tiêu là thử màn hình xác nhận, mốc ngày và mức phiền của nhắc. Ghi rõ đây là mô phỏng tương tác, không được tính thành độ chính xác phần cứng.

Mỗi người thử các trường hợp mới với nhãn giấy, app nhập tay và FreshBox mô phỏng. Đổi thứ tự giữa người để giảm lợi thế quen bài; tính công xác nhận/sửa vào thời gian.

### Bước C — Khi đã có nguyên mẫu cảm biến

Đề xuất 30 lượt sự kiện có người quan sát, chia đều 6 nhóm: cất mới, lấy ra, đặt lại cùng món, thay món, nhiễu/di chuyển, ngoại lệ nguồn/mạng. Thêm tình huống nhiều món và vật cùng trọng lượng để xác nhận giới hạn hệ thống. Báo riêng kết quả từng nhóm, không gộp lượt mô phỏng với lượt cảm biến thật.

Thử lịch nhắc riêng: ghi mốc hẹn, lúc gửi và lúc điện thoại thực nhận. Các lần không kết nối phải được báo riêng, không loại khỏi báo cáo một cách âm thầm.

### Bước D — Chỉ thử tại tủ khi phần cứng phù hợp

Đo khung, khoảng hở, đóng/mở cửa, ảnh hưởng lên việc sắp đồ và luồng khí; kiểm kết nối và năng lượng trong điều kiện tủ. Người có chuyên môn kiểm tra thiết kế nguồn trước khi đặt nguyên mẫu điện vào môi trường ẩm/lạnh. Chưa có sơ đồ pin hoặc hướng dẫn đấu nối trong bài.

Theo dõi thăm dò một tuần nếu đủ điều kiện, không dùng thử nghiệm để khuyến khích ăn thực phẩm đáng ngờ. Không diễn giải một tuần ít bỏ đồ là hiệu quả đã được chứng minh.

## 5. Điều kiện Go / Not Yet / No-Go

| Quyết định | Căn cứ cần có |
|---|---|
| Go với pilot giới hạn | Nhu cầu được xác nhận, cảm biến và định danh đạt mục tiêu, người dùng chấp nhận thao tác, phần cứng đủ điều kiện và có người phụ trách |
| Not Yet | Thiếu dữ liệu, danh tính sự kiện còn mơ hồ, kết nối/nguồn chưa ổn định hoặc chưa so được với cách đơn giản |
| No-Go cho FreshBox ở phân khúc này | Nhãn/app đã đủ, công xác nhận quá lớn hoặc khung gây bất tiện hơn lợi ích |
| No-Go cho nhánh AI | OCR không giảm công nhập + sửa so với chọn tay hoặc thêm lỗi khó phát hiện |

Các mục tiêu tại [bảng metric](03-problem-statement.md) là ngưỡng đề xuất; nhóm cần thống nhất trước khi thử.

## 6. Fallback và điều kiện dừng một lượt thử

- Không rõ món: giữ “chờ xác nhận”; không sửa lịch sử của món khác.
- Cùng món quay lại: thêm sự kiện, giữ mốc gốc.
- Thiếu thời gian/nguồn: ghi chưa rõ; người dùng bổ sung hoặc dùng nhãn tay.
- Mất kết nối: hiển thị lần cập nhật cuối; nhắc trên điện thoại có thể bị trễ.
- Pin/nguồn bất thường hoặc nguyên mẫu cản vận hành tủ: dừng thử phần cứng để kiểm tra.
- Giao diện đưa ra lời bảo đảm “ăn được” từ giờ cất: sửa phạm vi và nội dung thông báo trước khi tiếp tục.

## 7. Nhóm cần chốt

- Người phụ trách xác nhận nhu cầu, log thử và phần cứng: **chưa được cung cấp**.
- Người làm phần nào và phản biện đã nêu: **chưa được cung cấp**.
- Decision cuối, bằng chứng xác nhận/phản bác và phạm vi tiếp theo: **nhóm bổ sung sau kiểm chứng**.

Mẫu nhắc minh họa: “Hộp A được ghi nhận đặt vào lúc …; đến mốc bạn đã chọn để kiểm tra. Hãy xem thông tin nhãn và lịch sử bảo quản.” Đây là nội dung đề xuất, không phải tin nhắn đã được hệ thống gửi.
